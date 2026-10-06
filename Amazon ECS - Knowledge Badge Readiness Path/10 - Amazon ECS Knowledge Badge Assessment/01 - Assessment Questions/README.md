---
title: Amazon ECS Knowledge Badge Assessment
document_type: lesson
source: AWS Skill Builder
source_url: https://skillbuilder.aws/learn/S8122GC28K/amazon-ecs-knowledge-badge-assessment/BJTT9E5E9P?parentId=Q2R57WU6TT
learning_path: Amazon ECS - Knowledge Badge Readiness Path
course: Amazon ECS Knowledge Badge Assessment
lesson_order: 1
---

# Amazon ECS Knowledge Badge Assessment

AWS Skill Builder describes this assessment as validation of comprehension of the Amazon ECS Knowledge Badge Readiness Path. Its page says questions are based on the path's courses, question order is randomized per attempt, and a score of 80% or better can earn the badge. It states Credly issuance takes 5–7 business days. The learning-plan outline showed this training as In Progress.

## Assessment questions

### Question 1 of 60

**Question:** What capabilities does the Service Connect proxy provide without requiring application code changes?

**Choices:**

- A. Data encryption and certificate management
- B. Authentication and authorization for service requests
- C. Database connection pooling and query optimization
- D. Load balancing, health-based routing, and detailed metrics collection

**Selection rule:** The platform presents four radio-button choices, so this question accepts one answer. No answer had been selected when this question was first recorded.

**Selected answer:** D. Load balancing, health-based routing, and detailed metrics collection. The radio button is selected; correctness remains unconfirmed until the assessment provides feedback.

**Platform feedback:** Pending; no correctness feedback has been observed.

**Learning note:** Pending review against the lesson source and any assessment feedback.

## Progress

- Last saved step: Questions 1–60 are captured and selected; Question 60 is visibly selected. Correctness is unverified.
- Next action: submit the assessment to obtain actual score and feedback.
- Remaining sections: final assessment summary and platform feedback.
- Access gaps: none observed for Question 1.
- Platform status: In Progress; this note does not establish a score or badge award.



### Question 2 of 60

**Question:** What type of scanning does Amazon ECR provide by default for repositories?

**Choices:**

- A. Enhanced scanning with continuous monitoring enabled
- B. Basic scanning with improved features rolled out across the fleet
- C. Push-only scanning without vulnerability detection
- D. No scanning until manually configured by the user

**Selection rule:** The platform presents four radio-button choices, so this question accepts one answer.

**Selected answer:** B. Basic scanning with improved features rolled out across the fleet. The radio button is selected; correctness remains unconfirmed until the assessment provides feedback.

**Platform feedback:** Pending; no correctness feedback has been observed.

**Learning note:** Pending review against the lesson source and any assessment feedback.


### Question 3 of 60

**Question:** How does setting minimum healthy percentage to 50% affect rolling deployment behavior?

**Choices:**

- A. Only 50% of new tasks will be deployed at a time
- B. 50% of tasks must remain in pending state during deployment
- C. The deployment will maintain exactly 50% capacity throughout
- D. 50% of tasks can be stopped during the deployment process

**Selection rule:** The platform presents four radio-button choices, so this question accepts one answer.

**Selected answer:** D. 50% of tasks can be stopped during the deployment process. Correctness remains unconfirmed until the assessment provides feedback.

**Platform feedback:** Pending; no correctness feedback has been observed.

**Learning note:** The minimum healthy percentage is the lower bound for healthy service tasks during a rolling deployment; a value of 50% can allow service capacity to drop to half the desired count while tasks are replaced.



### Question 4 of 60

**Question:** What defines the container configuration and application code in ECS deployments?

**Choices:**

- A. Load balancer target group settings
- B. Task definitions with different revisions
- C. CodeDeploy application specifications
- D. Service configurations in the ECS cluster

**Selection rule:** The platform presents four radio-button choices, so this question accepts one answer.

**Selected answer:** B. Task definitions with different revisions. Correctness remains unconfirmed until the assessment provides feedback.

**Platform feedback:** Pending; no correctness feedback has been observed.

**Learning note:** An ECS task definition is the blueprint for an application: it specifies containers, images, resources, networking, and other runtime configuration. Revisions track changes to that blueprint.



### Question 5 of 60

**Question:** Which combination of VPC endpoints is required for ECS tasks to pull images from Amazon ECR?

**Choices:**

- A. ECR gateway endpoints and DynamoDB interface endpoints
- B. S3 interface endpoints and CloudWatch gateway endpoints
- C. ECR interface endpoints and S3 gateway endpoints
- D. Only ECR interface endpoints are sufficient for image pulling operations

**Selection rule:** The platform presents four radio-button choices, so this question accepts one answer.

**Selected answer:** C. ECR interface endpoints and S3 gateway endpoints. Correctness remains unconfirmed until the assessment provides feedback.

**Platform feedback:** Pending; no correctness feedback has been observed.

**Learning note:** Private image pulls from ECR use interface endpoints for ECR APIs and registry access, plus an S3 gateway endpoint for image layers stored in S3.



### Question 6 of 60

**Question:** What is the primary purpose of control groups (cgroups) in containers?

**Choices:**

- A. Enable containers to share files with the host system
- B. Isolate container processes from seeing each other
- C. Restrict what resources a container process can access
- D. Provide separate network interfaces for each container

**Selection rule:** The platform presents four radio-button choices, so this question accepts one answer.

**Selected answer:** C. Restrict what resources a container process can access. Correctness remains unconfirmed until the assessment provides feedback.

**Platform feedback:** Pending; no correctness feedback has been observed.

**Learning note:** Linux cgroups account for and limit resource use by process groups, including CPU and memory. Namespaces provide process, mount, network, and other isolation boundaries.



