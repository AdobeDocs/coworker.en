---
title: Analyze Customer Journeys and Drop-Off with Coworker Chat
description: Use Coworker Chat to build funnels, find where customers drop off, diagnose conversion declines, and compare journeys across periods in your analytics data.
product_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: CX Enterprise Coworker
---

# Journey analysis overview

<!-- FLAG: Confidence: High for the first sentence and "Best for" (carried over from analytics-overview.md). Medium for the second sentence, which summarizes the row descriptions from the slides. -->

Use Adobe CX Enterprise Coworker Chat to find where customers drop out of the journey to conversion, and why, across channels, devices, and segments. Describe the journey in plain language, and Coworker Chat builds the funnel, shows the drop-off at each step, and helps you investigate the cause.

Journey analysis is one of several analysis domains in Coworker Chat. To see all domains, see [Start analyzing in Coworker Chat](/help/chat/use-cases/data-insights/analytics-overview.md#start-analyzing-in-coworker-chat) in Analyze data with Coworker Chat.

**Best for:** Analyst, Business user

## Prerequisites

To use the use cases on this page, you need:

* Coworker Chat connected to your Customer Journey Analytics data views or Adobe Analytics report suites. See [Get started analyzing data with Coworker Chat](/help/chat/use-cases/data-insights/analytics-chat.md).
* View access to the data views or report suites that you want to analyze. Coworker Chat inherits your permissions from Customer Journey Analytics or Adobe Analytics.

## Use cases

| Use case | Function |
| --- | --- |
| [Analyze Customer Journey Analytics and Adobe Analytics data](/help/chat/use-cases/data-insights/analytics-chat.md)<p>![Analyze Customer Journey Analytics and Adobe Analytics data](../../assets/coworker-funnel-response-card.png)</p> | Answers natural-language questions about your data views or report suites, builds funnels and other visualizations, and finds where customers drop off. You can open any visualization in Analysis Workspace for further analysis.<p>**Sample prompt:** "Show me page views for the last 30 days"</p><p>For more information, see [Get started analyzing data with Coworker Chat](/help/chat/use-cases/data-insights/analytics-chat.md).</p> |
| [Find where customers drop off](/help/chat/use-cases/data-insights/analytics-overview.md#skills-and-limitations) | Builds a funnel from a plain-language question, ranks the biggest leaks, and suggests next steps.<p>**Best for:** Business user</p><p>**Sample prompts:**</p><ul><li>"Where are we losing people on the way to purchase?"</li><li>"Walk me through the checkout funnel"</li></ul><p>For more information, see [Skills and limitations](/help/chat/use-cases/data-insights/analytics-overview.md#skills-and-limitations).</p> |
| Diagnose conversion declines | Investigates where customers drop out and evaluates what contributed to the change.<p>**Sample prompts:**</p><ul><li>"Why did conversions drop last week?"</li><li>"Where did customers drop out after the site change?"</li></ul> |
| Isolate the cause of a drop-off | Rules out causes one at a time to isolate the channel, device, or segment behind the problem.<p>**Sample prompts:**</p><ul><li>"Is cart abandonment worse on mobile or desktop?"</li><li>"Which channels leak the most between cart and purchase?"</li></ul> |
| Compare journeys across periods | Shows, step by step, whether the changes you shipped moved the funnel.<p>**Best for:** Business user</p><p>**Sample prompts:**</p><ul><li>"Compare checkout conversion this quarter to last"</li><li>"How did my funnel change after the redesign?"</li></ul> |

## Example: Find where customers drop off

For a full example conversation, from the first question to a recommendation, see [Example: Find where customers drop off](/help/chat/use-cases/data-insights/analytics-chat.md#example-find-where-customers-drop-off) in Get started analyzing data with Coworker Chat.

## Skills used

<!-- FLAG: Confidence: High for `cja` and `aa` (the Skills and limitations table lists funnel and fallout analysis and side-by-side comparison of time periods). Medium for the root cause analysis skills: workflows.md maps the prompt "Why did conversions drop last week?" to them, but the mapping to the slide rows "Diagnose conversion declines" and "Isolate the cause of a drop-off" is inferred. Confirm with the PM. -->

Coworker uses the following skills for the use cases described in this article. For a list of all analytics skills, including the permissions they require and what they don't cover, see [Skills and limitations](/help/chat/use-cases/data-insights/analytics-overview.md#skills-and-limitations) in Analyze data with Coworker Chat.

| Skill | Used for |
| --- | --- |
| `cja`, `aa` | Analyze Customer Journey Analytics and Adobe Analytics data<br>Find where customers drop off<br>Compare journeys across periods |
| `cja-root-cause-analysis`, `aa-root-cause-analysis` | Diagnose conversion declines<br>Isolate the cause of a drop-off |

## Tips for better results

<!-- FLAG: Confidence: High, except the first bullet (Medium), which moved here from Prerequisites and is inferred from how funnel prompts work. The rest are adapted from the best practices in analytics-overview.md. -->

* Name the journey steps that you want to analyze, such as product page, cart, checkout, and purchase.
* Name the dimensions, metrics, and date range you want analyzed, and reference components by their exact name.
* Ask for a funnel or fallout visualization if that's what you want to see.
* Specify the segments, channels, or devices that you want included, excluded, or compared.
* Mention any hypothesis you already have, such as a recent site change, so Coworker Chat can validate or rule it out.
* Ask for recommended next steps if you want Coworker Chat to suggest follow-up questions.
* Open any visualization in Analysis Workspace when you want more manual control. See [Open a visualization in Analysis Workspace](/help/chat/use-cases/data-insights/analytics-chat.md#open-a-visualization-in-analysis-workspace).

## Next steps

* For an overview of data analysis with Coworker Chat, including the other analysis domains and best practices, see [Analyze data with Coworker Chat](/help/chat/use-cases/data-insights/analytics-overview.md).
* To set up Coworker Chat and walk through a working example, see [Get started analyzing data with Coworker Chat](/help/chat/use-cases/data-insights/analytics-chat.md).
