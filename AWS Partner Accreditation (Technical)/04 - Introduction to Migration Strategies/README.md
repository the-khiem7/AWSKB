---
title: Introduction to Migration Strategies
document_type: lesson
source: AWS Skill Builder
source_url: https://skillbuilder.aws/learn/8DDTPJ2RK5/aws-partner-accreditation-technical/AHX1VJYYVV
course: AWS Partner Accreditation (Technical)
lesson_order: 4
---

# Introduction to Migration Strategies

## Choosing a migration approach

A migration strategy is the approach used to move a workload to AWS. The right choice depends on the application, its technical environment, business needs, and relationships to other workloads. A portfolio can use different strategies for different applications. Before recommending one, discover the customer's existing workload inventory and architecture, then gather business drivers, stakeholders, dependencies, and application impact. Tools can support discovery, but the customer context is needed to interpret the data.

The lesson recommends asking the application owner or customer:

- Who owns or supports the application?
- Which business units rely on it?
- How important or critical is it to the business?

Once the business and technical drivers are understood, choose among the seven common migration strategies, the **7 Rs**.

## The 7 Rs

| Strategy | Meaning and common use |
|---|---|
| **Relocate** | Move a workload with minimal downtime while keeping its operating approach and technical stack intact. The video gives a VMware example: when a data-center lease is ending, moving a familiar VMware environment to AWS can be the fastest path. |
| **Rehost** | “Lift and shift”: move the application without changing its operating system or application stack. This can meet a time-sensitive need or support rapid scaling; modernization can follow after the workload is running in AWS. |
| **Replatform** | “Lift, tinker, and shift”: make selected optimizations while migrating. One example is replacing a self-managed database layer with a managed database service, reducing routine operations so teams can focus more on business logic. |
| **Repurchase** | Replace the current application with a different version or product when the alternative creates more business value. A replacement may improve access, remove infrastructure maintenance, use pay-as-you-go pricing, and reduce maintenance, infrastructure, or licensing costs. |
| **Refactor or re-architect** | Redesign or rewrite the application before or during migration to make it cloud-native. The video describes breaking a monolith into modules to make new features, performance improvements, and scaling easier. It is the most complex strategy and is not recommended as the default for a large migration; large portfolios can be moved first and modernized afterward. |
| **Retire** | Decommission an application that an inventory or audit shows is no longer needed or used. |
| **Retain** | Keep an application where it is for now and reconsider later. Licensing constraints, other blockers, a recent system upgrade, or the effort needed for a mainframe or database migration can justify deferral. |

For large migrations, the lesson highlights **rehost, replatform, relocate, and retire** as practical high-volume approaches. Because refactoring expands the change scope, it can be difficult to manage across many applications; migrating first and modernizing later can reduce that complexity. The strategies remain workload-specific, so an organization may combine them across its portfolio.

## Video coverage

The video connects migration planning to AWS CAF: assess current business and IT conditions, uncover readiness gaps, and prepare the organization. It then explains why workload discovery and application relationships matter before a recommendation is made. Strategy selection can happen during Mobilize or as part of an initial portfolio assessment. The sequence moves from gathering application and business information, to selecting a suitable strategy, then to examples of each R. The examples include an expiring VMware data-center lease for Relocate, a quick move followed by modernization for Rehost, moving a database to a managed service for Replatform, replacing an application for Repurchase, modularizing a monolith for Refactor, decommissioning unused software for Retire, and deferring constrained or recently upgraded systems for Retain. The lesson closes by emphasizing that different applications can take different paths.

The on-page transcript was expanded and used to prepare this detailed summary. It exposes no timestamps, so none are inferred. The player showed the “Migration Strategies” title over a blue-to-teal gradient with a play control; it remained paused during this notes pass. No separate lesson diagram or downloadable visual was exposed.

The seven strategy names link to the same AWS Prescriptive Guidance page about migration strategies: [AWS Prescriptive Guidance: migration strategies](https://docs.aws.amazon.com/prescriptive-guidance/latest/large-migration-guide/migration-strategies.html).

## Knowledge checks

1. **How many strategies are there for customers to choose from when migrating to AWS?** Choices shown: 2, 3, 7, 10. The earlier checkpoint recorded that feedback confirmed **seven** strategies, but did not preserve the submitted choice. In the current revisit, all radios are blank, “TAKE AGAIN” is present, and no feedback is open.
2. **Which strategy is best when replacing existing applications with different products that provide more business value?** Choices shown: Relocation, Replatform, Repurchase, Retire. The earlier checkpoint recorded **Repurchase** as the feedback-confirmed answer, without preserving the submitted choice. The current revisit shows no selected option or feedback. The checks were not retaken for this documentation pass.

## Progress

- Last saved step: rechecked the full migration lesson, expanded the video transcript, captured all seven strategies and their use cases, and recorded both knowledge-check prompts and choices.
- Next action: refresh “Introduction to the AWS Well-Architected Framework” in the parent course.
- Remaining sections: Well-Architected, Summary, Resources, Contact Us, and top-level outline/outcome reconciliation.
- Access gaps: transcript timestamps and a direct image export are not exposed. The video remains paused; its transcript provides the instructional content. Current knowledge-check feedback is not visible, so earlier feedback is labeled as historical.
- Source state observed: the parent player reports 100% complete and marks this lesson Completed.
