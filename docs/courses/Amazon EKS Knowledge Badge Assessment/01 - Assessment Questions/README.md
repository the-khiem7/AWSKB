---
title: Amazon EKS Knowledge Badge Assessment Questions
document_type: lesson
source: AWS Skill Builder
source_url: https://skillbuilder.aws/assessments/en/5b909209-f6c1-47aa-9026-2a536dc5f334/1/questions/8ba9153f-5ad5-4986-8b54-ae0f89ee7feb
course: Amazon EKS Knowledge Badge Assessment
lesson_order: 1
---

# Amazon EKS Knowledge Badge Assessment Questions

## Assessment questions

### Question 1 of 60

**Question:** You are a solutions architect advising a client on EKS deployment options. The client needs to deploy applications with ultra-low latency for 5G applications. Which AWS infrastructure component would you recommend?

**Choices:**

- A. AWS Local Zones
- B. AWS Outposts
- C. AWS Regions
- D. AWS Wavelength Zones

**Selection rule:** The platform presents four radio-button choices, so this question accepts one answer.

**Selected answer:** D. AWS Wavelength Zones. The radio button is visibly selected; correctness remains unconfirmed until the assessment provides feedback.

**Platform feedback:** Pending; no correctness feedback has been observed.

**Learning note:** AWS Wavelength Zones place compute and storage at the edge of 5G networks to support ultra-low-latency applications.

### Question 2 of 60

**Question:** A startup has deployed several applications in a single EKS cluster. They have received alerts that one of the nodes is utilizing 100% of the CPU. How can the customer determine which pods are responsible for the CPU spike using CloudWatch Container Insights Performance Monitoring?

**Choices:**

- A. Filter by EKS Nodes and identify pods with high CPU
- B. Filter by EKS Pods and identify by high CPU
- C. Filter by EKS Clusters and identify pods with high CPU
- D. This is not possible because Container Insights Performance Monitoring cannot see pod level metrics.

**Selection rule:** The platform presents four radio-button choices, so this question accepts one answer.

**Selected answer:** B. Filter by EKS Pods and identify by high CPU. The radio button is visibly selected; correctness remains unconfirmed until the assessment provides feedback.

**Platform feedback:** Pending; no correctness feedback has been observed.

**Learning note:** Container Insights performance monitoring exposes metrics by Kubernetes resource type. Filtering the EKS Pods view surfaces individual pods and their CPU use.

### Question 3 of 60

**Question:** A company is running a microservices application on Amazon EKS. The application consists of a front-end service, several back-end services, and a MongoDB database for persistence. The DevOps engineer wants to deploy MongoDB as a stateful workload. Which Kubernetes resource should be used to deploy MongoDB for data persistence?

**Choices:**

- A. StatefulSet
- B. ReplicaSet
- C. Deployment
- D. DaemonSet

**Selection rule:** The platform presents four radio-button choices, so this question accepts one answer.

**Selected answer:** A. StatefulSet. The radio button is visibly selected; correctness remains unconfirmed until the assessment provides feedback.

**Platform feedback:** Pending; no correctness feedback has been observed.

**Learning note:** A StatefulSet is designed for stateful applications that need stable pod identities and persistent storage. A database such as MongoDB uses it rather than a generic stateless Deployment.

### Question 4 of 60

**Question:** You are a DevOps engineer tasked with building a new continuous delivery pipeline to deploy applications on an EKS cluster. Your team is curious about using GitOps but needs to know the key difference between GitOps and traditional CI/CD workflow. Which option BEST summarizes this difference?

**Choices:**

- A. GitOps uses a pull process in which changes are pulled into the cluster by the agent while a traditional CI/CD workflow's CD server pushes changes onto the cluster.
- B. GitOps uses a push process while a traditional CD server pulls changes into the cluster.
- C. GitOps workflows use Git for source control while traditional CI/CD workflows do not.
- D. GitOps uses declarative manifests while traditional CI/CD workflows do not.

**Selection rule:** The platform presents four radio-button choices, so this question accepts one answer.

**Selected answer:** A. GitOps uses a pull process in which changes are pulled into the cluster by the agent while a traditional CI/CD workflow's CD server pushes changes onto the cluster. The radio button is visibly selected; correctness remains unconfirmed until the assessment provides feedback.

**Platform feedback:** Pending; no correctness feedback has been observed.

**Learning note:** GitOps normally has an in-cluster reconciliation agent pull the desired state from Git; traditional CD commonly pushes an artifact or configuration into the target environment.

### Question 5 of 60

**Question:** A team currently builds and runs Docker applications on Amazon EC2 and is evaluating Amazon EKS to orchestrate existing containers. Which EKS components help with deployment, scheduling, and container management? *(Select THREE.)*

**Choices:**

- A. AWS Systems Manager Agent
- B. kube-controller-manager
- C. CloudWatch Agent
- D. AWS DMS
- E. kube-apiserver
- F. kube-scheduler

**Selection rule:** The platform explicitly requires three checkbox choices.

**Selected answer:** B. kube-controller-manager; E. kube-apiserver; F. kube-scheduler. All three checkboxes are visibly selected; correctness remains unconfirmed until the assessment provides feedback.

**Platform feedback:** Pending; no correctness feedback has been observed.

