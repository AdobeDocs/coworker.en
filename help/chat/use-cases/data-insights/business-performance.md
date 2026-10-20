---
title: Analyze Business Performance and KPIs with Coworker Chat
description: Use Coworker Chat to explain why metrics moved, forecast where they're heading, prepare performance reviews, and turn repeat analyses into reusable skills.
product_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: CX Enterprise Coworker
---

# Business performance overview

<!-- FLAG: Confidence: High for the first sentence and "Best for" (carried over from analytics-overview.md). Medium for the second sentence, which summarizes the row descriptions. -->

Use Adobe CX Enterprise Coworker Chat to understand how the business is doing, why a metric moved, where it's heading, and what to do next. Investigate changes in your key metrics, project them forward, and turn your findings into stakeholder-ready summaries and reusable skills.

Business performance is one of several analysis domains in Coworker Chat. To see all domains, see [Start analyzing in Coworker Chat](/help/chat/use-cases/data-insights/analytics-overview.md#start-analyzing-in-coworker-chat) in Analyze data with Coworker Chat.

**Best for:** Analyst, Business user

## Prerequisites

To use the use cases on this page, you need:

* Coworker Chat connected to your Customer Journey Analytics data views or Adobe Analytics report suites. See [Get started analyzing data with Coworker Chat](/help/chat/use-cases/data-insights/analytics-chat.md).
* View access to the data views or report suites that you want to analyze. Coworker Chat inherits your permissions from Customer Journey Analytics or Adobe Analytics.

## Use cases

| Use case | Function |
| --- | --- |
| [Explore trends and root causes](/help/chat/use-cases/data-insights/root-cause-analysis.md)<p>![Explore trends and root causes](../../assets/data-validation-aa-cja/trend-line-card.png)</p> | Identifies trends in your Customer Journey Analytics and Adobe Analytics data and the factors that drive changes in performance, without manual queries.<p>**Sample prompt:** "Why did conversions drop last week?"</p><p>For more information, see [Customer Journey Analytics & Coworker](/help/chat/use-cases/data-insights/root-cause-analysis.md).</p> |
| [Explain why a metric moved](/help/chat/use-cases/data-insights/analytics-overview.md#skills-and-limitations) | Runs a root cause analysis that surfaces the dimensions and segments behind a change and rules out the rest.<p>**Sample prompts:**</p><ul><li>"Why did revenue spike on Tuesday?"</li><li>"What drove the change in sessions this month?"</li></ul><p>For more information, see [Skills and limitations](/help/chat/use-cases/data-insights/analytics-overview.md#skills-and-limitations).</p> |
| [Prepare business performance reviews](/help/chat/use-cases/data-insights/analytics-overview.md#skills-and-limitations) | Turns trusted metrics into an explained performance story, with findings and recommended next steps.<p>**Sample prompts:**</p><ul><li>"Give me an executive summary of last month"</li><li>"Summarize performance for the leadership team"</li></ul><p>For more information, see [Skills and limitations](/help/chat/use-cases/data-insights/analytics-overview.md#skills-and-limitations).</p> |
| [Forecast where a metric is heading](/help/chat/use-cases/data-insights/analytics-overview.md#skills-and-limitations) | Projects a metric from historical data so that you can see a miss coming.<p>**Sample prompts:**</p><ul><li>"Forecast sessions for the next 30 days"</li><li>"Are we on track to hit our revenue goal?"</li></ul><p>For more information, see [Skills and limitations](/help/chat/use-cases/data-insights/analytics-overview.md#skills-and-limitations).</p> |
| [Create custom Customer Journey Analytics skills](/help/chat/use-cases/data-insights/analytics-overview.md#skills-and-limitations) | Turn an analysis that you repeat into a reusable skill that persists across sessions.<p>**Sample prompt:** "Turn this weekly revenue analysis into a reusable skill"</p><p>**Additional prerequisite:** In addition to the [general prerequisites](#prerequisites), this use case also requires the Manage skills permission.</p><p>For more information, see [Skills and limitations](/help/chat/use-cases/data-insights/analytics-overview.md#skills-and-limitations).</p> |
| [Repeat successful analysis across markets](/help/chat/use-cases/data-insights/analytics-overview.md#skills-and-limitations) | Applies a proven analytical approach across brands, regions, or business units.<p>**Best for:** Analyst</p><p>**Sample prompt:** "Run my weekly funnel skill for the EMEA data view"</p><p>For more information, see [Skills and limitations](/help/chat/use-cases/data-insights/analytics-overview.md#skills-and-limitations).</p> |

## Skills used

<!-- FLAG: Confidence: High for the root cause analysis skills, `cja-executive-summary`, forecasting with `cja` and `aa`, and `cja-skill-creator` for creating skills. All are listed in the Skills and limitations table and in workflows.md. Medium for mapping Repeat successful analysis across markets to `cja-skill-creator`: the row describes running a saved skill, which is inferred. workflows.md also lists `cja-bacom-anomaly-tracker-v2`, `cja-cno-weekly-pulse`, and `cja-reporting` for executive summaries. They're left out because they look org-specific. Confirm with the PM. -->

Coworker uses the following skills for the use cases described in this article. For a list of all analytics skills, including the permissions they require and what they don't cover, see [Skills and limitations](/help/chat/use-cases/data-insights/analytics-overview.md#skills-and-limitations) in Analyze data with Coworker Chat.

| Skill | Used for |
| --- | --- |
| `cja-root-cause-analysis`, `aa-root-cause-analysis` | Explore trends and root causes<br>Explain why a metric moved |
| `cja-executive-summary` | Prepare business performance reviews |
| `cja`, `aa` | Forecast where a metric is heading |
| `cja-skill-creator` | Create custom Customer Journey Analytics skills<br>Repeat successful analysis across markets |

## Tips for better results

* Name the metric and the period of the change that you want to investigate. Root cause analysis works on a known metric over a known period.
* Ask for the contributing dimensions if you want a breakdown of a metric change.
* Ask for a forecast horizon, such as "next 30 days," when projecting metrics.
* Specify the audience for a summary, such as leadership or the marketing team, and request a slide deck outline if you plan to present the findings.
* Complete an analysis first, then ask Coworker Chat to save it as a skill. Give the skill a clear, descriptive name, and note how often you plan to reuse it.

## Next steps

* For an overview of data analysis with Coworker Chat, including the other analysis domains and best practices, see [Analyze data with Coworker Chat](/help/chat/use-cases/data-insights/analytics-overview.md).
* To see root cause analysis in action, see [Customer Journey Analytics & Coworker](/help/chat/use-cases/data-insights/root-cause-analysis.md).