### Question 7 of 60

**Question:** How do control groups (cgroups) contribute to container isolation?

**Choices:**

- A. Control groups create separate network interfaces for each container application
- B. Control groups restrict what resources like CPU and memory a process can use
- C. Control groups automatically scale container resources based on application demand
- D. Control groups hide running processes from other containers on the system

**Selection rule:** The platform presents four radio-button choices, so this question accepts one answer.

**Selected answer:** B. Control groups restrict what resources like CPU and memory a process can use. Correctness remains unconfirmed until the assessment provides feedback.

**Platform feedback:** Pending; no correctness feedback has been observed.

**Learning note:** Cgroups account for and limit resource consumption by process groups. Process visibility isolation is supplied by namespaces, while ECS auto scaling is a separate service-level control.



### Question 8 of 60

**Question:** Which operating system choice provides the smallest attack surface for ECS workloads?

**Choices:**

- A. Amazon Linux 2023, because it includes the latest security patches and updates
- B. Bottlerocket, as it is built specifically to run containers with minimal components
- C. Any custom OS, as long as it is regularly updated with security patches
- D. Windows AMIs, since they provide familiar administrative tools and interfaces

**Selection rule:** The platform presents four radio-button choices, so this question accepts one answer.

**Selected answer:** B. Bottlerocket, as it is built specifically to run containers with minimal components. Correctness remains unconfirmed until the assessment provides feedback.

**Platform feedback:** Pending; no correctness feedback has been observed.

**Learning note:** Bottlerocket is a purpose-built host operating system for containers with a minimal footprint and managed updates; the reduced component set helps limit the attack surface.



### Question 9 of 60

**Question:** Which subnet type allows direct connection to tasks via public IP addresses?

**Choices:**

- A. Public subnets
- B. Database subnets
- C. NAT subnets
- D. Private subnets

**Selection rule:** The platform presents four radio-button choices, so this question accepts one answer.

**Selected answer:** A. Public subnets. Correctness remains unconfirmed until the assessment provides feedback.

**Platform feedback:** Pending; no correctness feedback has been observed.

**Learning note:** A task attached to a public subnet can use a public IP for direct internet connectivity when routing and security rules allow it. Private-subnet tasks typically use NAT for outbound access and load balancers or other routed paths for inbound traffic.



### Question 10 of 60

**Question:** What are the deployment differences for GuardDuty agents between ECS Fargate and ECS on EC2?

**Choices:**

- A. Fargate runs the agent as a sidecar container while EC2 runs it as a process on the instance
- B. Fargate runs the agent on the instance while EC2 runs it as a sidecar container
- C. Both deployment types run the agent as a sidecar container within each task
- D. Both deployment types run the agent as a process on the underlying compute instance

**Selection rule:** The platform presents four radio-button choices, so this question accepts one answer.

**Selected answer:** A. Fargate runs the agent as a sidecar container while EC2 runs it as a process on the instance. Correctness remains unconfirmed until the assessment provides feedback.

**Platform feedback:** Pending; no correctness feedback has been observed.

**Learning note:** Fargate does not expose the underlying host, so GuardDuty runtime monitoring uses an agent container in each task. On ECS with EC2 launch type, the agent runs at the host level.



### Question 11 of 60

**Question:** What is the recommended approach for resource management in ECS EC2 mode?

**Choices:**

- A. Always set explicit task limits for predictable performance
- B. Use only EC2 instance limits without task configuration
- C. Use container reservations instead of task limits
- D. Set task limits equal to EC2 instance capacity

**Selection rule:** The platform presents four radio-button choices, so this question accepts one answer.

**Selected answer:** C. Use container reservations instead of task limits. Correctness remains unconfirmed until the assessment provides feedback.

**Platform feedback:** Pending; no correctness feedback has been observed.

**Learning note:** Container resource reservations inform ECS placement and reserve capacity for scheduling. Hard limits constrain consumption; in EC2 mode they should be chosen deliberately rather than blindly set to instance capacity.



### Question 12 of 60

**Question:** Which IAM role allows the container or Fargate agent to pull images and write logs?

**Choices:**

- A. Task role
- B. Service linked role
- C. Task execution role
- D. Instance role

**Selection rule:** The platform presents four radio-button choices, so this question accepts one answer.

**Selected answer:** C. Task execution role. Correctness remains unconfirmed until the assessment provides feedback.

**Platform feedback:** Pending; no correctness feedback has been observed.

**Learning note:** The task execution role grants ECS/Fargate agent permissions needed to start a task, including pulling images and sending logs. The task role supplies credentials to the application containers for calls they make to AWS services.



### Question 13 of 60

**Question:** How many containers can be defined within a single ECS task definition?

**Choices:**

- A. Up to 10 containers
- B. Up to 5 containers
- C. Unlimited containers
- D. Up to 15 containers

**Selection rule:** The platform presents four radio-button choices, so this question accepts one answer.

**Selected answer:** A. Up to 10 containers. Correctness remains unconfirmed until the assessment provides feedback.

**Platform feedback:** Pending; no correctness feedback has been observed.

**Learning note:** An ECS task definition can specify multiple containers that are scheduled together as one task; the offered limit is 10 container definitions.




### Question 14 of 60

**Question:** Which AWS services require network connectivity for ECS container agents to function properly?

**Choices:**

- A. Only Amazon ECS control plane and CloudWatch
- B. Amazon ECS control plane and Route 53 only
- C. Amazon ECS control plane, ECR, and S3 for image layers
- D. ECR, Lambda, and API Gateway services

**Selection rule:** The platform presents four radio-button choices, so this question accepts one answer.

**Selected answer:** C. Amazon ECS control plane, ECR, and S3 for image layers. Correctness remains unconfirmed until the assessment provides feedback.

