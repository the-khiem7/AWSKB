---
title: AWS Technical Essentials Module 1 Introduction to AWS
document_type: lesson
source: AWS Skill Builder
source_url: https://skillbuilder.aws/learn/K8C2FNZM6X/aws-technical-essentials/N7Q3SXQCDY
course: AWS Technical Essentials
lesson_order: 2
---

# Module 1: Introduction to Amazon Web Services

## 1. What Is AWS?

Cloud computing is on-demand delivery of IT resources over the internet, primarily with pay-as-you-go pricing. On-premises operations require organizations to host and maintain their own compute, storage, and network hardware. A cloud deployment shifts the underlying data-center operation to providers such as AWS. A hybrid deployment connects cloud resources and applications with existing non-cloud infrastructure.

Using the cloud makes it possible to replicate a production-like QA environment in minutes or seconds instead of acquiring and configuring physical hardware. This removes undifferentiated heavy lifting, allowing teams to concentrate on business-specific code and outcomes while AWS manages common infrastructure tasks.

### Six advantages of cloud computing

1. Pay only for resources used instead of funding potentially underused data-center capacity.
2. Benefit from cloud-provider economies of scale and lower pay-as-you-go prices.
3. Stop guessing capacity; scale up or down with demand.
4. Increase speed and agility by reducing resource provisioning from weeks to minutes.
5. Realize cost savings by focusing on differentiated work rather than data-center operation.
6. Deploy globally across multiple Regions quickly to reduce latency and improve customer experience.

## 2. AWS Global Infrastructure

AWS infrastructure is nested for redundancy: data centers form Availability Zones (AZs), and AZs form Regions. An AZ contains one or more data centers with redundant power, networking, and connectivity; a Region is a geographic collection of AZs connected by redundant, high-speed, low-latency links.

Region selection should first satisfy compliance requirements, then balance latency to users, regional pricing, and the availability of required services. Regions are independent: data is not replicated between them without explicit customer consent and authorization. Regional managed services provide built-in availability and durability; for AZ-scoped workloads, replicate across at least two AZs to retain availability when one fails.

Edge locations cache content near users. CloudFront uses the global edge network and AWS backbone to route requests to a low-latency edge location, reducing delivery latency.

## Progress

- Last saved step: “AWS Global Infrastructure” video transcript and readings were reviewed.
- Next action: open “Interacting with AWS.”
- Remaining sections: all subsequent Module 1 topics, Parts 1–2, and the assessment.
- Access gaps: none observed.
- Platform status: Module 1 has started; player shows 6% overall progress.
