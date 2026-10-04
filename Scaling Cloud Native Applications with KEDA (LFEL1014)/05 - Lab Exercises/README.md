---
title: Lab Exercises
document_type: lesson
source: The Linux Foundation Training Portal
source_url: https://trainingportal.linuxfoundation.org/learn/course/scaling-cloud-native-applications-with-keda-lfel1014/lab-exercises/getting-hands-on-1?page=1
course: Scaling Cloud Native Applications with KEDA (LFEL1014)
lesson_order: 5
---

# Lab Exercises

## Source lab guides

The course provides these three downloadable guides. The course page provides the source downloads:

- [Lab 1: Setting Up the Course Lab Environment](media/lab-1-environment-guide.pdf)
- [Lab 2: Implementing HPA in Kubernetes](media/lab-2-hpa-guide.pdf)
- [Lab 3: Installing KEDA and Setting Up Cron Scaler](media/lab-3-keda-cron-guide.pdf)

## Section and SCORM overview

The portal section is **Lab Exercises**, with the source page **Getting Hands On** and the internal page **Hands-On Practice**. The embedded module is titled **Chapter 5. Lab Exercises**. Its cover says the labs apply Kubernetes autoscaling concepts by setting up the environment, implementing HPA in Kubernetes, and configuring KEDA for event-driven scaling with a Cron scaler.

### Lab table of contents

The SCORM table of contents lists three labs, all unstarted when the cover was observed:

1. Lab 1. Setting Up the Course Lab Environment
2. Lab 2. Implementing HPA in Kubernetes
3. Lab 3. Installing KEDA and Setting Up Cron Scaler

The portal repeats the course navigation instructions: begin the lesson, use its menu, advance with the next-lesson control at the bottom of each page, and finish all content before using the gray next-section arrow. The cover repeats the cloud/KEDA artwork used in Chapter 4: a KEDA wordmark inside an outlined hexagon beneath a Kubernetes symbol, with cloud backdrop, blue down arrow, green up arrow, and pod-like containers.

## Lab 1. Setting Up the Course Lab Environment

### Goal and prerequisites

The lab prepares a Linux host for later Kubernetes autoscaling exercises. Its overview assigns Docker to provision the cluster through kind, kind to create the cluster, kubectl to manage it, Helm to install Kubernetes packages, and Siege to generate HTTP/FTP load. The course-information section recommends an Ubuntu 24.04 VM; this lab guide assumes an Ubuntu host and uses a local kind cluster. The PDF is titled `Lab 1. Setting Up the Course Lab Environment` and carries the revision label `LFEL1014-v10.21.2025`.

### Exercise 1.1: install the tools

Install Docker with the convenience script, enable and start the service, verify status, add the current user to the `docker` group, re-open the shell session, and verify that Docker responds:

```bash
curl -fsSL https://get.docker.com/ | sh
sudo systemctl enable --now docker
sudo systemctl status docker
sudo usermod -aG docker "$USER"
# Exit and log in again to refresh group membership.
docker ps
```

The guide installs the latest kubectl release by reading the version from Kubernetes' `stable.txt` endpoint, downloading the Linux AMD64 binary, making it executable, and moving it into `/usr/local/bin`:

```bash
curl -sSL -O "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl"
chmod +x kubectl
sudo mv kubectl /usr/local/bin
```

For Helm, the guide downloads Helm v3.19.0 for Linux AMD64, extracts it, and installs the binary into `/usr/local/bin/helm`:

```bash
curl -sSL -O https://get.helm.sh/helm-v3.19.0-linux-amd64.tar.gz
tar -zxf helm-v3.19.0-linux-amd64.tar.gz
sudo mv linux-amd64/helm /usr/local/bin/helm
```

Install Siege from Ubuntu's package repository with `sudo apt-get install siege`. The guide characterizes it as a multithreaded HTTP/FTP load-testing and benchmarking utility.

Install kind v0.30.0 using the binary that matches the host architecture. For `x86_64`, download `https://kind.sigs.k8s.io/dl/v0.30.0/kind-linux-amd64`; for `aarch64`, download `https://kind.sigs.k8s.io/dl/v0.30.0/kind-linux-arm64`. In either case, the guide saves the download as `./kind`, then runs `chmod +x ./kind` and `sudo mv ./kind /usr/local/bin/kind`.

