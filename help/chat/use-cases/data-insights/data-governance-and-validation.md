---
title: Implement and Administer Analytics with Coworker Chat
description: Plan your implementation, track it in a checklist, and validate Adobe Analytics, Customer Journey Analytics, and Experience Platform data with Coworker Chat.
product_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: CX Enterprise Coworker
---

# Intelligent implementation and administration overview

Use Adobe CX Enterprise Coworker Chat to set up, migrate, and manage your analytics implementation, and to make sure that you can trust the data behind every answer. Coworker can plan your implementation, turn that plan into a checklist that your team can track, and validate your data after it's collected.

Intelligent implementation and administration is one of several analysis domains in Coworker Chat. To see all domains, see [Start analyzing in Coworker Chat](/help/chat/use-cases/data-insights/analytics-overview.md#start-analyzing-in-coworker-chat) in Analyze data with Coworker Chat.

**Best for:** Admin

## How the implementation workflow fits together

The use cases on this page follow an optional, three-stage workflow. You can use any stage on its own. For example, you can validate your data without first generating a plan or a checklist.

1. **Plan:** Get a personalized, ordered implementation or upgrade plan. See [Plan your implementation with Coworker](/help/chat/use-cases/data-insights/implementation-guide.md).
1. **Implement:** Turn your plan into a checklist in Coworker Projects that your team can assign and track. See [Generate an implementation checklist with Coworker Projects](/help/chat/use-cases/data-insights/intelligent-checklist.md).
1. **Validate:** Confirm that your data is configured and collected correctly. See the validation use cases in the [Use cases](#use-cases) table.

## Prerequisites

<!-- FLAG: Confidence: Medium for the shared bullets. They differ from the other domain pages on purpose: planning doesn't query your data, and Experience Platform validation uses Experience Platform datasets rather than data views or report suites. The permission inheritance for Experience Platform is inferred. High for the "Additional prerequisite" notes in the Use cases table, which are sourced from the "Before you begin" section of each linked article. Some of those articles flag their own prerequisites as unconfirmed (implementation-guide.md, intelligent-checklist.md, streaming-media-validation.md), so verify those rows when those flags are resolved. Validate dataset quality for Customer Journey Analytics is a video page with no stated prerequisites, so it isn't listed. -->

To use the use cases on this page, you need:

* Access to Coworker Chat. See [Get started analyzing data with Coworker Chat](/help/chat/use-cases/data-insights/analytics-chat.md).
* View access to the data that you want to validate. Coworker Chat inherits your permissions from the Adobe applications that it connects to.

## Use cases

| Use case | Function |
| --- | --- |
| [Plan your implementation](/help/chat/use-cases/data-insights/implementation-guide.md)<p>![Plan your implementation](../../assets/ui-guide-6.png)</p> | Creates a personalized, step-by-step plan for implementing Customer Journey Analytics, upgrading from Adobe Analytics, or setting up Content Analytics, Marketing Campaign Analytics, or Streaming Media collection on the Edge. Plans include details such as owners, effort estimates, dependencies, and validation steps.<p>**Sample prompt:** "Help me plan my implementation of Customer Journey Analytics"</p><p>**Additional prerequisite:** In addition to the [general prerequisites](#prerequisites), this use case also requires that you know which implementation path applies to you, and basic details about your current environment, such as your licensing status or planned data ingestion path.</p><p>For more information, see [Plan your implementation with Coworker](/help/chat/use-cases/data-insights/implementation-guide.md).</p> |
| [Generate an implementation checklist](/help/chat/use-cases/data-insights/intelligent-checklist.md)<p>![Generate an implementation checklist](../../assets/data-validation-aa-cja/date-detail.png)</p> <p>Experimental</p> | Turns your Customer Journey Analytics implementation plan into a checklist in Coworker Projects, where your team can assign steps, track status, and add approval gates.<p>**Additional prerequisite:** In addition to the [general prerequisites](#prerequisites), this use case also requires a completed implementation guide conversation, and access to Coworker Projects in your organization.</p><p>For more information, see [Generate an implementation checklist with Coworker Projects](/help/chat/use-cases/data-insights/intelligent-checklist.md).</p> |
| [Validate data when upgrading from Adobe Analytics to Customer Journey Analytics](/help/chat/use-cases/data-insights/data-validation-aa-cja.md)<p>![Validate data when upgrading from Adobe Analytics to Customer Journey Analytics](../../assets/data-validation-aa-cja/trend-bar-card.png)</p> | Compares dimensions, metrics, and trends between your Adobe Analytics report suites and Customer Journey Analytics data views, flags discrepancies, then recommends fixes to support your upgrade.<p>**Best for:** Admin, Analyst</p><p>**Sample prompts:**</p><ul><li>"Compare my AA report suite to my CJA data view"</li><li>"Which metrics do not match between AA and CJA?"</li></ul><p>**Additional prerequisite:** In addition to the [general prerequisites](#prerequisites), this use case also requires the Adobe Analytics report suite you want to validate, and the Customer Journey Analytics data view that contains the same data.</p><p>For more information, see [Validate data with Coworker when upgrading from Adobe Analytics to Customer Journey Analytics](/help/chat/use-cases/data-insights/data-validation-aa-cja.md).</p> |
| [Migrate Adobe Analytics projects to Customer Journey Analytics](/help/chat/use-cases/data-insights/migrate-projects-aa-cja.md) <br/>(Limited Availability) | Validates that the dimensions and metrics in an Adobe Analytics project are mapped to dimensions and metrics in a Customer Journey Analytics data view, helps you map any that can't be automatically mapped, then re-creates the project and its associated components in Customer Journey Analytics.<p>**Sample prompt:** "I want to migrate components from AA to CJA"</p><p>**Additional prerequisite:** In addition to the [general prerequisites](#prerequisites), this use case also requires Adobe Analytics MCP access, and either Adobe Analytics administrator rights or the Component Migration permission.</p><p>For more information, see [Migrate Adobe Analytics projects to Customer Journey Analytics with Coworker](/help/chat/use-cases/data-insights/migrate-projects-aa-cja.md).</p> |
| [Validate your Streaming Media implementation](/help/chat/use-cases/data-insights/streaming-media-validation.md)<p>![Validate your Streaming Media implementation](../../assets/ui-guide-8.png)</p> <p>Experimental</p> | Checks your datastream, schema, dataset, data view, and session data to confirm that streaming media tracking is configured and collecting data correctly.<p>**Sample prompt:** "How healthy is my streaming media implementation overall?"</p><p>**Additional prerequisite:** In addition to the [general prerequisites](#prerequisites), this use case also requires that your organization's Experience Platform and Customer Journey Analytics data is connected to Coworker. For some validation modes, you also need a video session ID or a log file.</p><p>For more information, see [Validate your Streaming Media implementation with Coworker](/help/chat/use-cases/data-insights/streaming-media-validation.md).</p> |
| [Validate dataset quality for Customer Journey Analytics](/help/chat/use-cases/data-insights/validate-dataset-quality-for-cja.md)<p>![Validate dataset quality for Customer Journey Analytics](../../assets/data-validation-aep/dataset-validation.png)</p> <p>Experimental (next week)</p> | Identifies the datasets that feed your Customer Journey Analytics reporting, then checks schemas, identity quality, and field quality so you can resolve issues before you build dashboards.<p>For more information, see [Validate Customer Journey Analytics data with the data validation skill in Coworker](/help/chat/use-cases/data-insights/validate-dataset-quality-for-cja.md).</p> |
| [Validate data after ingestion into Experience Platform](/help/chat/use-cases/data-insights/data-validation-aep.md)<p>![Validate data after ingestion into Experience Platform](../../assets/data-validation-aep/null-values.png)</p> | Runs statistical and semantic checks on Experience Platform datasets and fields to find data quality issues, such as invalid values or mapping problems, after a new implementation or as part of ongoing data stewardship.<p>**Sample prompts:**</p><ul><li>"Validate the dataset [dataset name]"</li><li>"Validate the [data field] from dataset [dataset name]"</li></ul><p>**Additional prerequisite:** In addition to the [general prerequisites](#prerequisites), this use case also requires the name or ID of the dataset you want to validate. Optionally, you can provide the name of a specific field to validate.</p><p>For more information, see [Validate your Experience Platform data with Coworker](/help/chat/use-cases/data-insights/data-validation-aep.md).</p> |
| [Accelerate data insights](/help/chat/use-cases/data-insights/accelerate-data-insights.md) | Shows in a video how Coworker plans your implementation, runs supported actions, and guides product and development steps across Adobe Experience Manager, Experience Platform, Web SDK, and Customer Journey Analytics until your website engagement data is ready to analyze.<p>For more information, see [Accelerate data insights with Coworker, AEM and CJA](/help/chat/use-cases/data-insights/accelerate-data-insights.md).</p> |

## Skills used

<!-- FLAG: Confidence: High for `aa-cja-validation` (listed in the Skills and limitations table and in workflows.md). Medium for `data-validation`: workflows.md lists it, but with a TODO to confirm the skill ID with engineering. Medium for the implementation guide skills and the Streaming Media Validation skill: the articles name them but don't give technical skill IDs, so they're listed by display name. Only `aa-cja-validation` currently appears in the Skills and limitations table on analytics-overview.md. Add the others there so the link below covers them. -->

Coworker uses the following skills for the use cases described in this article. For a list of all analytics skills, including the permissions they require and what they don't cover, see [Skills and limitations](/help/chat/use-cases/data-insights/analytics-overview.md#skills-and-limitations) in Analyze data with Coworker Chat.

| Skill | Used for |
| --- | --- |
| Implementation guide skills (one each for Customer Journey Analytics, an Adobe Analytics to Customer Journey Analytics upgrade, Content Analytics, Marketing Campaign Analytics, and Streaming Media) | Plan your implementation |
| `aa-cja-validation` | Validate data when upgrading from Adobe Analytics to Customer Journey Analytics |
| Streaming Media Validation skill | Validate your Streaming Media implementation |
| Data Validation skill (`data-validation`) | Validate dataset quality for Customer Journey Analytics<br>Validate data after ingestion into Experience Platform |

## Tips for better results

* Name the specific report suite and data view you want to compare when validating data.
* Use validation results as a guide for your own changes. The Streaming Media Validation and Data Validation skills identify issues but don't change your configuration or data.
* Rerun Streaming Media validation after each implementation change. It runs on demand and doesn't provide continuous monitoring.
* Use the implementation guide skills for planning only. They don't access your Adobe systems or perform the implementation.

## Next steps

* For an overview of data analysis with Coworker Chat, including the other analysis domains and best practices, see [Analyze data with Coworker Chat](/help/chat/use-cases/data-insights/analytics-overview.md).
* To set up Coworker Chat and walk through a working example, see [Get started analyzing data with Coworker Chat](/help/chat/use-cases/data-insights/analytics-chat.md).
