---
title: DevOps on AWS
document_type: lesson
source: AWS Skill Builder
source_url: https://skillbuilder.aws/learn/XNP64SN2AX/aws-partner-devops-essentials/4BXN5YQESG
course: AWS Partner: DevOps Essentials
lesson_order: 3
---
# DevOps on AWS

## Outline items

- Quick Reference: AWS DevOps Services
- Common Use Cases
- Knowledge Check

## Quick Reference: AWS DevOps Services — lesson 7 of 14

The lesson introduces AWS service mapping as a way to connect customer needs with targeted DevOps solutions. Its reference table lists:

| Category | AWS service |
|---|---|
| CI/CD | AWS CodeCommit, AWS CodeBuild, AWS CodePipeline, AWS CodeDeploy |
| AI-powered development | Kiro |
| AI operations | AWS DevOps Agent |
| Modernization | AWS Transform |

The explanatory text assigns CodeCommit to source control, CodeBuild to compilation and testing, CodePipeline to workflow orchestration, and CodeDeploy to automated application deployment. It further describes Kiro as providing enhanced observability and monitoring, AWS DevOps Agent as intelligent automation and assistance, and AWS Transform as modernizing and optimizing DevOps practices. This Kiro description is recorded as the lesson states it.

The service map is shown as a two-column table on a pale blue-gray panel, with a solid blue header row labeled Category and AWS Service. The four category rows have thin grid lines; no accompanying video or decorative illustration is visible. The customer scenarios appear as vertically stacked white accordion cards with fine gray separators, plus/minus controls, and a blue accent strip at the left edge of the expanded panel.

### Connecting customer needs to AWS services

Three expandable examples are listed: **Automating Software Releases**, **Building and Testing Code**, and **Deploying Applications Safely**. Their details remain to be expanded.