**Learning note:** The kube-apiserver exposes the Kubernetes API, kube-controller-manager runs reconciliation controllers, and kube-scheduler assigns Pods to eligible nodes. The other choices are AWS services or agents, not core Kubernetes control-plane components.

### Question 6 of 60

**Question:** For organizations requiring air-gapped environments completely disconnected from the cloud, which EKS deployment option should they use?

**Choices:**

- A. Amazon EKS Anywhere
- B. EKS in AWS Regions
- C. EKS on Outposts
- D. Cloud-connected use case

**Selection rule:** The platform presents four radio-button choices, so this question accepts one answer.

**Selected answer:** A. Amazon EKS Anywhere. The radio button is visibly selected; correctness remains unconfirmed until the assessment provides feedback.

**Platform feedback:** Pending; no correctness feedback has been observed.

**Learning note:** Amazon EKS Anywhere is designed to run Kubernetes on customer-managed infrastructure, including disconnected or air-gapped environments. EKS on Outposts extends AWS infrastructure on premises but retains a cloud dependency.

### Question 7 of 60

**Question:** An organization needs application storage to outlive Pods and scale to hundreds of applications without manually creating volumes. What is the best approach?

**Choices:**

- A. Dynamic Provisioning: define a PersistentVolumeClaim and StorageClass; PersistentVolumes are provisioned automatically.
- B. Dynamic Provisioning: define a StorageClass; PersistentVolumes and PersistentVolumeClaims are provisioned automatically.
- C. Dynamic Provisioning: define a PersistentVolume, PersistentVolumeClaim, and StorageClass.
- D. Dynamic Provisioning: define only a PersistentVolume; PersistentVolumeClaims and StorageClasses are provisioned automatically.

**Selection rule:** The platform presents four radio-button choices, so this question accepts one answer.

**Selected answer:** A. Define a PersistentVolumeClaim and StorageClass; dynamically provision the PersistentVolume. The radio button is visibly selected; correctness remains unconfirmed until the assessment provides feedback.

**Platform feedback:** Pending; no correctness feedback has been observed.

**Learning note:** A StorageClass selects the dynamic provisioner, while an application declares its requested storage with a PersistentVolumeClaim. Kubernetes then provisions the backing PersistentVolume.

### Question 8 of 60

**Question:** Multiple EKS microservices must be exposed publicly over HTTP with low cost and minimum operational overhead. How should this be done?

**Choices:**

- A. Create a public LoadBalancer for each Service.
- B. Create a public NodePort for each Service.
- C. Use ExternalName to expose each Service externally.
- D. Create the AWS Load Balancer Controller and an Ingress resource with path-based mappings for the Services.

**Selection rule:** The platform presents four radio-button choices, so this question accepts one answer.

**Selected answer:** D. Use the AWS Load Balancer Controller and an Ingress with path-based mappings. The radio button is visibly selected; correctness remains unconfirmed until the assessment provides feedback.

**Platform feedback:** Pending; no correctness feedback has been observed.

**Learning note:** The AWS Load Balancer Controller provisions and configures an ALB from an Ingress. Path-based routing permits several HTTP services to share one load balancer.

### Question 9 of 60

**Question:** Cluster Autoscaler is installed but the deployment's application Pod count stays static as load changes. Which resource is missing to scale Pods based on utilization?

**Choices:**

- A. ReplicaSet
- B. Karpenter
- C. Vertical Pod Autoscaler
- D. Horizontal Pod Autoscaler

**Selection rule:** The platform presents four radio-button choices, so this question accepts one answer.

**Selected answer:** D. Horizontal Pod Autoscaler. The radio button is visibly selected; correctness remains unconfirmed until the assessment provides feedback.

**Platform feedback:** Pending; no correctness feedback has been observed.

**Learning note:** Cluster Autoscaler changes node capacity for unschedulable Pods. A HorizontalPodAutoscaler changes a workload's replica count from observed metrics, which can then trigger node scaling when needed.

### Question 10 of 60

**Question:** Which platform best supports consistent on-premises and cloud deployment, serverless applications, and highly available applications?

**Choices:**

- A. Run your own Kubernetes cluster.
- B. Create container microservices and use Terraform to manage workloads.
- C. Docker.
- D. Amazon EKS.

**Selection rule:** The platform presents four radio-button choices, so this question accepts one answer.

**Selected answer:** D. Amazon EKS. The radio button is visibly selected; correctness remains unconfirmed until the assessment provides feedback.

**Platform feedback:** Pending; no correctness feedback has been observed.

**Learning note:** Amazon EKS provides managed Kubernetes, high availability for its control plane, integration with serverless Fargate, and a consistent Kubernetes operating model across supported deployment options.

### Question 11 of 60

**Question:** A critical high-performance microservice needs a highly available EKS node group. Which type should be used?

**Choices:**

- A. Custom node group with Spot Instances.
- B. AWS Fargate node group.
- C. Managed node group with Spot Instances.
- D. Custom node group with On-Demand Instances.

**Selection rule:** The platform presents four radio-button choices, so this question accepts one answer.

**Selected answer:** D. Custom node group with On-Demand Instances. The radio button is visibly selected; correctness remains unconfirmed until the assessment provides feedback.

**Platform feedback:** Pending; no correctness feedback has been observed.

**Learning note:** On-Demand capacity avoids Spot interruption risk for a critical workload. A custom group permits high-performance instance selection and multi-AZ design when those requirements need direct control.

### Question 12 of 60

