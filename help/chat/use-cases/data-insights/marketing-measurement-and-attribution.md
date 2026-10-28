---
title: Measure Marketing Impact and Attribution with Coworker Chat
description: Use Coworker Chat to measure each channel's incremental impact, find where spend saturates, build what-if budget scenarios, and check marketing model quality.
product_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: CX Enterprise Coworker
---

# Marketing measurement and attribution overview

<!-- FLAG: Confidence: High for the first sentence and "Best for" (carried over from analytics-overview.md). Medium for the second sentence, which summarizes the row descriptions from the slides. -->

Use Adobe CX Enterprise Coworker Chat to understand the incremental impact of every marketing channel and campaign so that you can allocate spend to optimize ROI. See how channels work together, where extra spend stops paying off, and how different budget allocations compare before you commit.

Marketing measurement and attribution is one of several analysis domains in Coworker Chat. To see all domains, see [Start analyzing in Coworker Chat](/help/chat/use-cases/data-insights/analytics-overview.md#start-analyzing-in-coworker-chat) in Analyze data with Coworker Chat.

**Best for:** Analyst, Business user

## Prerequisites

<!-- FLAG: Confidence: High for the shared bullets (sourced from analytics-chat.md and the Skills and limitations table). They're confirmed for Measure campaign performance only; whether the marketing mix modeling use cases also need a data view or report suite connection is unknown. Low for the "Additional prerequisite" notes on the four marketing mix modeling rows in the Use cases table: incremental impact, response curves, budget scenarios, and model retraining describe a marketing mix model, but no source names the product or data that these use cases need. It could be Adobe Mix Modeler or Marketing Campaign Analytics (listed as an implementation path in implementation-guide.md). Confirm with the PM before publishing. -->

To use the use cases on this page, you need:

* Coworker Chat connected to your Customer Journey Analytics data views or Adobe Analytics report suites. See [Get started analyzing data with Coworker Chat](/help/chat/use-cases/data-insights/analytics-chat.md).
* View access to the data views or report suites that you want to analyze. Coworker Chat inherits your permissions from Customer Journey Analytics or Adobe Analytics.

## Use cases

| Use case | Function |
| --- | --- |
| Discover each channel's incremental impact | Shows each channel's incremental value, how channels amplify each other, and the role of outside factors.<p>**Sample prompts:**</p><ul><li>"Which channels drove the most incremental conversions?"</li><li>"How do paid search and display amplify each other?"</li></ul><p>**Additional prerequisite:** In addition to the [general prerequisites](#prerequisites), this use case also requires a trained marketing measurement model. *[Product and setup requirements to be confirmed.]*</p> |
| Find where spend starts to saturate<p>![Find where spend starts to saturate](assets/marketing-measurement.png)</p> | Shows response curves that reveal where extra spend stops paying off.<p>**Sample prompts:**</p><ul><li>"Where does paid search spend start to saturate?"</li><li>"Show response curves for each channel"</li></ul><p>**Additional prerequisite:** In addition to the [general prerequisites](#prerequisites), this use case also requires a trained marketing measurement model. *[Product and setup requirements to be confirmed.]*</p> |
| Build what-if budget scenarios | Compares allocation options side by side to support planning decisions.<p>**Best for:** Business user</p><p>**Sample prompts:**</p><ul><li>"Build budget scenarios for next quarter"</li><li>"What if I shift 10% of spend from display to search?"</li></ul><p>**Additional prerequisite:** In addition to the [general prerequisites](#prerequisites), this use case also requires a trained marketing measurement model. *[Product and setup requirements to be confirmed.]*</p> |
| Check model quality and when to retrain | Inspects model quality, training details, and scoring metrics so that you know how much to trust an answer.<p>**Best for:** Analyst</p><p>**Sample prompts:**</p><ul><li>"Are there other factors that we need for this model?"</li><li>"Does this model need to be retrained?"</li></ul><p>**Additional prerequisite:** In addition to the [general prerequisites](#prerequisites), this use case also requires a trained marketing measurement model. *[Product and setup requirements to be confirmed.]*</p> |
| [Measure campaign performance](/help/chat/use-cases/workflows.md#data-insights) | See how campaigns, channels, and web properties performed over a given period.<p>**Sample prompt:** "How did our Acrobat web campaigns perform last month?"</p><p>For more information, see [Data insights](/help/chat/use-cases/workflows.md#data-insights) in Coworker Chat use cases.</p> |

## Skills used

<!-- FLAG: Confidence: High for Measure campaign performance (workflows.md lists `cja`, `aa`, `dx-api`, and `knowledge-graph` for "Campaign performance"). `dx-api` and `knowledge-graph` aren't in the Skills and limitations table on analytics-overview.md. Low for the other four use cases: no source names their skills. Get the skill IDs from the PM, replace the placeholder row, and add the skills to the Skills and limitations table. -->

Coworker uses the following skills for the use cases described in this article. For a list of all analytics skills, including the permissions they require and what they don't cover, see [Skills and limitations](/help/chat/use-cases/data-insights/analytics-overview.md#skills-and-limitations) in Analyze data with Coworker Chat.

| Skill | Used for |
| --- | --- |
| `cja`, `aa`, `dx-api`, `knowledge-graph` | Measure campaign performance |
| *[Skill to be confirmed]* | Discover each channel's incremental impact<br>Find where spend starts to saturate<br>Build what-if budget scenarios<br>Check model quality and when to retrain |

## Tips for better results

<!-- FLAG: Confidence: Medium. The first two bullets are adapted from the best practices in analytics-overview.md. The third bullet is inferred from the sample prompts. -->

* Name the channels, campaigns, and date range you want to analyze.
* Mention any hypothesis you already have, such as two channels working together, so Coworker Chat can validate or rule it out.
* State the specific budget shift that you want to test when building what-if scenarios, such as moving 10% of spend from one channel to another.

## Next steps

* For an overview of data analysis with Coworker Chat, including the other analysis domains and best practices, see [Analyze data with Coworker Chat](/help/chat/use-cases/data-insights/analytics-overview.md).
* To set up Coworker Chat and walk through a working example, see [Get started analyzing data with Coworker Chat](/help/chat/use-cases/data-insights/analytics-chat.md).