The lesson links to the [AWS DevOps Agent user guide](https://docs.aws.amazon.com/devopsagent/latest/userguide/about-aws-devops-agent.html). It advises first understanding the customer’s specific needs, then mapping requirements to services such as CodePipeline for release automation, CodeBuild for testing, or CodeDeploy for deployment management, rather than proposing unnecessary complexity.

### CloudFormation pipeline example

The lesson asks learners to save the sample as `devops-pipeline.yaml` and create a CloudFormation stack through the console, or run:

```sh
aws cloudformation create-stack --template-body file://devops-pipeline.yaml --capabilities CAPABILITY_IAM
```

The accessible code block defines this pipeline:

```yaml
AWSTemplateFormatVersion: '2010-09-09'
Description: 'DevOps pipeline connecting common customer needs to AWS services'

Resources:
  Pipeline:
    Type: AWS::CodePipeline::Pipeline
    Properties:
      RoleArn: !GetAtt PipelineRole.Arn
      ArtifactStore:
        Type: S3
        Location: !Ref ArtifactBucket
      Stages:
        - Name: Source
          Actions:
            - Name: Source
              ActionTypeId:
                Category: Source
                Owner: AWS
                Provider: CodeCommit
                Version: '1'
              Configuration:
                RepositoryName: my-app
                BranchName: main
              OutputArtifacts:
                - Name: SourceCode

        - Name: Build
          Actions:
            - Name: BuildAndTest
              ActionTypeId:
                Category: Build
                Owner: AWS
                Provider: CodeBuild
                Version: '1'
              Configuration:
                ProjectName: !Ref BuildProject
              InputArtifacts:
                - Name: SourceCode
              OutputArtifacts:
                - Name: BuildOutput

        - Name: Deploy
          Actions:
            - Name: Deploy
              ActionTypeId:
                Category: Deploy
                Owner: AWS
                Provider: CodeDeploy
                Version: '1'
              Configuration:
                ApplicationName: my-app
                DeploymentGroupName: prod
              InputArtifacts:
                - Name: BuildOutput
```

The accessible sample ends after the deploy stage’s `InputArtifacts`; any remaining template content is unverified. `PipelineRole`, `ArtifactBucket`, and `BuildProject` are referenced in the visible code but are not defined in this exposed portion. The stack has not been deployed.
#### Building and Testing Code — CodeBuild

The expanded scenario recommends AWS CodeBuild when customers want standardized builds and tests or want to stop maintaining build servers. CodeBuild is fully managed: it compiles code, runs tests, and produces deployable packages. It is useful for parallel builds and tests or when customers want to avoid managing build infrastructure. One example automatically compiles an application and runs unit tests whenever new code is committed. The course says CodeBuild is unnecessary for simple build needs handled by basic scripts. It links to the [CodeBuild integration guide](https://docs.aws.amazon.com/codebuild/latest/userguide/how-to-create-pipeline.html).
#### Deploying Applications Safely — CodeDeploy

The expanded scenario recommends AWS CodeDeploy when customers need reliable deployments and quick rollbacks. It automates deployment across compute infrastructure and is useful for fleets of servers, zero-downtime deployment, and automatic rollback. One example deploys a web application across multiple EC2 instances with blue/green strategies. The course says CodeDeploy may not suit a simple single-server deployment or container applications where Amazon ECS deployments may fit better. It suggests starting with a [minimum viable pipeline](https://docs.aws.amazon.com/whitepapers/latest/practicing-continuous-integration-continuous-delivery/building-the-pipeline.html) and adding more advanced patterns as needed.
#### Automating Software Releases — CodePipeline

The expanded scenario recommends AWS CodePipeline when customers need automated releases or standardized movement from development to production. CodePipeline orchestrates source control, build, test, and deployment stages. A customer can automate code from an S3 bucket or CodeCommit repository through testing into production. The lesson cautions that CodePipeline may be too much for simple projects with little automation; start with basic CI/CD tools and graduate to CodePipeline as complexity grows. It links to [CodePipeline use cases and best practices](https://docs.aws.amazon.com/codepipeline/latest/userguide/best-practices.html).

#### New Service Alert — AWS DevOps Agent

A lightbulb callout describes AWS DevOps Agent as an autonomous, always-on operations agent and virtual on-call engineer. Visually, it uses a pale-blue background with a large white rounded text card and an overlapping circular green-to-purple AWS DevOps Agent logo; a “Learn more” link sits below. It detects incidents, correlates metrics, logs, traces, and recent code deployments to identify root causes, and can resolve issues without human intervention. The callout says it works across AWS, multicloud, and on-premises environments, integrating with Dynatrace, New Relic, GitHub, and GitLab. It says AWS announced the agent at re:Invent 2025 and it is generally available; early customers report 3–5x faster incident resolution than manual triage. The course frames it as a shift from reactive firefighting to proactive reliability management, with the agent learning from its environment to prevent incidents.
### Key Technical Capabilities at a Glance

The lesson says AWS provides an integrated suite of fully managed DevOps services, letting teams focus on delivery instead of assembling tools or maintaining infrastructure. It lists five advantages:

1. **Fully managed services:** Source-control services such as CodeCommit through deployment automation with CodePipeline require no customer-managed infrastructure, reducing operational overhead and supporting availability. The card links to the [CodeCommit user guide](https://docs.aws.amazon.com/codecommit/latest/userguide/welcome.html).
2. **Native integration:** CodeBuild integrates with CodePipeline; CodeDeploy works with EC2, Lambda, and ECS.
3. **Multiple deployment strategies:** Blue/green supports zero downtime; canary releases enable gradual rollouts. Built-in rollback capabilities allow a strategy suited to each application.
4. **Pay-as-you-go pricing:** No upfront cost or long-term commitment; partners can start small and scale for customers of different sizes.
5. **Security by design:** IAM supports fine-grained access control; services include encryption at rest and in transit, audit logging, and compliance certifications. The card links to the [IAM user guide](https://docs.aws.amazon.com/IAM/latest/UserGuide/introduction.html).

The concluding text says these capabilities help partners implement DevOps efficiently while controlling security and cost, from simple pipelines to complex multi-account strategies. No image or video is shown on this screen.
### Common Use Cases

#### Automated CI/CD Pipeline

The lesson presents automated CI/CD as a response to slow, error-prone manual deployments that can cause production problems and dissatisfied customers. Its example flow starts with a developer committing code to AWS CodeCommit. AWS CodePipeline orchestrates delivery and triggers CodeBuild to compile the application and run automated tests. When tests pass, CodeDeploy sends the application to staging for validation, then the pipeline promotes it to production. If deployment detects a problem, CodeDeploy rolls back to the last known good version to maintain availability. The lesson links to [CodeDeploy deployment configurations and rollback options](https://docs.aws.amazon.com/codedeploy/latest/userguide/deployment-configurations.html).

Four benefit tabs say changes can be deployed in minutes instead of days or weeks; consistent testing and deployment reduce human error; automation reduces manual effort for development and operations teams; and a full audit trail of changes and approvals supports compliance. The lesson summarizes the business benefits as faster deployments, fewer human errors, lower operational costs, and a compliance audit trail. More complex pipelines can add manual approval steps for critical deployments, container-service integration such as Amazon ECS, and custom actions implemented with AWS Lambda. It points to [CodePipeline's visual editor tutorial](https://docs.aws.amazon.com/codepipeline/latest/userguide/tutorials-simple-pipeline.html), which configures stages without writing code; the lesson recommends adding sophistication gradually as needs evolve.

The embedded example is titled “CI/CD pipeline for web application deployment.” It says the CloudFormation template builds and deploys a web application after developers push to CodeCommit, and instructs learners to save it as webapp-pipeline.yaml. The course supplies this deployment command: aws cloudformation create-stack --template-body file://webapp-pipeline.yaml --capabilities CAPABILITY_IAM. The visible YAML defines a RepositoryName parameter, a CodeCommit repository, a CodeBuild project using the standard 5.0 Linux image and buildspec.yml, and CodePipeline Source and Build stages. The exposed snippet ends after the Build stage's BuildOutput artifact; later template content is not visible in the accessible text. Referenced CodeBuildServiceRole, CodePipelineServiceRole, and ArtifactBucket resources are not defined in the exposed excerpt. The template was not deployed.

The accompanying AWS DevOps Agent alert repeats that the autonomous always-on agent acts as a virtual on-call engineer, detects incidents, correlates metrics, logs, traces, and recent deployments to find root causes, and may resolve issues without human intervention. It says the agent works across AWS, multicloud, and on-premises environments and integrates with Dynatrace, New Relic, GitHub, and GitLab. The course states it was announced at re:Invent 2025, is generally available, and early customers report 3–5x faster incident resolution than manual triage. It frames the change as a move from reactive firefighting to proactive reliability management, with the agent learning from the environment to help prevent incidents. The accompanying visual is described in the Quick Reference section above.

On the first viewport, the white course canvas shows the large Common Use Cases heading, a short blue underline, and the Automated CI/CD Pipeline section below it; the fixed left navigation is blue and displays 50% completion. The benefit tabs appear inline above their selected short benefit statement. No video appears in this use case. No standalone image file was exposed for export.

#### Consistent Environments with Infrastructure as Code

The lesson explains that IaC treats infrastructure configuration like software: teams define environments in version-controlled templates that can be reviewed and deployed automatically instead of relying on console clicks or ad-hoc scripts. This promotes consistency across development, testing, and production and provides an audit trail of infrastructure changes. AWS CloudFormation YAML or JSON templates act as a single source of truth; parameters can tune instance sizes or replica counts while preventing environment drift and making tests representative of production.

For teams who prefer familiar programming languages such as TypeScript or Python, AWS CDK defines infrastructure with code constructs and reusable components. The transcript cites Thomson Reuters' CDK extension library as an example of enforcing security and compliance standards across deployments, and says CDK constructs help teams share best practices. For deployment across accounts and regions, CloudFormation StackSets deploys the same stacks in one operation. The transcript suggests this for organizations with separate business unit or compliance accounts; a financial-services example uses StackSets to keep logging and security controls consistent across regional operations. It links to the [CloudFormation template format guide](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/template-formats.html), [AWS CDK Developer Guide](https://docs.aws.amazon.com/cdk/v2/guide/home.html), and [CloudFormation StackSets documentation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/what-is-cfnstacksets.html).

The example is titled “Maintain consistent environments by defining a parameterized web application stack.” It says to save the sample as webapp-environments.yaml and gives this command: aws cloudformation create-stack --template-body file://webapp-environments.yaml --parameters ParameterKey=EnvironmentType,ParameterValue=Production. The visible excerpt defines an EnvironmentType parameter restricted to Development, Staging, or Production and a mapping: Development uses t3.small with 1–2 instances, Staging uses t3.medium with 2–4, and Production uses t3.large with 3–6. It begins an Auto Scaling group whose minimum and maximum sizes come from the mapping, an EC2 launch template whose instance type also comes from the mapping, the placeholder image ID ami-0123456789abcdef0, and a security group with HTTP port 80 open to 0.0.0.0/0. The exposed sample ends during the security group definition; remaining resources and configuration are unavailable in the visible excerpt. This is a course example and was not deployed.

The accompanying video is titled “Consistent Environments with Infrastructure as Code” and is 2:13 long. A male presenter wearing a dark navy overshirt and light shirt sits in a metal-framed chair and speaks to camera in a bright modern interior with a tall leafy plant, stone-textured wall, window, and small decor on a shelf. The transcript panel contains three sections: template-based definitions with CloudFormation, code-first definitions with CDK, and multi-account deployment patterns with StackSets; their full teaching points are captured above. The player exposes captions, playback rate, picture-in-picture, fullscreen, and volume controls. No separate downloadable video or still image was exposed.

#### Proactive Monitoring and Faster Recovery

The lesson says that waiting for customer reports is no longer acceptable for fast-moving digital services; organizations need to detect and resolve issues before users are affected. Amazon CloudWatch is presented as an early-warning system that monitors applications and infrastructure continuously. Anomalies such as CPU spikes, memory constraints, or application errors can trigger Amazon SNS notifications to the operations team.

The five-step workflow infographic says: (1) CloudWatch collects metrics and logs across AWS resources in real time; (2) preconfigured alarms trigger when thresholds are breached; (3) operations teams receive immediate notifications; (4) teams use CloudWatch Dashboards to visualize system behavior and identify root causes; and (5) detailed logs help diagnose and resolve issues quickly. The diagram stacks five wide rounded bars vertically, shaded from pale gray-blue at the top to darker blue lower down, with centered bold step labels and explanatory text.

The stated business benefits are reduced Mean Time to Recovery through faster detection and diagnosis, lower operational costs from preventing major outages, improved customer satisfaction through consistent availability, and better capacity planning from historical performance data. For deeper observability, AWS X-Ray can trace requests through distributed applications alongside CloudWatch to expose performance bottlenecks. To begin, the lesson recommends focusing on critical business services, configuring the [CloudWatch agent](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/CloudWatch-Agent-getting-started.html) to collect relevant metrics, and gradually expanding monitoring as teams refine alert thresholds and response procedures. It emphasizes that monitoring should lead to meaningful reliability improvements, not just data collection.

The example, “Setup proactive monitoring with CloudWatch Alarms and Dashboard,” describes a template that creates a high-CPU CloudWatch alarm, dashboard, and SNS notification topic. It says to save the file as monitoring-stack.yaml and gives this command: aws cloudformation create-stack --stack-name monitoring-stack --template-body file://monitoring-stack.yaml --capabilities CAPABILITY_IAM. The visible YAML creates an SNS topic named high-cpu-alert, then a CloudWatch alarm for EC2 CPUUtilization averaging over 300-second periods, with two evaluation periods, two datapoints to alarm, and an 80% GreaterThanThreshold threshold. Alarm actions publish to the SNS topic; the alarm dimension uses AutoScalingGroupName set to the stack name. A CloudWatch dashboard includes a metric widget for AWS/EC2 CPUUtilization, 300-second period, Average statistic, stack-name dimension, current region, and title “CPU Usage.” The visible code excerpt ends after the widget definition. This is a course example and was not deployed.

No video is attached to this monitoring scenario. The main illustration is the five-step workflow diagram described above; no separate image file was exposed for export.

### Knowledge Check

All five multiple-choice questions were submitted and marked Correct. The course showed the selected correct answer and marked every other choice correctly unselected; no additional rationale text appeared.

1. **A retail customer wants to speed up their deployment process while maintaining consistent environments across development, staging and production. Which AWS service combination should you recommend FIRST?** A. Manual deployments using AWS Console with detailed runbooks to ensure consistency. B. Amazon EC2 Auto Scaling with custom AMIs to replicate environments and AWS Systems Manager for deployments. **C. AWS CodePipeline with CloudFormation templates to automate deployments and ensure environment consistency.** D. AWS Elastic Beanstalk with environment cloning for each stage.
2. **A development team is experiencing frequent production issues due to environment differences. Which underlying problem should you address FIRST?** A. Implement more rigorous testing procedures in the staging environment, which requires careful evaluation of the trade-offs between automation complexity and operational overhead across teams. B. Add more monitoring and alerting using Amazon CloudWatch. C. Implement blue-green deployments using AWS CodeDeploy. **D. Define infrastructure as code using AWS CloudFormation to ensure environment consistency.**
3. **A financial services customer needs to deploy the same security controls across multiple AWS accounts in different regions. What's the most efficient solution?** **A. Implement CloudFormation StackSets to deploy identical stacks across accounts and regions.** B. Use AWS Organizations to create Service Control Policies. C. Create separate CloudFormation templates for each account and region. D. Write custom scripts to deploy CloudFormation templates to each account.
4. **A team is experiencing delayed response to system issues because they only learn about problems when customers complain. How should they address this?** A. Increase the size of the operations team to handle issues faster. **B. Configure CloudWatch alarms with SNS notifications for key metrics and error conditions.** C. Create detailed troubleshooting guides for customer service representatives, while also considering the broader organizational impact and long-term sustainability of the approach. D. Implement a customer feedback portal to gather issues more quickly.
5. **A startup wants to implement CI/CD but has limited DevOps expertise. Which approach should you recommend?** A. Set up Jenkins on EC2 instances with custom deployment scripts. B. Continue with manual deployments until the team can hire experienced DevOps engineers. **C. Start with CodePipeline's visual editor to create a basic pipeline, then gradually add complexity.** D. Implement a complex multi-stage pipeline using AWS CDK.

## Progress

- Last saved step: completed the DevOps on AWS Knowledge Check; all five questions were marked correct.
- Next action: begin Partner Opportunity and Resources in Course Wrap-Up.
- Remaining sections: Course Wrap-Up, Course Conclusion, the separate assessment, Feedback review, and Achievements review.
- Access gaps: The Quick Reference pipeline excerpt ends at deploy-stage InputArtifacts; the first Common Use Cases pipeline excerpt ends after the Build stage. The IaC sample ends during security-group ingress, so remaining template content is unverified. The monitoring sample ends after its dashboard widget definition. Examples were not deployed. The AWS DevOps Agent icon is described but not saved locally. Overall course progress is 57%.