### Create and verify the kind cluster

Create the default cluster with `kind create cluster`. The guide's sample output uses node image `kindest/node:v1.34.0`, prepares nodes, writes configuration, starts the control plane, installs CNI and the default StorageClass, then sets kubectl's context to `kind-kind`. Verify with `kubectl cluster-info --context kind-kind` and `kubectl get ns`. The sample namespace listing includes `default`, `kube-node-lease`, `kube-public`, `kube-system`, and `local-path-storage`, each Active.

### Install and validate Metrics Server

Add the Kubernetes SIGs Metrics Server Helm repository, install the chart into `kube-system`, and set `--kubelet-insecure-tls` as the first chart argument for this local lab cluster:

```bash
helm repo add metrics-server https://kubernetes-sigs.github.io/metrics-server/
helm upgrade --install metrics-server metrics-server/metrics-server -n kube-system --set args[0]=--kubelet-insecure-tls
kubectl get pods -n kube-system -l=app.kubernetes.io/name=metrics-server
```

The guide's sample deployment reports chart version 3.13.0, Metrics Server app version 0.8.0, and a pod in `1/1 Running` state. Its final line says the environment is ready. These version strings and command outputs are examples printed in the October 2025 guide, not live versions verified during this review.

### Visuals and media

The four-page PDF contains a blue Linux Foundation Education wordmark as its only embedded image, shown as a wide header banner on page 1; the remaining pages present prose, commands, and terminal output as text rather than screenshots. The banner is embedded below. The lab guide targets a separately provisioned Ubuntu 24.04 host.

![Blue Linux Foundation Education wordmark banner from the Lab 1 guide](img/lab1-linux-foundation-education.png)

## Lab 2. Implementing HPA in Kubernetes

### Goal and prerequisites

The lab provides hands-on practice with a Kubernetes Horizontal Pod Autoscaler (HPA). Its prerequisite is a Kubernetes cluster with Metrics Server installed as in Lab 1. The guide revision is `LFEL1014-v10.21.2025`.

### Exercise 2.1: deploy the sample web application

Create `webapp.yaml` for a Deployment named `webapp`, initially with two replicas and selector/template label `app: webapp`. The pod runs the `nginx` image with CPU request and limit each set to `10m`:

```yaml
apiVersion: apps/v1
kind: Deployment
metadata:
  name: webapp
spec:
  replicas: 2
  selector:
    matchLabels:
      app: webapp
  template:
    metadata:
      labels:
        app: webapp
    spec:
      containers:
      - image: nginx
        name: nginx
        resources:
          limits:
            cpu: "10m"
          requests:
            cpu: "10m"
```

Apply it with `kubectl apply -f webapp.yaml`; the sample `kubectl get deployments` output shows 2/2 Ready, 2 up-to-date, and 2 available. Start port forwarding in a separate terminal so it remains active while generating load: `kubectl port-forward deploy/webapp 8080:80`. The guide's sample says localhost ports 127.0.0.1:8080 and [::1]:8080 forward to port 80. Test with `curl http://localhost:8080/`; the sample response is the NGINX welcome HTML.

### Exercise 2.2: configure HPA and observe scaling

Create an HPA targeting the `webapp` Deployment, with a minimum of two replicas, maximum of five, and target CPU utilization of 20%:

```bash
kubectl autoscale deployment webapp --min=2 --max=5 --cpu-percent=20
kubectl get hpa
```

The sample first output says `horizontalpodautoscaler.autoscaling/webapp autoscaled`; `kubectl get hpa` reports a CPU target `0%/20%`, minPods 2, maxPods 5, and replicas 2. Generate traffic for one minute with two concurrent Siege clients:

```bash
siege -q -c 2 -t 1m http://localhost:8080
```

Monitor the HPA with `kubectl get hpa -w`. The example shows CPU at `20%/20%` and replicas increasing to 3. The guide explains `TARGETS` as current/average CPU against the target, `MINPODS` and `MAXPODS` as scaling bounds, and `REPLICAS` as the current pod count. There is a wording inconsistency: one paragraph says CPU above a **50% threshold**, while the command, HPA output, following explanation, and target definition all use **20%**. The sample scaling narrative also says that meeting the 20% target triggered an increase; this is a guide example, not a live-observed result.