**Question:** A front end needs two replicas for high availability and public Internet access in EKS. Which Kubernetes objects meet the requirement?

**Choices:**

- A. A Deployment with two replicas, exposed by a Service of type LoadBalancer.
- B. Two Pods, each exposed by its own load balancer.
- C. One Pod with two containers, exposed by an Application Load Balancer.
- D. A ReplicaSet with two replicas, exposed by an Application Load Balancer.

**Selection rule:** The platform presents four radio-button choices, so this question accepts one answer.

**Selected answer:** A. A Deployment with two replicas and a LoadBalancer Service. The radio button is visibly selected; correctness remains unconfirmed until the assessment provides feedback.

**Platform feedback:** Pending; no correctness feedback has been observed.

**Learning note:** A Deployment maintains the requested replica count and supports rollout behavior. A `LoadBalancer` Service publishes a stable network endpoint that directs traffic to ready Pod endpoints.

### Question 13 of 60

**Question:** A polyglot EKS microservice estate has timeouts and high MTTR. It needs auto-instrumentation, standardization, and flexibility while tracing backends are still being evaluated. What is recommended?

**Choices:**

- A. Use the AWS Distro for OpenTelemetry SDK plus the ADOT add-on and collector to capture and send traces to X-Ray.
- B. Use the X-Ray SDK and X-Ray agent to capture and send traces to X-Ray.
- C. Use the X-Ray SDK and CloudWatch agent to capture and send traces to X-Ray.
- D. Use a Prometheus library and ADOT to send correlated metrics and traces to X-Ray.

**Selection rule:** The platform presents four radio-button choices, so this question accepts one answer.

**Selected answer:** A. Use ADOT SDK, add-on, and collector. The radio button is visibly selected; correctness remains unconfirmed until the assessment provides feedback.

**Platform feedback:** Pending; no correctness feedback has been observed.

**Learning note:** OpenTelemetry provides vendor-neutral APIs, SDKs, and semantic conventions. ADOT supports standard collection and export pipelines while preserving the ability to select a backend later.

### Question 14 of 60

**Question:** When deploying a single Kubernetes Pod, which consideration supports efficient and reliable operations?

**Choices:**

- A. CPU cores and RAM allocated to the Pod.
- B. Maximum Pods that can run on a node.
- C. Kubernetes version for cluster management.
- D. Geographical location of the cluster.

**Selection rule:** The platform presents four radio-button choices, so this question accepts one answer.

**Selected answer:** A. CPU cores and RAM allocated to the Pod. The radio button is visibly selected; correctness remains unconfirmed until the assessment provides feedback.

**Platform feedback:** Pending; no correctness feedback has been observed.

**Learning note:** Pod container resource requests influence scheduling and capacity planning, while resource limits constrain runtime consumption. Both must be chosen appropriately for workload reliability.

### Question 15 of 60

**Question:** How should application resources and team access be isolated in a shared EKS cluster?

**Choices:** A. `kube-system` namespace. B. Create a new namespace for the application. C. Separate worker node. D. `default` namespace.

**Selection rule:** One radio-button choice.

**Selected answer:** B. Create a new namespace for this application and deploy its resources there. The radio button is visibly selected; correctness remains unconfirmed until feedback.

**Platform feedback:** Pending.

**Learning note:** A namespace provides a logical scope for namespaced resources and RBAC rules; it supports least-privilege team access in a shared cluster.

### Question 16 of 60

**Question:** Which `docker container run` flag starts a locally run container with an interactive TTY session?

**Choices:** A. `--attach` B. `--it` C. `--link` D. `--expose`

**Selection rule:** One radio-button choice.

**Selected answer:** B. `--it`. The radio button is visibly selected; correctness remains unconfirmed until feedback.

**Platform feedback:** Pending.

**Learning note:** `-i` keeps standard input open and `-t` allocates a pseudo-terminal; `--it` is their combined shorthand.

### Question 17 of 60

**Question:** Which three Helm concepts should a team know when packaging Kubernetes manifests for EKS?

**Choices:** A. SSM document B. Repository C. AWS Artifact D. CloudFormation templates E. Release F. Chart

**Selection rule:** Select three checkbox choices.

**Selected answer:** B. Repository; E. Release; F. Chart. All three checkboxes are visibly selected; correctness remains unconfirmed until feedback.

**Platform feedback:** Pending.

**Learning note:** A Chart is the package, a Repository distributes Charts, and a Release is a named deployed instance of a Chart.

### Question 18 of 60

**Question:** How are IAM permissions configured for the EKS control plane?

**Choices:** A. Associate `AdministratorAccess`. B. Use an IAM user's access keys. C. Create an IAM role with `AmazonEKSClusterPolicy`, EKS service trust, and specify it during cluster creation. D. Use `AmazonEKSWorkerNodePolicy`.

**Selection rule:** One radio-button choice.

**Selected answer:** C. IAM role with `AmazonEKSClusterPolicy` and EKS service trust. The radio button is visibly selected; correctness remains unconfirmed until feedback.

**Platform feedback:** Pending.

**Learning note:** The EKS cluster IAM role is assumed by `eks.amazonaws.com` and grants the control plane the AWS permissions it requires. Node IAM permissions are separate.

### Question 19 of 60

**Question:** How can several externally exposed EKS services reduce load-balancer cost with minimal operational overhead?