**Platform feedback:** Pending; no correctness feedback has been observed.

**Learning note:** The ECS agent needs the ECS control plane; image-pull paths also need ECR registry/API access and S3 access to image layers. Additional integrations such as CloudWatch Logs require their own network path when configured.



### Question 15 of 60

**Question:** What is the primary responsibility of an ECS service?

**Choices:**

- A. Managing the underlying EC2 infrastructure
- B. Running and maintaining a specified number of task instances simultaneously
- C. Storing container images in the registry
- D. Defining container images and CPU requirements

**Selection rule:** The platform presents four radio-button choices, so this question accepts one answer.

**Selected answer:** B. Running and maintaining a specified number of task instances simultaneously. Correctness remains unconfirmed until the assessment provides feedback.

**Platform feedback:** Pending; no correctness feedback has been observed.

**Learning note:** An ECS service maintains the desired number of task copies and replaces failed tasks; it can also attach tasks to load balancers and support rolling deployments.



### Question 16 of 60

**Question:** How should the assign public IP field be configured for tasks in private subnets?

**Choices:**

- A. Set to auto to let ECS decide automatically
- B. Set to disabled and use a NAT gateway for outbound traffic
- C. Set to disabled and configure an internet gateway
- D. Set to enabled to allow internet access

**Selection rule:** The platform presents four radio-button choices, so this question accepts one answer.

**Selected answer:** B. Set to disabled and use a NAT gateway for outbound traffic. Correctness remains unconfirmed until the assessment provides feedback.

**Platform feedback:** Pending; no correctness feedback has been observed.

**Learning note:** Tasks in private subnets should not receive public IPs. A NAT gateway can provide outbound internet access; VPC endpoints are another route for supported AWS services.



### Question 17 of 60

**Question:** How does the ECS service linked role get created in your AWS account?

**Choices:**

- A. Automatically created by Amazon ECS when you first create a cluster
- B. Generated by AWS CloudFormation during stack deployment
- C. Created automatically when the first task is launched
- D. Manually created by the user before launching any ECS resources

**Selection rule:** The platform presents four radio-button choices, so this question accepts one answer.

**Selected answer:** A. Automatically created by Amazon ECS when you first create a cluster. Correctness remains unconfirmed until the assessment provides feedback.

**Platform feedback:** Pending; no correctness feedback has been observed.

**Learning note:** ECS uses a service-linked role to call other AWS services on the account's behalf. ECS can create the role during initial use when it is absent.



### Question 18 of 60

**Question:** Which two parameters control how aggressively ECS can schedule new tasks during deployment?

**Choices:**

- A. Task launch speed and task shutdown speed
- B. Minimum healthy percent and maximum percent
- C. De-registration delay and health check timeout
- D. Circuit breaker threshold and health check interval

**Selection rule:** Although the prompt names two parameters, the platform shows four radio-button combinations and accepts one answer.

**Selected answer:** B. Minimum healthy percent and maximum percent. Correctness remains unconfirmed until the assessment provides feedback.

**Platform feedback:** Pending; no correctness feedback has been observed.

**Learning note:** ECS rolling deployments use minimumHealthyPercent to set the lower healthy-task bound and maximumPercent to set the upper number of tasks allowed during deployment.



### Question 19 of 60

**Question:** What is the primary benefit of implementing VPC endpoints for AWS services in an ECS architecture?

**Choices:**

- A. Traffic remains within the AWS network, improving security and potentially reducing NAT gateway costs
- B. VPC endpoints enable direct internet access for tasks in private subnets
- C. VPC endpoints eliminate the need for security groups on ECS tasks
- D. VPC endpoints automatically provide load balancing for AWS service requests

**Selection rule:** The platform presents four radio-button choices, so this question accepts one answer.

**Selected answer:** A. Traffic remains within the AWS network, improving security and potentially reducing NAT gateway costs. Correctness remains unconfirmed until the assessment provides feedback.

**Platform feedback:** Pending; no correctness feedback has been observed.

**Learning note:** Interface and gateway VPC endpoints provide private paths to supported AWS services. They can keep service traffic off public internet routes and reduce reliance on NAT for those destinations.



### Question 20 of 60

**Question:** Which core pillar of ECS focuses on eliminating complex infrastructure management?

**Choices:**

- A. Enhancing security
- B. Simplifying container management at scale
- C. Driving high performance availability
- D. Reducing total cost of ownership

**Selection rule:** The platform presents four radio-button choices, so this question accepts one answer.

**Selected answer:** B. Simplifying container management at scale. Correctness remains unconfirmed until the assessment provides feedback.

**Platform feedback:** Pending; no correctness feedback has been observed.

**Learning note:** Amazon ECS is a managed container orchestration service that reduces the operational work needed to deploy and manage container workloads at scale.



### Question 21 of 60

**Question:** How should you evaluate the trade-offs when selecting between ECS and CodeDeploy controllers?

**Choices:**

- A. Choose based solely on the fastest deployment speed capabilities
- B. Prioritize the newest controller features over operational requirements
- C. Select the controller with the most configuration options available
- D. Balance simplicity and setup requirements against advanced features and monitoring needs

**Selection rule:** The platform presents four radio-button choices, so this question accepts one answer.

**Selected answer:** D. Balance simplicity and setup requirements against advanced features and monitoring needs. Correctness remains unconfirmed until the assessment provides feedback.

**Platform feedback:** Pending; no correctness feedback has been observed.

**Learning note:** The ECS deployment controller supports standard rolling updates with simpler setup. The CodeDeploy controller supports blue/green deployments and traffic shifting, with additional setup and operational controls.



### Question 22 of 60

**Question:** What is the security benefit of using Secrets Manager over hard-coding passwords?

