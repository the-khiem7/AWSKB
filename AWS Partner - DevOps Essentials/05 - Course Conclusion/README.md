---
title: Course Conclusion
document_type: lesson
source: AWS Skill Builder
source_url: https://skillbuilder.aws/learn/XNP64SN2AX/aws-partner-devops-essentials/4BXN5YQESG
course: AWS Partner: DevOps Essentials
lesson_order: 5
---
# Course Conclusion

## Outline items

- Course Summary
- Contact Us

## Course Summary

### Course conclusion

The course congratulates learners on completing AWS Partner: DevOps Essentials and summarizes the outcome as a foundational understanding of Cloud Operations on AWS: key terminology, AWS services that address customer operational challenges, and partner programs and resources for delivering solutions. It asks learners to apply the material by identifying a current customer conversation where Cloud Operations is relevant, reviewing the course's downloadable resources, and exploring the recommended next course within 30 days.

### DevOps Partner Conversation Guide

The guide promises ready-to-use discovery questions, solution mappings, and objection responses for customer conversations about DevOps on AWS. Its callout says to begin with two questions—how frequently the customer deploys to production and what happens when a deployment fails—because they quickly reveal DevOps maturity.

| Ask this | Listen for |
| --- | --- |
| How often does your team deploy to production? | Infrequent releases, long cycles, or manual processes. |
| What happens when a deployment fails? | No rollback strategy, manual recovery, or extended downtime. |
| How do you manage differences between dev, staging, and production? | Environment drift, manual configuration, or inconsistent setups. |
| How long from code commit to production? | Days or weeks, or manual approval bottlenecks. |
| How do you know when something breaks in production? | Customer reports first or no proactive monitoring. |

The page has a large Course Summary title with a short blue underline, followed by a plain-text conclusion, bold section headings, and a pale-blue bordered tip callout. The discovery guide is presented as a two-column table. No video or standalone illustration is present in this portion.

### Customer Pain Point to AWS Solution

| Customer says | Recommend | Why it matters |
| --- | --- | --- |
| “Releases take weeks” | AWS CodePipeline and AWS CodeCatalyst | Fully managed CI/CD builds, tests, and deploys on every commit. |
| “Deployments are error-prone” | AWS CodeDeploy | Blue/green, canary, and rolling strategies with built-in rollback. |
| “Environments keep drifting” | AWS CloudFormation and AWS CDK | IaC makes environments identical and version-controlled. |
| “We can't see app health” | Amazon CloudWatch and AWS X-Ray | End-to-end observability from metrics to distributed tracing. |
| “Security slows us down” | AWS IAM, AWS Security Hub, and Amazon Inspector | Automated security scanning integrated into the pipeline. |

The mapping appears in a bordered three-column table with a dark blue header row and white centered labels; the five customer quotes and service mappings are in white/light cells. A wide blue CONTINUE button is beneath it. No image or video appears. Course Summary progress was 47% when this guide section loaded; overall course progress remained 86%.

### Handling Customer Objections

Four objection cards provide concise responses:

- **“We already use Jenkins/GitLab”** — AWS DevOps services integrate with existing tools. CodePipeline works alongside Jenkins, and CodeBuild can replace or complement existing build servers. Many customers use a hybrid approach during migration.
- **“Our team isn't ready for CI/CD”** — Start with a minimum viable pipeline containing one build-and-test step. CodePipeline and CodeCatalyst let teams start small and add stages as they mature; automation does not need to happen all at once.
- **“We can't afford deployment downtime”** — CodeDeploy supports blue/green and canary deployments that gradually route traffic. Automatic rollback can occur in seconds if something goes wrong.
- **“Infrastructure as Code seems complex”** — AWS CDK lets developers define infrastructure in familiar languages such as TypeScript, Python, or Java rather than YAML; CloudFormation handles provisioning.

The section ends with the guidance: frame DevOps as a business capability, not just a technical practice. Customers buy faster time to market, fewer failed deployments, and reduced operational risk. Visually, the four objections appear as stacked white bordered accordion cards with bold quoted headers and plus/minus controls; expanded cards reveal the response in plain text. No image or video appears.

### AWS DevOps Services Cheat Sheet

The cheat sheet organizes services by lifecycle phase:

- **Code and Build:** AWS CodeCommit provides managed Git repositories with IAM integration. AWS CodeBuild is a managed build service that compiles, tests, and produces artifacts without customer-managed build servers. AWS CodeArtifact is a managed artifact repository for npm, PyPI, Maven, and NuGet packages.
- **Test and Release:** AWS CodePipeline orchestrates build, test, and deploy stages for code changes and supports manual approval gates. AWS CodeDeploy automates deployments to EC2, Lambda, and ECS, including blue/green, canary, and rolling strategies with automatic rollback.
- **Infrastructure as Code:** AWS CloudFormation uses declarative JSON/YAML templates for repeatable infrastructure across accounts and regions. AWS CDK defines infrastructure in TypeScript, Python, Java, C#, or Go with reusable higher-level constructs. AWS SAM is a simplified CloudFormation experience for serverless applications using Lambda, API Gateway, and DynamoDB.
- **Monitor and Operate:** Amazon CloudWatch provides metrics, logs, traces, dashboards, and alarms. AWS X-Ray supplies distributed tracing for microservices and serverless applications to debug latency. Amazon DevOps Guru uses machine-learning anomaly detection and provides remediation recommendations.
- **Security:** AWS IAM supplies fine-grained access control for pipeline roles and deployment permissions. AWS Security Hub centralizes findings and automates compliance checks. Amazon Inspector scans EC2, containers, and Lambda for vulnerabilities.