**Choices:** A. Make all Services `ClusterIP`. B. Add an NLB ingress annotation to put them behind one ALB. C. Use NodePort and point DNS to one node. D. Expose all external Services with an Ingress.

**Selection rule:** One radio-button choice.

**Selected answer:** D. Expose all external-facing Services using an Ingress resource. The radio button is visibly selected; correctness remains unconfirmed until feedback.

**Platform feedback:** Pending.

**Learning note:** An Ingress, implemented through an ingress controller such as the AWS Load Balancer Controller, can route multiple hosts or paths through shared ALB infrastructure.

### Question 20 of 60

**Question:** Microservices are in separate namespaces. What is the lowest-overhead, cost-efficient public exposure approach?

**Choices:** A. One ALB Ingress in one namespace. B. AWS Load Balancer Controller, Ingress per namespace, shared IngressGroup and distinct paths. C. One NGINX Ingress in one namespace. D. A LoadBalancer Service per microservice.

**Selection rule:** One radio-button choice.

**Selected answer:** B. Separate Ingress resources joined by the same IngressGroup. The radio button is visibly selected; correctness remains unconfirmed until feedback.

**Platform feedback:** Pending.

**Learning note:** An Ingress is namespace-scoped. The AWS Load Balancer Controller's IngressGroup feature can consolidate compatible Ingress resources across namespaces onto one ALB.

### Question 21 of 60

**Question:** How can a connected EKS Anywhere cluster be viewed in the Amazon EKS console?

**Choices:** A. AWS Console directly B. CloudWatch C. Systems Manager D. EKS Connector

**Selection rule:** One radio-button choice.

**Selected answer:** D. EKS Connector. The radio button is visibly selected; correctness remains unconfirmed until feedback.

**Platform feedback:** Pending.

**Learning note:** EKS Connector registers supported external Kubernetes clusters with Amazon EKS for console visibility and selected management integration.

### Question 22 of 60

**Question:** An EKS API must be inaccessible outside its VPC and Kubernetes API activity must be audited. Which two cluster-creation actions are required?

**Choices:** A. Send control-plane audit logs to CloudWatch Logs. B. Public and private endpoint access. C. Public endpoint only. D. Private endpoint only. E. Send audit logs to S3.

**Selection rule:** Select two checkbox choices.

**Selected answer:** A. Enable audit logs to CloudWatch Logs; D. choose private endpoint access. Both checkboxes are visibly selected; correctness remains unconfirmed until feedback.

**Platform feedback:** Pending.

**Learning note:** EKS control-plane logs, including audit logs, are exported to CloudWatch Logs when enabled. A private-only endpoint restricts Kubernetes API network access to the VPC and connected networks.

### Question 23 of 60

**Question:** Which Kubernetes function gives a frontend reliable, cost-efficient in-cluster communication with ClusterIP backend APIs?

**Choices:** A. Use the resulting load balancer. B. Use CoreDNS Service DNS names. C. Use Pod IPs. D. Use Pod names.

**Selection rule:** One radio-button choice.

**Selected answer:** B. Use Service DNS names assigned by CoreDNS. The radio button is visibly selected; correctness remains unconfirmed until feedback.

**Platform feedback:** Pending.

**Learning note:** Kubernetes Services provide stable virtual IPs and DNS names while their backing Pods can be replaced or rescheduled.

### Question 24 of 60

**Question:** A scanned container image is compromised and sending traffic to an unknown IP. Which three possible causes remain?

**Choices:** A. Embedded malware B. Distroless images C. Privilege escalation from misconfiguration D. Immutable image tags E. Social engineering hack F. Zero-day vulnerability

**Selection rule:** Select three checkbox choices.

**Selected answer:** A. Embedded malware; C. privilege escalation from misconfiguration; F. zero-day vulnerability. All three checkboxes are visibly selected; correctness remains unconfirmed until feedback.

**Platform feedback:** Pending.

**Learning note:** Image scanning reduces known-vulnerability exposure but does not eliminate runtime misconfiguration, malware that evades detection, or newly discovered vulnerabilities.

### Question 25 of 60

**Question:** Which two authentication methods are available for EKS Anywhere when connected to AWS?

**Choices:** A. Secret keys B. Certificate-based authentication C. Password authentication D. IAM role for service account E. AWS IAM for cluster authentication

**Selection rule:** Select two checkbox choices.

**Selected answer:** B. Certificate-based authentication; E. AWS IAM for cluster authentication. Both checkboxes are visibly selected; correctness remains unconfirmed until feedback.

**Platform feedback:** Pending.

**Learning note:** EKS Anywhere supports Kubernetes certificate credentials and can integrate connected clusters with AWS IAM authentication. IRSA is a workload identity mechanism, not a human cluster-authentication method.

### Question 26 of 60

**Question:** Which statement about an EKS Ingress controller is true?

**Choices:** A. It defines routing rules for external traffic. B. It routes internal Pod-to-Pod traffic. C. It is only needed for a single AZ. D. EKS provisions it automatically without configuration.

**Selection rule:** One radio-button choice.

**Selected answer:** A. It defines external-traffic routing rules. The radio button is visibly selected; correctness remains unconfirmed until feedback.

**Platform feedback:** Pending.

**Learning note:** An Ingress resource defines HTTP(S) routing intent, while an installed Ingress controller implements that intent. EKS itself does not automatically supply an Ingress controller.