**Choices:**

- A. Passwords are backed up automatically to S3
- B. Passwords are cached locally for faster access
- C. Passwords are automatically encrypted during transmission
- D. Passwords are stored securely outside the task definition

**Selection rule:** The platform presents four radio-button choices, so this question accepts one answer.

**Selected answer:** D. Passwords are stored securely outside the task definition. Correctness remains unconfirmed until the assessment provides feedback.

**Platform feedback:** Pending; no correctness feedback has been observed.

**Learning note:** Referencing Secrets Manager lets ECS inject or retrieve secrets at task startup without embedding secret values in the task definition. Access is governed by IAM and the secret can be rotated.



### Question 23 of 60

**Question:** Which AWS service provides out-of-the-box system metrics for ECS Fargate and EC2?

**Choices:**

- A. AWS SDK
- B. CloudWatch
- C. Container Insights
- D. EventBridge

**Selection rule:** The platform presents four radio-button choices, so this question accepts one answer.

**Selected answer:** C. Container Insights. Correctness remains unconfirmed until the assessment provides feedback.

**Platform feedback:** Pending; no correctness feedback has been observed.

**Learning note:** CloudWatch Container Insights provides curated ECS metrics for clusters, services, tasks, and containers. CloudWatch is the broader monitoring service in which those metrics are published.



### Question 24 of 60

**Question:** What network component allows ECS tasks in private subnets to access the internet?

**Choices:**

- A. NAT gateway
- B. Internet gateway
- C. Route table
- D. VPC endpoint

**Selection rule:** The platform presents four radio-button choices, so this question accepts one answer.

**Selected answer:** A. NAT gateway. Correctness remains unconfirmed until the assessment provides feedback.

**Platform feedback:** Pending; no correctness feedback has been observed.

**Learning note:** A NAT gateway in a public subnet allows resources in private subnets to initiate outbound internet connections without accepting unsolicited inbound internet connections.



### Question 25 of 60

**Question:** What is the fundamental security isolation model that AWS Fargate implements?

**Choices:**

- A. Tasks are isolated using enhanced security groups and network access control lists
- B. Multiple tasks from the same customer share instances but use container-level isolation
- C. Container isolation relies primarily on cgroups, namespaces, and seccomp policies
- D. Each task runs on a dedicated EC2 instance with no other tasks sharing the same instance

**Selection rule:** The platform presents four radio-button choices, so this question accepts one answer.

**Selected answer:** D. Each task runs on a dedicated EC2 instance with no other tasks sharing the same instance. Correctness remains unconfirmed until the assessment provides feedback.

**Platform feedback:** Pending; no correctness feedback has been observed.

**Learning note:** Fargate provides isolation at the task boundary on dedicated underlying infrastructure, so another customer's task does not share that task's kernel. The EC2 host is abstracted from the customer; the option's “dedicated EC2 instance” wording is a simplified description of that isolation.



### Question 26 of 60

**Question:** What is the primary role of each observability pillar when investigating system issues?

**Choices:**

- A. Events show something is happening, traces explain what is happening, logs show system performance over time
- B. Logs show something is happening, metrics explain what is happening, traces provide platform context
- C. Traces show something is happening, events explain what is happening, metrics show request flow patterns
- D. Metrics show something is happening, logs explain what is happening, traces show how requests flow through the system

**Selection rule:** The platform presents four radio-button choices, so this question accepts one answer.

**Selected answer:** D. Metrics show something is happening, logs explain what is happening, traces show how requests flow through the system. Correctness remains unconfirmed until the assessment provides feedback.

**Platform feedback:** Pending; no correctness feedback has been observed.

**Learning note:** Metrics provide aggregate measurements over time, logs provide detailed event records, and distributed traces connect spans across components to show a request's path.



### Question 27 of 60

**Question:** Which scanning option adds additional cost when configured for ECR repositories?

**Choices:**

- A. Basic scanning with improved features
- B. Wildcard matching for repository names
- C. Scan on push for selected repositories
- D. Continuous scanning for all repositories

**Selection rule:** The platform presents four radio-button choices, so this question accepts one answer.

**Selected answer:** D. Continuous scanning for all repositories. Correctness remains unconfirmed until the assessment provides feedback.

**Platform feedback:** Pending; no correctness feedback has been observed.

**Learning note:** Enhanced ECR image scanning integrates with Amazon Inspector for vulnerability findings and continuous rescanning, which has a separate charge; basic scanning is included with ECR.



### Question 28 of 60

**Question:** What problem does software version consistency solve in ECS deployments?

**Choices:**

- A. Prevents tasks from using different container image versions when images are updated during deployment
- B. Synchronizes task startup timing to prevent resource conflicts between old and new tasks
- C. Ensures all tasks use the latest available container image regardless of deployment timing
- D. Automatically rolls back deployments when container image tags are modified externally

**Selection rule:** The platform presents four radio-button choices, so this question accepts one answer.

**Selected answer:** A. Prevents tasks from using different container image versions when images are updated during deployment. Correctness remains unconfirmed until the assessment provides feedback.

**Platform feedback:** Pending; no correctness feedback has been observed.

**Learning note:** Using immutable image digests or versioned tags makes deployments reproducible. Mutable tags can point at a new image while tasks are being replaced, resulting in mixed versions.



### Question 29 of 60

**Question:** Which combination of AWS managed services provides Prometheus and Grafana functionality without infrastructure management?

**Choices:**

- A. AWS X-Ray and CloudWatch Insights
- B. Amazon Managed Prometheus (AMP) and Amazon Managed Grafana (AMG)
- C. ECS Container Insights and CloudFormation
- D. CloudWatch Metrics and CloudWatch Dashboards

