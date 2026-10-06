---
title: "Quick Reference: AWS Cloud Operations Services"
document_type: lesson
source: AWS Skill Builder
source_url: https://skillbuilder.aws/learn/J1JFNY86AU/aws-partner-cloud-operations-essentials/732Y89ECYW
course: AWS Partner: Cloud Operations Essentials
lesson_order: 5
---

# Quick Reference: AWS Cloud Operations Services

## Match operational needs to AWS services

This lesson is a conversation aid for mapping a customer's operations challenge to AWS services. The core service combinations are CloudWatch with Systems Manager for monitoring and visibility, AWS Config for configuration and compliance, and EventBridge with Systems Manager Automation for event response. CloudWatch is presented as a fit for real-time metrics, logs, and events; Systems Manager Explorer gives teams a configurable operations view across accounts and Regions. For specialized application performance monitoring, the lesson notes that CloudWatch may not be sufficient by itself and names DevOps Guru or a third-party APM product as alternatives. AWS Health Dashboard surfaces AWS service disruptions, maintenance, and account-specific events.

For compliance, AWS Config continuously records and evaluates resource configurations. Config Rules compare resources with desired settings, and remediation actions can correct some noncompliant configurations automatically. This approach is relevant to regulated customers. Scope the recorder and rules deliberately because Config charges depend on recorded configuration items. AWS Organizations can complement Config for centralized management across accounts.

For operational event response, EventBridge detects and routes changes or issues to Systems Manager Automation runbooks. Example remediations include restarting an unresponsive instance, rotating an expired certificate, or scaling resources as utilization changes. This can reduce mean time to resolution while preserving reliability. Systems Manager Incident Manager supports structured human response and collaboration when incidents need people to coordinate.

## Technical capabilities across an AWS environment

The lesson emphasizes integrated operations rather than isolated tools. Systems Manager Explorer and CloudWatch dashboards can aggregate data across accounts and Regions, giving teams a shared operational view. Systems Manager Automation has more than 300 prebuilt automation documents for routine work and incident response. AWS Organizations and Control Tower support consistent multi-account security policies, access controls, and compliance requirements.

The reference list includes AWS Config Rules for compliance checks; Cost Explorer and Compute Optimizer for cost visibility and optimization; and CloudWatch, CloudTrail, and Amazon Managed Grafana for monitoring, logging, and visualization. Native service integrations support automated workflows, troubleshooting, and operational insights without building every integration with third-party tools.

## Visual descriptions

- The service-mapping diagram has three columns: customer needs, AWS services, and outcomes. Monitoring and operational visibility connects CloudWatch and Systems Manager to real-time resource monitoring; configuration and compliance connects AWS Config to compliance reporting; automated incident response connects EventBridge to automated issue resolution. Its legend distinguishes customer needs, primary services, supporting services, and outcomes by color.
- The integrated-capabilities diagram places Unified Dashboards and Automated Remediation on the left, Multi-Account Governance and Cost Management on the right, with arrows converging on Integrated Cloud Operations in the center. The legend separates capability groups from the central integration.
- The compliance image is a close-up of a red angular check-like piece over black outlined boxes. The cost-management image shows a calculator, currency symbols, coins, and an orange pen. The observability image shows a yellow circular “93% quality” indicator against a dark-blue monitoring interface.
- An incident-response panel contains a dark statistics dashboard with a large “Total Recovered 444,492” count, a “Total Tested” count above 2.8 million, and geographic rows beneath; it resembles a public-health recovery dashboard. A key-takeaway banner uses a dark blue network background with a robotic finger touching a node.

## Media

No video or audio element was present. The lesson uses service-mapping diagrams, feature photographs, and a dashboard illustration; visual descriptions are recorded above rather than copying the images.