### Question 27 of 60

**Question:** A critical Kubernetes application must be highly available and retain user preferences across restarts. What deployment approach fits?

**Choices:** A. Stateful on one node B. Stateless/manual scale C. Stateless/internal only D. Stateful with two or more replicas

**Selection rule:** One radio-button choice.

**Selected answer:** D. Stateful application with two or more replicas. The radio button is visibly selected; correctness remains unconfirmed until feedback.

**Platform feedback:** Pending.

**Learning note:** State must live in durable storage and the workload needs a high-availability topology. Stateful workloads use stable identities and persistent volumes; replicas must be designed with the application's replication model.

### Question 28 of 60

**Question:** What are two advantages of GitOps and Continuous Operations?

**Choices:** A. Securely store API keys/passwords in Git B. Identify incorrectly written tests C. Reproducible automated application and infrastructure deployments D. Git as system desired-state source of truth E. Ensures agile methodology

**Selection rule:** Select two checkbox choices.

**Selected answer:** C. Reproducible automated deployments; D. Git as the desired-state source of truth. Both checkboxes are visibly selected; correctness remains unconfirmed until feedback.

**Platform feedback:** Pending.

**Learning note:** GitOps versions and reviews declarative desired state in Git. Reconciliation agents continuously converge environments on that state, yielding repeatable deployment and audit trails.

### Question 29 of 60

**Question:** How can Pods be prevented from receiving traffic before they have completed initialization?

**Choices:** A. Readiness probe with a shared 5-second delay B. Readiness probe with delay fitted to each application's startup time C. Readiness probe defaults D. Liveness probe

**Selection rule:** One radio-button choice.

**Selected answer:** B. Configure a readiness probe with `initialDelaySeconds` based on each application's startup time. The radio button is visibly selected; correctness remains unconfirmed until feedback.

**Platform feedback:** Pending.

**Learning note:** A readiness probe controls whether a Pod is placed in Service endpoints. It must reflect actual initialization behavior; a liveness probe instead determines whether Kubernetes restarts a container.

### Question 30 of 60

**Question:** Which Kubernetes resource best creates and manages Pods for an application?

**Choices:** A. Deployments B. Pods C. Namespaces D. Services

**Selection rule:** One radio-button choice.

**Selected answer:** A. Deployments. The radio button is visibly selected; correctness remains unconfirmed until feedback.

**Platform feedback:** Pending.

**Learning note:** A Deployment manages a ReplicaSet and declaratively maintains a set of Pods, including rollout and rollback behavior.

### Question 31 of 60

**Question:** Which command begins building a final image from a prepared Dockerfile?

**Choices:** A. `docker tag` B. `docker pull` C. `docker build` D. `docker commit`

**Selection rule:** One radio-button choice.

**Selected answer:** C. `docker build`. The radio button is visibly selected; correctness remains unconfirmed until feedback.

**Platform feedback:** Pending.

**Learning note:** `docker build` reads a Dockerfile and build context to construct an image; `tag` labels an existing image and `pull` retrieves one.

### Question 32 of 60

**Question:** Which Kubernetes object supports rolling updates for a multiple-Pod web application?

**Choices:** A. Neither Deployment nor ReplicaSet B. ReplicaSet only C. Both D. Deployment only

**Selection rule:** One radio-button choice.

**Selected answer:** D. Deployment only. The radio button is visibly selected; correctness remains unconfirmed until feedback.

**Platform feedback:** Pending.

**Learning note:** A Deployment manages a rolling update strategy over ReplicaSets. A ReplicaSet itself only maintains the desired number of matching Pods.

### Question 33 of 60

**Question:** What is GitHub Actions' role when deploying EKS microservices?

**Choices:** A. Production scaling monitoring B. EKS GUI C. Automate GitHub code build, test, package, release, or deployment jobs/workflows D. In-cluster service communication

**Selection rule:** One radio-button choice.

**Selected answer:** C. Automate build, test, package, release, or deployment workflows from GitHub to EKS. The radio button is visibly selected; correctness remains unconfirmed until feedback.

**Platform feedback:** Pending.

**Learning note:** GitHub Actions is CI/CD automation hosted around repository events and workflows; it is not a Kubernetes control-plane or service-mesh capability.

### Question 34 of 60

**Question:** With default VPC CNI and node subnets `192.168.32.0/19` and `192.168.64.0/19`, which IP could an EKS Pod use for a VPC-local outbound call?

**Choices:** A. `10.52.36.11` B. `172.16.25.5` C. `192.168.67.9` D. `127.0.0.1`

**Selection rule:** One radio-button choice.

**Selected answer:** C. `192.168.67.9`. The radio button is visibly selected; correctness remains unconfirmed until feedback.

**Platform feedback:** Pending.

**Learning note:** With the Amazon VPC CNI default networking, Pods receive VPC-routable addresses from the node subnet. `192.168.67.9` is inside `192.168.64.0/19`.

### Question 35 of 60

**Question:** What is the correct basic sequence to containerize an application?

**Choices:** A. Dockerfile, build image, push to registry B. Choose cloud, Dockerfile, build, load balancer C. Choose registry, Dockerfile, build, production deployment D. Architecture, Dockerfile, build, Kubernetes deployment

**Selection rule:** One radio-button choice.

**Selected answer:** A. Write a Dockerfile, build the image, then push it to a container registry. The radio button is visibly selected; correctness remains unconfirmed until feedback.