**Selection rule:** The platform presents four radio-button choices, so this question accepts one answer.

**Selected answer:** B. Amazon Managed Prometheus (AMP) and Amazon Managed Grafana (AMG). Correctness remains unconfirmed until the assessment provides feedback.

**Platform feedback:** Pending; no correctness feedback has been observed.

**Learning note:** Amazon Managed Service for Prometheus provides managed Prometheus-compatible metrics, while Amazon Managed Grafana provides managed Grafana workspaces without requiring customers to operate those servers.



### Question 30 of 60

**Question:** What networking configuration must be specified when running a service with AWS VPC mode?

**Choices:**

- A. Only the VPC ID and security groups
- B. Only the internet gateway and NAT gateway settings
- C. Only the availability zones and route tables
- D. Subnets where tasks will run and optionally security groups and public IP assignment

**Selection rule:** The platform presents four radio-button choices, so this question accepts one answer.

**Selected answer:** D. Subnets where tasks will run and optionally security groups and public IP assignment. Correctness remains unconfirmed until the assessment provides feedback.

**Platform feedback:** Pending; no correctness feedback has been observed.

**Learning note:** For the `awsvpc` network mode, the service's network configuration names the subnets and may specify security groups and public IP assignment for tasks.



### Question 31 of 60

**Question:** Which health check configuration takes precedence when both are present in an ECS deployment?

**Choices:**

- A. Load balancer health check settings
- B. Docker health checks embedded in the container image
- C. Auto Scaling group health check configurations
- D. Health check parameters defined in the ECS task definition container definition

**Selection rule:** The platform presents four radio-button choices, so this question accepts one answer.

**Selected answer:** D. Health check parameters defined in the ECS task definition container definition. Correctness remains unconfirmed until the assessment provides feedback.

**Platform feedback:** Pending; no correctness feedback has been observed.

**Learning note:** An ECS task definition health check overrides the image's Dockerfile health check. Load-balancer health checks are separate and are used for routing and service replacement decisions.



### Question 32 of 60

**Question:** What migration flexibility exists between ECS deployment controllers in production environments?

**Choices:**

- A. Migration requires complete application redeployment and downtime
- B. You can migrate from ECS controller to CodeDeploy controller when advanced features are needed
- C. Only external controllers can be migrated to other deployment options
- D. Controllers are permanently locked once selected and cannot be changed

**Selection rule:** The platform presents four radio-button choices, so this question accepts one answer.

**Selected answer:** B. You can migrate from ECS controller to CodeDeploy controller when advanced features are needed. Correctness remains unconfirmed until the assessment provides feedback.

**Platform feedback:** Pending; no correctness feedback has been observed.

**Learning note:** An ECS service can be moved toward CodeDeploy-controlled deployments when blue/green features are needed. Plan and validate the migration against the service's task definitions, load balancers, and deployment configuration.



### Question 33 of 60

**Question:** Which load balancer type is most appropriate for routing HTTP traffic with path-based routing requirements?

**Choices:**

- A. Application Load Balancer (ALB)
- B. Classic Load Balancer (CLB)
- C. Gateway Load Balancer (GLB)
- D. Network Load Balancer (NLB)

**Selection rule:** The platform presents four radio-button choices, so this question accepts one answer.

**Selected answer:** A. Application Load Balancer (ALB). Correctness remains unconfirmed until the assessment provides feedback.

**Platform feedback:** Pending; no correctness feedback has been observed.

**Learning note:** An Application Load Balancer operates at the HTTP/HTTPS application layer and supports host- and path-based routing to target groups.



### Question 34 of 60

**Question:** Where do you configure data in transit encryption for Amazon EFS in ECS?

**Choices:**

- A. Using IAM policies attached to the ECS service
- B. Within the ECS task definition
- C. Through the ECS cluster security group rules
- D. In the EFS file system configuration settings

**Selection rule:** The platform presents four radio-button choices, so this question accepts one answer.

**Selected answer:** B. Within the ECS task definition. Correctness remains unconfirmed until the assessment provides feedback.

**Platform feedback:** Pending; no correctness feedback has been observed.

**Learning note:** For an ECS EFS volume, the task definition's EFS volume configuration controls in-transit encryption (and can specify an EFS access point). EFS file-system encryption settings govern encryption at rest.



### Question 35 of 60

**Question:** In the public-facing web application pattern, where should ECS tasks be placed for optimal security?

**Choices:**

- A. In the same subnet as the load balancer for better performance
- B. In a separate VPC connected via VPC peering
- C. In public subnets alongside the load balancer
- D. In private subnets behind the load balancer

**Selection rule:** The platform presents four radio-button choices, so this question accepts one answer.

**Selected answer:** D. In private subnets behind the load balancer. Correctness remains unconfirmed until the assessment provides feedback.

**Platform feedback:** Pending; no correctness feedback has been observed.

**Learning note:** Place the internet-facing ALB in public subnets and ECS tasks in private subnets. The load balancer forwards only allowed application traffic to tasks, reducing direct internet exposure.



### Question 36 of 60

**Question:** What target type should be configured when using AWS VPC networking mode with ECS?

**Choices:**

- A. Lambda
- B. IP
- C. Instance
- D. Application

**Selection rule:** The platform presents four radio-button choices, so this question accepts one answer.

**Selected answer:** B. IP. Correctness remains unconfirmed until the assessment provides feedback.

**Platform feedback:** Pending; no correctness feedback has been observed.

**Learning note:** With `awsvpc` networking, each task has its own ENI and IP address, so an ALB or NLB target group must use the `ip` target type rather than instance IDs.



### Question 37 of 60

**Question:** Which IAM role type controls an ECS application's access to AWS services like DynamoDB?

**Choices:**

- A. Task execution role
- B. Task role
- C. Service role
- D. Instance role

