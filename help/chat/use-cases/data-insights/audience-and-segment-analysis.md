---
title: Compare Audiences and Customer Segments with Coworker Chat
description: Use Coworker Chat to compare customer groups, find overlooked growth opportunities, track audience trends, and turn insights into audiences you can build.
product_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: CX Enterprise Coworker
feature_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: CX Enterprise Coworker
---

# Audience and segment analysis overview

<!-- FLAG: Confidence: High for the first sentence and "Best for" (carried over from analytics-overview.md). Medium for the second sentence, which summarizes the row descriptions. -->

Use Adobe CX Enterprise Coworker Chat to understand which customer groups behave differently and how, so you can focus on the ones that matter most. Compare channels, time periods, and segments side by side, track how audiences change over time, and turn what you find into an audience that you can build.

Audience and segment analysis is one of several analysis domains in Coworker Chat. To see all domains, see [Start analyzing in Coworker Chat](/help/chat/use-cases/data-insights/analytics-overview.md#start-analyzing-in-coworker-chat) in Analyze data with Coworker Chat.

**Best for:** Analyst, Business user

## Prerequisites

<!-- FLAG: Confidence: High for the shared bullets (sourced from the Skills and limitations table and analytics-chat.md). Medium for the "Additional prerequisite" notes on the operational trends rows in the Use cases table: workflows.md lists the operational time-series skill as available for "All Eligible Applications" but doesn't state required permissions. Mapping Track audience size trends to the same requirement is inferred. Low for the "Additional prerequisite" note on the Take an insight into an audience row: inferred from the Audiences section of workflows.md, which lists Real-Time CDP as the application for audience creation. Confirm with the PM. -->

To use the use cases on this page, you need:

* Coworker Chat connected to your Customer Journey Analytics data views or Adobe Analytics report suites. See [Get started analyzing data with Coworker Chat](/help/chat/use-cases/data-insights/analytics-chat.md).
* View access to the data views or report suites that you want to analyze. Coworker Chat inherits your permissions from Customer Journey Analytics or Adobe Analytics.

## Use cases

| Use case | Function |
| --- | --- |
| [Compare performance](/help/chat/use-cases/data-insights/analytics-overview.md#skills-and-limitations) | Compare metrics across channels, time periods, or segments side by side.<p>**Sample prompt:** "Compare revenue by channel month over month"</p><p>For more information, see [Skills and limitations](/help/chat/use-cases/data-insights/analytics-overview.md#skills-and-limitations).</p> |
| [Compare customer groups](/help/chat/use-cases/data-insights/analytics-overview.md#skills-and-limitations) | Shows which groups behave differently, without requiring you to write segment logic.<p>**Best for:** Business user</p><p>**Sample prompts:**</p><ul><li>"Do paid social visitors convert differently than email?"</li><li>"Compare new and returning visitors on revenue"</li></ul><p>For more information, see [Skills and limitations](/help/chat/use-cases/data-insights/analytics-overview.md#skills-and-limitations).</p> |
| Find overlooked growth opportunities | Explores audiences, journeys, and channels to identify opportunities that overall performance figures can conceal.<p>**Sample prompts:**</p><ul><li>"Which audiences convert above average but get little traffic?"</li><li>"Which channels are underused for their conversion rate?"</li></ul> |
| [Analyze operational trends and causes](/help/chat/use-cases/workflows.md#data-insights) | Query historical time-series data for audiences, datasets, and journeys, and identify what caused a change.<p>**Best for:** Admin, Analyst</p><p>**Sample prompt:** "Show me audience size trends over the last 90 days"</p><p>**Additional prerequisite:** In addition to the [general prerequisites](#prerequisites), this use case also requires access to the audiences, datasets, or journeys that you want to analyze.</p><p>For more information, see [Data insights](/help/chat/use-cases/workflows.md#data-insights) in Coworker Chat use cases.</p> |
| Track audience size trends | Spots audiences that are growing or shrinking and looks into the cause.<p>**Best for:** Admin, Analyst</p><p>**Sample prompt:** "Which audiences grew the fastest this quarter?"</p><p>**Additional prerequisite:** In addition to the [general prerequisites](#prerequisites), this use case also requires access to the audiences that you want to track.</p> |
| Take an insight into an audience | Goes from an insight to an audience that you can build, without starting over.<p>**Sample prompts:**</p><ul><li>"Open this comparison in Analysis Workspace"</li><li>"Help me build an audience from this group"</li></ul><p>**Additional prerequisite:** In addition to the [general prerequisites](#prerequisites), this use case also requires access to Real-Time Customer Data Platform and permission to create audiences.</p> |

## Skills used

<!-- FLAG: Confidence: High for Compare performance and Analyze operational trends and causes (skills listed for "Comparative analysis" and "Operational time-series & causal analysis" in workflows.md). Medium for Compare customer groups and Track audience size trends, which are mapped to the same skills based on their descriptions. Low for `audience-creation-flow`: inferred from the Audiences section of workflows.md. No skill is listed for Find overlooked growth opportunities because no source names one. Only `cja`, `aa`, and the root cause analysis skills currently appear in the Skills and limitations table on analytics-overview.md. -->

Coworker uses the following skills for the use cases described in this article. For a list of all analytics skills, including the permissions they require and what they don't cover, see [Skills and limitations](/help/chat/use-cases/data-insights/analytics-overview.md#skills-and-limitations) in Analyze data with Coworker Chat.

| Skill | Used for |
| --- | --- |
| `cja`, `aa` | Compare performance<br>Compare customer groups |
| `cja-root-cause-analysis`, `aa-root-cause-analysis` | Compare performance |
| `operational-stats-causal-analysis` | Analyze operational trends and causes<br>Track audience size trends |
| `audience-creation-flow` | Take an insight into an audience |

## Tips for better results

* Specify the segments, audiences, channels, or devices that you want included, excluded, or compared.
* Reference segments and other components by their exact name.
* Name the metric and date range that you want to compare on, such as revenue month over month.
* Ask for the contributing dimensions if you want to know why one group behaves differently from another.

## Next steps

* For an overview of data analysis with Coworker Chat, including the other analysis domains and best practices, see [Analyze data with Coworker Chat](/help/chat/use-cases/data-insights/analytics-overview.md).
* To build audiences directly in Coworker Chat, see [Assess Experience Platform health and build audiences from natural language with Coworker](/help/chat/use-cases/audiences/create-audience-from-natural-language.md).