**Platform feedback:** Pending.

**Learning note:** A Dockerfile defines the image recipe; image build produces the artifact; a registry then makes the immutable image available for deployments.

### Question 36 of 60

**Question:** Which two managed policies minimally let EKS worker nodes join the cluster and pull images?

**Choices:** A. `AmazonEKSWorkerNodePolicy` B. `AdministratorAccess` C. `AmazonEC2FullAccess` D. `AmazonEKSClusterPolicy` E. `AmazonEC2ContainerRegistryReadOnly`

**Selection rule:** Select two checkbox choices.

**Selected answer:** A. `AmazonEKSWorkerNodePolicy`; E. `AmazonEC2ContainerRegistryReadOnly`. Both checkboxes are visibly selected; correctness remains unconfirmed until feedback.

**Platform feedback:** Pending.

**Learning note:** Nodes need the worker-node policy to interact with EKS and ECR read permissions to retrieve images. Cluster-control-plane permissions and broad EC2/admin access are not least privilege.

### Question 37 of 60

**Question:** Which statement best summarizes Kubernetes cluster architecture?

**Choices:** A. API server, etcd, controllers, scheduler and DNS all on control plane B. Control plane API/scheduler/controllers, worker application nodes, and etcd C. Pods, Services, ReplicaSets, namespaces only D. Workers and one master

**Selection rule:** One radio-button choice.

**Selected answer:** B. Control-plane components, worker nodes, and the etcd distributed store. The radio button is visibly selected; correctness remains unconfirmed until feedback.

**Platform feedback:** Pending.

**Learning note:** The control plane makes global decisions and reconciles desired state; worker nodes run Pods. etcd persists cluster state.

### Question 38 of 60

**Question:** At least how many days before an EKS Kubernetes minor version end-of-support date are customers notified?

**Choices:** A. 30 B. 90 C. 60 D. 15

**Selection rule:** One radio-button choice.

**Selected answer:** C. 60 days. The radio button is visibly selected; correctness remains unconfirmed until feedback.

**Platform feedback:** Pending.

**Learning note:** EKS communicates planned minor-version end-of-support dates in advance so customers can schedule cluster and workload compatibility upgrades.

### Question 39 of 60

**Question:** Which Service type exposes a private-subnet payment microservice both internally and externally while distributing traffic across Pods?

**Choices:** A. ClusterIP B. LoadBalancer C. NodePort D. Headless

**Selection rule:** One radio-button choice.

**Selected answer:** B. LoadBalancer. The radio button is visibly selected; correctness remains unconfirmed until feedback.

**Platform feedback:** Pending.

**Learning note:** A LoadBalancer Service provisions an external load-balancing entry point (subject to annotations/configuration) and retains the usual in-cluster Service DNS and load distribution.

### Question 40 of 60

**Question:** Which statement is a Docker container-image build best practice?

**Choices:** A. Use an unpinned latest base image B. Version tags are unimportant C. Install unnecessary packages D. Use multi-stage images to separate build tools from runtime dependencies

**Selection rule:** One radio-button choice.

**Selected answer:** D. Use multi-stage images with separate build and runtime stages. The radio button is visibly selected; correctness remains unconfirmed until feedback.

**Platform feedback:** Pending.

**Learning note:** Multi-stage builds keep compilers and other build-only dependencies out of the runtime image, reducing size and attack surface.

### Question 41 of 60

**Question:** A deny-all ingress/egress policy blocked an entire namespace, but only Pods A and B should be blocked. How should it be fixed?

**Choices:** A. Label Pods A/B and set `podSelector` to those labels B. Remove Egress policy type C. Remove Ingress policy type D. Restart Pods

**Selection rule:** One radio-button choice.

**Selected answer:** A. Select only Pods A and B with labels in `podSelector`. The radio button is visibly selected; correctness remains unconfirmed until feedback.

**Platform feedback:** Pending.

**Learning note:** A NetworkPolicy's `podSelector` scopes the policy to matching Pods in its namespace; an empty selector applies to every Pod in that namespace.

### Question 42 of 60

**Question:** What is GitOps' key benefit for EKS automation?

**Choices:** A. Faster builds B. Reduced server maintenance C. Centralized version control and change tracking D. Enhanced container security

**Selection rule:** One radio-button choice.

**Selected answer:** C. Centralized version control and change tracking. The radio button is visibly selected; correctness remains unconfirmed until feedback.

**Platform feedback:** Pending.

**Learning note:** Git is the reviewable, auditable desired-state record in a GitOps workflow; automation reconciles deployed state from it.

### Question 43 of 60

**Question:** Which Docker CLI command accepts CPU and memory constraints while starting a container?

**Choices:** A. `docker create` B. `docker exec` C. `docker start` D. `docker run`

**Selection rule:** One radio-button choice.

**Selected answer:** D. `docker run`. The radio button is visibly selected; correctness remains unconfirmed until feedback.

**Platform feedback:** Pending.

**Learning note:** `docker run` supports options such as `--cpus` and `--memory` at container creation time.

### Question 44 of 60

**Question:** How should a non-HTTP TCP/5000 application on private-subnet EKS nodes be exposed to the public Internet?

**Choices:** A. Ingress B. LoadBalancer Service using NLB C. ClusterIP D. NodePort

**Selection rule:** One radio-button choice.