**Selection rule:** The platform presents four radio-button choices, so this question accepts one answer.

**Selected answer:** B. Task role. Correctness remains unconfirmed until the assessment provides feedback.

**Platform feedback:** Pending; no correctness feedback has been observed.

**Learning note:** The task role provides AWS credentials to the application containers, so application calls to services such as DynamoDB use its permissions. The execution role is for ECS agent actions such as image pulls and log delivery.



### Question 38 of 60

**Question:** What information is required to create an ECS service using Fargate?

**Choices:**

- A. Container image URL and security group configurations
- B. Cluster name, service name, task definition name, and networking configuration
- C. Load balancer ARN and auto-scaling policies
- D. Only the cluster name and desired number of tasks

**Selection rule:** The platform presents four radio-button choices, so this question accepts one answer.

**Selected answer:** B. Cluster name, service name, task definition name, and networking configuration. Correctness remains unconfirmed until the assessment provides feedback.

**Platform feedback:** Pending; no correctness feedback has been observed.

**Learning note:** Creating a Fargate service requires a cluster and service identity, a task definition, and network configuration (including subnets and security groups); desired count and optional load balancing can be configured as well.



### Question 39 of 60

**Question:** What problem can occur when using average response time as an auto scaling metric?

**Choices:**

- A. Adding more tasks may overwhelm downstream dependencies and worsen the problem
- B. Response time only measures successful requests
- C. Response time metrics are too slow to trigger scaling events
- D. Average calculations require complex mathematical processing

**Selection rule:** The platform presents four radio-button choices, so this question accepts one answer.

**Selected answer:** A. Adding more tasks may overwhelm downstream dependencies and worsen the problem. Correctness remains unconfirmed until the assessment provides feedback.

**Platform feedback:** Pending; no correctness feedback has been observed.

**Learning note:** Scaling directly on latency can create a feedback loop: adding tasks increases request volume to a constrained dependency, which can worsen latency. Choose metrics and scaling policies that reflect the actual bottleneck and dependency capacity.



### Question 40 of 60

**Question:** Which cost optimization strategy helps prevent logging budgets from exploding?

**Choices:**

- A. Storing all log types with the same retention period
- B. Sending identical logs to multiple destinations for redundancy
- C. Logging everything at debug level for complete visibility
- D. Setting appropriate retention policies and using sampling for high volume applications

**Selection rule:** The platform presents four radio-button choices, so this question accepts one answer.

**Selected answer:** D. Setting appropriate retention policies and using sampling for high volume applications. Correctness remains unconfirmed until the assessment provides feedback.

**Platform feedback:** Pending; no correctness feedback has been observed.

**Learning note:** Choose retention periods by log use and compliance needs, and sample or filter high-volume events to control ingestion and storage costs while preserving useful signals.



### Question 41 of 60

**Question:** Which port does the X-Ray Daemon listen on by default in ECS implementations?

**Choices:**

- A. Port 3000
- B. Port 443
- C. Port 2000
- D. Port 8080

**Selection rule:** The platform presents four radio-button choices, so this question accepts one answer.

**Selected answer:** C. Port 2000. Correctness remains unconfirmed until the assessment provides feedback.

**Platform feedback:** Pending; no correctness feedback has been observed.

**Learning note:** The AWS X-Ray daemon listens for UDP trace segments on port 2000 by default; ECS tasks must be configured to send traces to the daemon.



### Question 42 of 60

**Question:** What is the primary focus of this Amazon ECS deployment module?

**Choices:**

- A. Deploying containerized applications to Amazon ECS using a real-world retail application scenario
- B. Learning the theoretical concepts and fundamentals of Amazon ECS architecture
- C. Comparing different container orchestration services available on AWS
- D. Setting up AWS account permissions and initial configuration for ECS

**Selection rule:** The platform presents four radio-button choices, so this question accepts one answer.

**Selected answer:** A. Deploying containerized applications to Amazon ECS using a real-world retail application scenario. Correctness remains unconfirmed until the assessment provides feedback.

**Platform feedback:** Pending; no correctness feedback has been observed.

**Learning note:** The module centers on a practical application deployment scenario on ECS, complementing the path's theory and architecture courses.



### Question 43 of 60

**Question:** Which scenarios would benefit from creating multiple EC2 Capacity Providers?

**Choices:**

- A. Different availability zones, instance types, or workload priorities
- B. Different container image versions or application environments only
- C. Different networking configurations or security group settings only
- D. Different AWS regions or cross-account deployments only

**Selection rule:** The platform presents four radio-button choices, so this question accepts one answer.

**Selected answer:** A. Different availability zones, instance types, or workload priorities. Correctness remains unconfirmed until the assessment provides feedback.

**Platform feedback:** Pending; no correctness feedback has been observed.

**Learning note:** Separate capacity providers can represent distinct Auto Scaling groups and instance fleets, allowing placement and scaling strategies to match availability, compute type, and workload priorities.



### Question 44 of 60

**Question:** What is the appropriate configuration for processing 8 data files simultaneously as a one-time job?

**Choices:**

- A. Configure a daemon service across 8 container instances
- B. Configure a service with desired count of 8 tasks
- C. Launch 8 standalone tasks in parallel with a single API call
- D. Configure 8 separate scheduled tasks to run once

**Selection rule:** The platform presents four radio-button choices, so this question accepts one answer.

**Selected answer:** C. Launch 8 standalone tasks in parallel with a single API call. Correctness remains unconfirmed until the assessment provides feedback.

**Platform feedback:** Pending; no correctness feedback has been observed.

**Learning note:** Standalone ECS tasks suit finite one-time jobs. A `RunTask` request can launch multiple tasks, while a service is intended to keep a desired number of tasks running.