### Cleanup

Remove the HPA and Deployment after the exercise:

```bash
kubectl delete hpa webapp
kubectl delete deploy webapp
```

### Visuals, media, and execution status

The four-page Lab 2 PDF repeats the blue Linux Foundation Education wordmark banner first seen on page 1 of the Lab 1 guide; there are no other embedded images, diagrams, or videos, and no audio. The lab requires the Ubuntu/kind environment from Lab 1. Its procedure covers deployment, load generation, scaling observation and cleanup.

## Lab 3. Installing KEDA and Setting Up Cron Scaler

### Goal and prerequisites

The lab provides practical experience installing KEDA and using a Cron `ScaledObject` to scale an application on a schedule. Its prerequisite is a Kubernetes cluster with Metrics Server installed as in Lab 1. The guide revision is `LFEL1014-v10.21.2025`.

### Exercise 3.1: install KEDA and deploy the application

Add and update the KEDA Helm repository, then install the chart as release `keda` in a new `keda` namespace:

```bash
helm repo add kedacore https://kedacore.github.io/charts
helm repo update
helm upgrade -i keda kedacore/keda --namespace keda --create-namespace
kubectl get deployment -n keda
```

The example shows three deployments—`keda-admission-webhooks`, `keda-operator`, and `keda-operator-metrics-apiserver`—each Ready 1/1 and Available. Create an NGINX application with two replicas and confirm it is ready:

```bash
kubectl create deploy myapp --image nginx --replicas=2
kubectl get deployments
```

The sample output reports `myapp` Ready 2/2, Up-to-Date 2, and Available 2.

### Configure the Cron ScaledObject

Create `cron.yaml` with a KEDA `ScaledObject` named `cron-scaledobject` in the `default` namespace. It targets Deployment `myapp` and uses a `cron` trigger in `Asia/Kolkata`; the schedule starts at minute 30 and ends at minute 45 of each hour, with a desired replica count of 10:

```yaml
apiVersion: keda.sh/v1alpha1
kind: ScaledObject
metadata:
  name: cron-scaledobject
  namespace: default
spec:
  scaleTargetRef:
    name: myapp
  triggers:
  - type: cron
    metadata:
      timezone: Asia/Kolkata
      start: 30 * * * *
      end: 45 * * * *
      desiredReplicas: "10"
```

The guide defines `timezone` as an IANA Time Zone Database value; `start` and `end` as five-field Linux cron expressions (minute, hour, day of month, month, day of week); and `desiredReplicas` as the count to use between the start and end schedule. Apply with `kubectl apply -f cron.yaml`, then inspect the resource with `kubectl get scaledobject.keda.sh`. Its sample row identifies an `apps/v1` Deployment target named `myapp`, Cron trigger, `READY=True`, `ACTIVE=False`, and `FALLBACK=Unknown`, with several blank/unspecified columns.

### Observe the scheduled scale-out

The guide asks learners to watch resources with `watch kubectl get all` and press Ctrl+C to stop. Its sample shows ten `myapp` Pods Ready and Running, Deployment `myapp` at 10/10, and a ReplicaSet with desired/current/ready all 10. It also shows `keda-hpa-cron-scaledobject` targeting `Deployment/myapp`, CPU `1/1 (avg)`, minPods 1, maxPods 100, and 10 replicas. The guide explains that the Cron scaler takes a workload from its minimum to the desired replica count while the configured time window is active. It describes this as a simple scheduled scaler and invites exploration of other scaler types. These outputs are examples from the guide.

### Cleanup and result status

The three-page Lab 3 guide includes no cleanup command. Its YAML example and sample workload output illustrate the scheduled scaling procedure; they are part of the course guide rather than results from running a cluster.

### Visuals and media

The PDF repeats the blue Linux Foundation Education wordmark banner from Labs 1 and 2. The remaining pages contain text, YAML, and terminal output rather than other embedded figures or screenshots. The cover art is described in the lesson; lab guides show their procedures, configuration examples and illustrative output.