**Selected answer:** B. A LoadBalancer Service configured for an NLB. The radio button is visibly selected; correctness remains unconfirmed until feedback.

**Platform feedback:** Pending.

**Learning note:** An NLB operates at Layer 4 and supports arbitrary TCP traffic. Ingress is mainly HTTP(S) routing, while ClusterIP is internal-only.

### Question 45 of 60

**Question:** Which Kubernetes component is responsible for ensuring an upgrade is performed safely and reliably?

**Choices:** A. Scheduler B. Kubelet C. API server D. Controller manager

**Selection rule:** One radio-button choice.

**Selected answer:** D. Kubernetes controller manager. The radio button is visibly selected; correctness remains unconfirmed until feedback.

**Platform feedback:** Pending.

**Learning note:** Controllers reconcile actual state against desired state and coordinate lifecycle changes. The scheduler places Pods and the kubelet manages node-local workloads.

### Question 46 of 60

**Question:** How can EKS administrative actions be audited and reviewed for compliance and debugging?

**Choices:** A. Enable EKS control-plane logs to CloudWatch Logs and use metric filters/alarms B. Container Insights C. CloudTrail to S3 D. Control-plane logs are enabled by default

**Selection rule:** One radio-button choice.

**Selected answer:** A. Enable EKS control-plane logs in CloudWatch Logs with filters and alarms. The radio button is visibly selected; correctness remains unconfirmed until feedback.

**Platform feedback:** Pending.

**Learning note:** EKS control-plane audit logs capture Kubernetes API activity and are disabled until explicitly selected. CloudWatch filtering and alarms support ongoing review.

### Question 47 of 60

**Question:** What is a strong reason to adopt containerization?

**Choices:** A. Long-term persistent storage B. Span hosts without complex config C. Simplifies updates and rollbacks, reducing deployment-failure risk D. Guarantees hardware isolation

**Selection rule:** One radio-button choice.

**Selected answer:** C. Simplified updates and rollbacks. The radio button is visibly selected; correctness remains unconfirmed until feedback.

**Platform feedback:** Pending.

**Learning note:** Containers package the application and its runtime dependencies into a versioned artifact, enabling consistent rollout and rapid rollback processes.

### Question 48 of 60

**Question:** Which Kubernetes mechanism restricts traffic between Pods in different namespaces for multi-tenant EKS network segmentation?

**Choices:** A. Built-in restriction B. Security groups for Pods C. NetworkPolicy D. Cluster security group

**Selection rule:** One radio-button choice.

**Selected answer:** C. NetworkPolicy. The radio button is visibly selected; correctness remains unconfirmed until feedback.

**Platform feedback:** Pending.

**Learning note:** NetworkPolicies select Pods and define permitted ingress/egress peers, including namespace selectors. A compatible CNI implementation must enforce them.

### Question 49 of 60

**Question:** What are two major StatefulSet differences from ReplicaSets?

**Choices:** A. Stable identity and ordered indexing B. No ordering/uniqueness C. Only ReplicaSets manage Pods D. StatefulSets share one PVC/ReplicaSets one per Pod E. ReplicaSets share PVCs/StatefulSets create one PVC per replica

**Selection rule:** Select two checkbox choices.

**Selected answer:** A. Stable identity and ordered indexing; E. StatefulSets create one PVC per replica. Both checkboxes are visibly selected; correctness remains unconfirmed until feedback.

**Platform feedback:** Pending.

**Learning note:** StatefulSets maintain ordinal Pod identities and can use `volumeClaimTemplates` so each replica receives durable, separate storage.

### Question 50 of 60

**Question:** With Karpenter using both Spot and On-Demand capacity, how can availability be protected during Spot interruptions?

**Choices:** A. More Spot nodes B. `minReady` C. Minimum capacity greater than On-Demand count D. `maxUnavailable`

**Selection rule:** One radio-button choice.

**Selected answer:** D. Set Karpenter `maxUnavailable`. The radio button is visibly selected; correctness remains unconfirmed until feedback.

**Platform feedback:** Pending.

**Learning note:** Limiting concurrent unavailable nodes preserves baseline service capacity while node provisioning and disruption handling replace capacity.

### Question 51 of 60

**Question:** Which statement best describes EKS cluster components?

**Choices:** A. Customer controls master and workers B. Customer-hosted control plane C. No managed control plane D. Managed master/control-plane components with Pods on worker nodes

**Selection rule:** One radio-button choice.

**Selected answer:** D. Master/control-plane components orchestrate while application Pods run on worker nodes. The radio button is visibly selected; correctness remains unconfirmed until feedback.

**Platform feedback:** Pending.

**Learning note:** EKS provides the managed Kubernetes control plane; workload compute runs on customer-selected capacity such as managed nodes, self-managed nodes, or Fargate.

### Question 52 of 60

**Question:** Which statement best describes a container?

**Choices:** A. Encapsulates app code and runtime dependencies B. Storage-only C. Full OS virtual machine D. Windows-only

**Selection rule:** One radio-button choice.

**Selected answer:** A. It packages application code with runtime dependencies for environmental consistency. The radio button is visibly selected; correctness remains unconfirmed until feedback.

**Platform feedback:** Pending.

**Learning note:** Containers use operating-system isolation and share the host kernel rather than emulating an entire guest OS like a VM.

### Question 53 of 60