### Question 45 of 60

**Question:** What is the key difference between ECS standalone tasks and services?

**Choices:**

- A. Standalone tasks can integrate with load balancers while services cannot
- B. Standalone tasks automatically replace failed instances while services do not
- C. Services maintain a specified number of running tasks continuously while standalone tasks are one-time executions
- D. Services are used for batch processing while standalone tasks are for long-running applications

**Selection rule:** The platform presents four radio-button choices, so this question accepts one answer.

**Selected answer:** C. Services maintain a specified number of running tasks continuously while standalone tasks are one-time executions. Correctness remains unconfirmed until the assessment provides feedback.

**Platform feedback:** Pending; no correctness feedback has been observed.

**Learning note:** An ECS service maintains a desired number of healthy tasks over time. A standalone task is launched directly for finite work and is not continuously reconciled by a service.



### Question 46 of 60

**Question:** Why must container images be copied to a private ECR repository for private subnet deployment?

**Choices:**

- A. Private ECR repositories provide enhanced security features
- B. Public ECR repositories are not compatible with VPC endpoints
- C. Public ECR repositories require internet access which private subnets lack
- D. Private ECR repositories have better performance than public ones

**Selection rule:** The platform presents four radio-button choices, so this question accepts one answer.

**Selected answer:** C. Public ECR repositories require internet access which private subnets lack. Correctness remains unconfirmed until the assessment provides feedback.

**Platform feedback:** Pending; no correctness feedback has been observed.

**Learning note:** For a private subnet without a NAT or other internet route, a private ECR repository can be reached through ECR interface endpoints and an S3 gateway endpoint for layers. The need depends on the subnet's actual egress configuration.



### Question 47 of 60

**Question:** What must be configured to allow HTTP communication to ECS tasks?

**Choices:**

- A. Internet Gateway with HTTP routing
- B. VPC endpoint for HTTP traffic
- C. Security group with HTTP port access
- D. Network Access Control List with HTTPS rules

**Selection rule:** The platform presents four radio-button choices, so this question accepts one answer.

**Selected answer:** C. Security group with HTTP port access. Correctness remains unconfirmed until the assessment provides feedback.

**Platform feedback:** Pending; no correctness feedback has been observed.

**Learning note:** The task's security group must allow inbound traffic on the application's HTTP port from the intended client or load balancer security group. Route tables and subnet paths must also support the connection.



### Question 48 of 60

**Question:** Which ECS feature helps microservices communicate with each other?

**Choices:**

- A. Task Connect
- B. VPC Connect
- C. Service Connect
- D. Container Connect

**Selection rule:** The platform presents four radio-button choices, so this question accepts one answer.

**Selected answer:** C. Service Connect. Correctness remains unconfirmed until the assessment provides feedback.

**Platform feedback:** Pending; no correctness feedback has been observed.

**Learning note:** Amazon ECS Service Connect provides service discovery and managed connectivity between services. Its proxy can supply load balancing, health-based routing, and metrics without requiring application code changes.



### Question 49 of 60

**Question:** What is the primary security advantage of using multi-stage builds in Docker?

**Choices:**

- A. Running each stage with different user permissions to prevent privilege escalation
- B. Automatically scanning each stage for vulnerabilities during the build process
- C. Selectively copying artifacts while leaving behind build tools and unnecessary binaries
- D. Encrypting sensitive data between stages to protect against data exposure

**Selection rule:** The platform presents four radio-button choices, so this question accepts one answer.

**Selected answer:** C. Selectively copying artifacts while leaving behind build tools and unnecessary binaries. Correctness remains unconfirmed until the assessment provides feedback.

**Platform feedback:** Pending; no correctness feedback has been observed.

**Learning note:** A multi-stage Docker build copies only final artifacts into the runtime image, leaving compilers and build dependencies behind. This reduces image size and the set of components that need patching.



### Question 50 of 60

**Question:** What is required for Fargate tasks but optional for EC2 tasks in task definitions?

**Choices:**

- A. CPU and memory settings
- B. IAM role permissions
- C. Network mode configuration
- D. Container name and image specifications

**Selection rule:** The platform presents four radio-button choices, so this question accepts one answer.

**Selected answer:** A. CPU and memory settings. Correctness remains unconfirmed until the assessment provides feedback.

**Platform feedback:** Pending; no correctness feedback has been observed.

**Learning note:** Fargate requires valid task-level CPU and memory values from its supported combinations. ECS on EC2 can schedule task definitions without task-level CPU or memory, though resource reservations and limits still guide placement and runtime use.



### Question 51 of 60

**Question:** What are the essential prerequisites needed before deploying applications to Amazon ECS?

**Choices:**

- A. VPC setup, IAM roles, and ECR container management
- B. Task definitions, services, and auto scaling
- C. Route 53, API Gateway, and Lambda functions
- D. CloudWatch logs, health checks, and load balancers

**Selection rule:** The platform presents four radio-button choices, so this question accepts one answer.

**Selected answer:** A. VPC setup, IAM roles, and ECR container management. Correctness remains unconfirmed until the assessment provides feedback.

**Platform feedback:** Pending; no correctness feedback has been observed.

**Learning note:** Deployment prerequisites include a network, appropriate IAM roles and policies, and accessible container images in a registry such as ECR. Task definitions and services are ECS deployment resources rather than infrastructure prerequisites.



### Question 52 of 60

**Question:** Where will the UI Service be deployed in this module?

**Choices:**

- A. Amazon EC2 instances
- B. Amazon EKS Cluster
- C. AWS Lambda
- D. Amazon ECS Cluster

**Selection rule:** The platform presents four radio-button choices, so this question accepts one answer.

**Selected answer:** D. Amazon ECS Cluster. Correctness remains unconfirmed until the assessment provides feedback.