The cheat sheet concludes that all listed services are fully managed, pay-as-you-go, and integrate natively for end-to-end CI/CD. It is a text reference with bold service names and underlined lifecycle headings on the plain white course page; no graphic or video appears in this section. Course Summary lesson progress was 82% after the service cheat sheet; the lesson was marked complete at the next transition, and overall course progress then showed 93%.

### Additional Resources

The course lists publicly available resources for continued learning:

**AWS documentation:** [Introduction to DevOps on AWS](https://docs.aws.amazon.com/whitepapers/latest/introduction-devops-aws/introduction-to-devops.html); [Practicing CI/CD on AWS](https://docs.aws.amazon.com/whitepapers/latest/practicing-continuous-integration-continuous-delivery/what-is-continuous-integration-and-continuous-deliverydeployment.html); [Building the Pipeline](https://docs.aws.amazon.com/whitepapers/latest/practicing-continuous-integration-continuous-delivery/building-the-pipeline.html); [CodePipeline Use Cases](https://docs.aws.amazon.com/codepipeline/latest/userguide/best-practices.html); and [Anti-patterns for Continuous Delivery](https://docs.aws.amazon.com/wellarchitected/latest/devops-guidance/anti-patterns-for-continuous-delivery.html).

**AWS blog posts:** [Powering Partner Success: 2026 Innovations](https://aws.amazon.com/blogs/apn/powering-partner-success-2026-innovations/) and [IaC at Thomson Reuters with AWS CDK](https://aws.amazon.com/blogs/devops/infrastructure-as-code-at-thomson-reuters-with-aws-cdk/).

**Training and partner programs:** [AWS Skill Builder](https://explore.skillbuilder.aws/), [AWS Partner Programs](https://aws.amazon.com/partners/programs/), and [AWS Training and Certification](https://aws.amazon.com/training/).

The resources are displayed as three sections of bulleted blue links on the plain white page. No illustration, video, or separate downloadable-file control appears in this section; the course's visible resources are the links and in-course guide/cheat sheet recorded above.

## Contact Us

The course invites learners to report content issues such as technical inaccuracies or typos, and technical issues encountered while taking the course; it says this feedback helps improve future course versions. The visible Contact Us button opens the support flow. For faster resolution, the page instructs learners to choose **Training** for Inquiry type, select the most relevant option for Additional details, and include the course name, a link to the course, and a detailed issue description in the “How can we help you?” field. This records the instructions only; no report was submitted.

Visually, the Contact Us page has the course's large black title with a short blue underline, a thin blue horizontal divider, explanatory copy, and a rounded blue CONTACT US button. Below it are three numbered support instructions in plain text. No image or video is shown.

## Course-level Feedback and Achievements

The course outline congratulates the learner with a trophy illustration and gives the completion date October 3, 2026. The Feedback item is still marked Incomplete. Its white card asks “Overall, how satisfied are you with your learning experience?” with five outlined star choices. The Rating definitions popover lists Very dissatisfied, Somewhat dissatisfied, Neither satisfied nor dissatisfied, Somewhat satisfied, and Very satisfied; “Save and continue” is disabled until a rating is chosen. No rating or feedback was selected or submitted. No image or video appears in this card.

The Achievements item is also marked Incomplete even though it displays a printer-friendly PDF Certificate of completion through a “View and download” link and a “Go to Credly to claim your badge” notice. The certificate row has a paper-sheet illustration with pale orange lines, a star wand, and a blue cloud-like shape. The badge row has a gray outlined shield labeled AWS DevOps Essentials and Trained Partner. The Achievements text says Credly will email instructions to claim the digital badge; the separate assessment Welcome lesson says the badge is issued in 2–3 business days. No certificate was downloaded and no badge email or Credly claim was observed. The illustrations appeared in the screenshot although the accessibility tree marked both image elements as failed to load.

## Progress

- Last saved step: completed Course Summary and Contact Us; the main course viewer displayed 100% overall progress.
- Completed the separate assessment with 20/20 correct, 100%, and Passed; full questions and answer key are in [06 - Assessment](../06%20-%20Assessment/README.md).
- Feedback and Achievements were reviewed after course completion; both remain marked Incomplete in the outline, and no rating, form, or certificate download was submitted.
- Access gaps: no standalone downloadable lesson resources were exposed. The Achievements panel offers a PDF certificate download, which was not downloaded. Public links and in-course references are recorded above. The Contact Us support flow was not opened, and no report was submitted.