**Question:** What is the simplest proactive way to identify trends and anomalies in Container Insights metrics across hundreds of EKS clusters?

**Choices:** A. DevOps Guru consumes CloudWatch metrics B. ADOT forwards metrics to DevOps Guru C. GuardDuty EKS protection D. Application Insights

**Selection rule:** One radio-button choice.

**Selected answer:** A. Configure Amazon DevOps Guru to continuously analyze the CloudWatch metrics. The radio button is visibly selected; correctness remains unconfirmed until feedback.

**Platform feedback:** Pending.

**Learning note:** DevOps Guru uses CloudWatch metrics and related signals to produce anomaly insights; Container Insights already supplies the relevant container metrics.

### Question 54 of 60

**Question:** What best describes `kubectl`?

**Choices:** A. Direct infrastructure changes B. Avoid it for UIs C. CLI to run commands against clusters, deploy/view/manage workloads D. Local manifest authoring only

**Selection rule:** One radio-button choice.

**Selected answer:** C. The Kubernetes command-line tool for deploying, viewing, and managing workloads. The radio button is visibly selected; correctness remains unconfirmed until feedback.

**Platform feedback:** Pending.

**Learning note:** `kubectl` authenticates to the Kubernetes API server and submits/queries resource operations defined by its context and credentials.

### Question 55 of 60

**Question:** What is the most efficient way to allocate shared EKS costs to application teams?

**Choices:** A. Spot/Karpenter B. Kubecost across Kubernetes resources C. Priority expander D. Cost Explorer/Savings Plans

**Selection rule:** One radio-button choice.

**Selected answer:** B. Kubecost for all Kubernetes resources. The radio button is visibly selected; correctness remains unconfirmed until feedback.

**Platform feedback:** Pending.

**Learning note:** Kubecost can attribute Kubernetes spend by namespace, labels, workloads, and teams, which supports shared-cluster chargeback.

### Question 56 of 60

**Question:** A readiness probe passes but the liveness probe repeatedly fails. What can this indicate?

**Choices:** A. Healthy but misconfigured B. Readiness too strict C. It is ready initially but later becomes unresponsive from an internal issue D. Normal/no issue

**Selection rule:** One radio-button choice.

**Selected answer:** C. An internal issue makes an initially ready application unresponsive later. The radio button is visibly selected; correctness remains unconfirmed until feedback.

**Platform feedback:** Pending.

**Learning note:** Readiness determines endpoint eligibility, whereas liveness detects a wedged/unrecoverable container and causes a restart when it fails according to configured thresholds.

### Question 57 of 60

**Question:** What is the most secure way for an EKS Pod to access an S3 bucket?

**Choices:** A. Node instance profile B. VPC endpoint C. IAM user access keys in Pod D. Pod Identity with a service account

**Selection rule:** One radio-button choice.

**Selected answer:** D. Use Pod Identity with a service account. The radio button is visibly selected; correctness remains unconfirmed until feedback.

**Platform feedback:** Pending.

**Learning note:** Pod Identity associates a least-privilege IAM role with a workload identity, avoiding shared node credentials and long-lived access keys.

### Question 58 of 60

**Question:** Which command queries the API server for Pod status and IP address?

**Choices:** A. `kubectl get pods -o wide` B. `apt-get` C. `systemctl` D. `etcdctl`

**Selection rule:** One radio-button choice.

**Selected answer:** A. `kubectl get pods -o wide`. The radio button is visibly selected; correctness remains unconfirmed until feedback.

**Platform feedback:** Pending.

**Learning note:** The wide output includes node and Pod IP columns in addition to status information.

### Question 59 of 60

**Question:** What deploys logging separately from application logic while keeping both components tightly coupled and sharing a Pod IP?

**Choices:** A. App sends logs directly B. Logging-agent sidecar in same Pod C. Agent in another Pod D. DaemonSet agent

**Selection rule:** One radio-button choice.

**Selected answer:** B. A logging-agent sidecar in the same Pod. The radio button is visibly selected; correctness remains unconfirmed until feedback.

**Platform feedback:** Pending.

**Learning note:** Containers in one Pod are scheduled together and share networking. A sidecar separates responsibilities while remaining part of the same deployable unit.

### Question 60 of 60

**Question:** How can images pushed to ECR be automatically scanned for CVEs and findings made available in Security Hub?

**Choices:** A. ECS B. Hadolint to Security Hub C. Hadolint text reports D. Amazon Inspector

**Selection rule:** One radio-button choice.

**Selected answer:** D. Enable Amazon Inspector. The radio button is visibly selected; correctness remains unconfirmed until platform feedback.

**Platform feedback:** The result export confirms this question was answered, but provides no item-level correctness verdict. The assessment passed overall.

**Learning note:** Amazon Inspector enhanced scanning for ECR continuously scans eligible images and can send findings to AWS Security Hub.

## Progress

- Source state observed: Passed, 96% on attempt 1 (58 correct, 2 incorrect, 0 skipped).
- Outcome reconciled: yes, from the user-provided AWS Skill Builder result-page export.
- Evidence: total time 27 minutes 31 seconds; average 28 seconds per question.
- Item-level feedback: the result export confirms every question was answered, but does not identify the two incorrect questions.
- Credential status: the export confirms a passing result but does not show badge or credential issuance.
- Access gaps: none observed.
- Platform status: assessment passed; no further assessment action is pending.