**Platform feedback:** Pending; no correctness feedback has been observed.

**Learning note:** This module's UI service is deployed as a workload in an Amazon ECS cluster.



### Question 53 of 60

**Question:** What scaling limitation currently exists with predictive scaling in ECS?

**Choices:**

- A. It only works with CPU metrics
- B. It only handles scaling out, not scaling in
- C. It requires manual threshold configuration
- D. It cannot be combined with other policies

**Selection rule:** The platform presents four radio-button choices, so this question accepts one answer.

**Selected answer:** B. It only handles scaling out, not scaling in. Correctness remains unconfirmed until the assessment provides feedback.

**Platform feedback:** Pending; no correctness feedback has been observed.

**Learning note:** The assessment's stated limitation is that predictive scaling can scale out but does not scale in. Treat this as assessment content until feedback confirms it.



### Question 54 of 60

**Question:** What deployment challenge does workload portability address for modern development teams?

**Choices:**

- A. Managing deployments across multiple environments and growing numbers of microservice applications
- B. Eliminating the need for testing environments in the development lifecycle
- C. Preventing unauthorized access to production deployment systems
- D. Reducing the number of programming languages used in development

**Selection rule:** The platform presents four radio-button choices, so this question accepts one answer.

**Selected answer:** A. Managing deployments across multiple environments and growing numbers of microservice applications. Correctness remains unconfirmed until the assessment provides feedback.

**Platform feedback:** Pending; no correctness feedback has been observed.

**Learning note:** Containerized workloads package application dependencies consistently, helping teams deploy the same workload across development, test, and production environments and across growing microservice estates.
### Question 55 of 60

**Question:** What is the primary purpose of a Dockerfile in container development?

**Choices:**

- A. To store application source code and dependencies
- B. To manage network connections between containers
- C. To define how to build and run a containerized application
- D. To provide runtime monitoring for container performance

**Selection rule:** The platform presents four radio-button choices, so this question accepts one answer.

**Selected answer:** C. To define how to build and run a containerized application. Correctness remains unconfirmed until the assessment provides feedback.

**Platform feedback:** Pending; no correctness feedback has been observed.

**Learning note:** A Dockerfile declares the instructions used to build a container image, including its base image, copied files, commands, and default runtime behavior.

### Question 56 of 60

**Question:** What AWS service distributes incoming customer traffic across multiple ECS tasks?

**Choices:**

- A. Application Load Balancer
- B. API Gateway
- C. CloudFront distribution
- D. Route 53 resolver

**Selection rule:** The platform presents four radio-button choices, so this question accepts one answer.

**Selected answer:** A. Application Load Balancer. Correctness remains unconfirmed until the assessment provides feedback.

**Platform feedback:** Pending; no correctness feedback has been observed.

**Learning note:** An Application Load Balancer can route incoming requests to healthy ECS task targets and distribute traffic among them.

### Question 57 of 60

**Question:** What routing capability does Service Connect provide to improve application reliability?

**Choices:**

- A. Geographic routing that directs traffic to the nearest available region
- B. Priority-based routing that favors services with higher resource allocations
- C. Health-aware routing that only sends requests to healthy service instances
- D. Round-robin routing that cycles through all registered service endpoints

**Selection rule:** The platform presents four radio-button choices, so this question accepts one answer.

**Selected answer:** C. Health-aware routing that only sends requests to healthy service instances. Correctness remains unconfirmed until the assessment provides feedback.

**Platform feedback:** Pending; no correctness feedback has been observed.

**Learning note:** Service Connect uses service discovery and managed proxy behavior to route communication between services; the answer here is the assessment's health-aware routing choice and remains unverified until feedback appears.

### Question 58 of 60

**Question:** How much advance notice do you receive before a spot instance is reclaimed?

**Choices:**

- A. Five minutes
- B. Thirty seconds
- C. Two minutes
- D. One minute

**Selection rule:** The platform presents four radio-button choices, so this question accepts one answer.

**Selected answer:** C. Two minutes. Correctness remains unconfirmed until the assessment provides feedback.

**Platform feedback:** Pending; no correctness feedback has been observed.

**Learning note:** EC2 Spot interruption notices generally provide about two minutes before the instance is interrupted, giving workloads a short window to drain or checkpoint work.

### Question 59 of 60

**Question:** What is the primary purpose of an ECS task definition?

**Choices:**

- A. It serves as a blueprint that defines how containerized applications run
- B. It automatically scales container instances based on demand
- C. It monitors the health status of running containers
- D. It manages network traffic routing between containers

**Selection rule:** The platform presents four radio-button choices, so this question accepts one answer.

**Selected answer:** A. It serves as a blueprint that defines how containerized applications run. Correctness remains unconfirmed until the assessment provides feedback.

**Platform feedback:** Pending; no correctness feedback has been observed.

**Learning note:** A task definition is the reusable blueprint for ECS tasks, including container images, resource settings, roles, networking, storage, and logging configuration.

### Question 60 of 60

**Question:** What is the primary benefit of the overlay file system used by containers?

**Choices:**

- A. Container images automatically inherit security patches from base layers
- B. Each application gets isolated storage that cannot be accessed by other containers
- C. Layers can be reused across multiple container images for efficient storage and distribution
- D. Applications run faster because file access is distributed across multiple layers

**Selection rule:** The platform presents four radio-button choices, so this question accepts one answer.

**Selected answer:** C. Layers can be reused across multiple container images for efficient storage and distribution. Correctness remains unconfirmed until the assessment provides feedback.

**Platform feedback:** Pending; no correctness feedback has been observed.

**Learning note:** Container image layers can be shared and cached, reducing duplicate storage and repeated transfer when images reuse common layers.
