---
title: Analyze Customer Journey Analytics Data with Coworker Chat
description: Learn how to use Adobe CX Enterprise Coworker Chat to analyze Customer Journey Analytics data, build funnels, and find where customers drop off in the journey.
product_v2:
    internal-label: CX Enterprise Coworker
feature_v2:
    internal-label: CX Enterprise Coworker
---

# Analyze data with Coworker Chat

The information on this page provides an overview of Adobe CX Enterprise Coworker Chat and how it can help you analyze data for your organization.

Coworker Chat enables teams to automate Adobe product tasks using natural language, quickly turning ideas into actions with flexible planning, customizable skills, and intelligent execution. For more general information about Coworker, see [CX Enterprise Coworker overview](/help/home.md).

## How data analysis works

Coworker Chat can perform advanced data analysis that was previously possible only in Analysis Workspace. Coworker Chat accesses data from your Customer Journey Analytics data views or Adobe Analytics report suites, allowing you to explore data and get answers with natural-language prompts.

Coworker Chat inherits permissions from Customer Journey Analytics or Adobe Analytics. You can access only those data views, report suites, dimensions, metrics, and segments available to you in Analysis Workspace.

When you create a visualization in Coworker chat, you can open it in Analysis Workspace any time for more manual control.

## Quick answers and deep-thought work

You can use Coworker Chat in two ways, depending on how much analysis you need:

* **Quick answers** - Ask a direct, plain-language question and get an immediate answer. Business users often use Coworker Chat this way, and analysts use it too when they need a fast answer for a stakeholder.
* **Deep-thought work** - Have an extended, multi-turn conversation with Coworker Chat to investigate a business problem, rule out causes, and arrive at a recommendation. Analysts typically use this approach to explore data in depth before making a recommendation.

## Start analyzing in Coworker Chat

Get started by describing what you want to know in plain language. Coworker Chat plans the analysis, queries your data views or report suites, and creates visualizations and summaries. 

The following use cases are grouped by analysis domain. Each domain has its own page with use cases, sample prompts, prerequisites, and the skills that it uses.

| Domain | What you can do | Best for |
| --- | --- | --- |
| [Data governance and validation](/help/chat/use-cases/data-insights/data-governance-and-validation.md) | Set up, migrate, and manage your implementation, and make sure that you can trust the data behind every answer. | Admin |
| [Journey analysis](/help/chat/use-cases/data-insights/journey-analysis.md) | Find where customers drop out of the journey to conversion, and why, across channels, devices, and segments. | Analyst, Business user |
| [Audience and segment analysis](/help/chat/use-cases/data-insights/audience-and-segment-analysis.md) | Understand which customer groups behave differently and how, so you can focus on the ones that matter most. | Analyst, Business user |
| [Business performance](/help/chat/use-cases/data-insights/business-performance.md) | Understand how the business is doing, why a metric moved, where it's heading, and what to do next. | Analyst, Business user |
| [Content performance](/help/chat/use-cases/data-insights/content-performance.md) | Understand which content wins and why, down to the attributes of each asset, so you can invest in what works. | Business user |
| [Marketing measurement and attribution](/help/chat/use-cases/data-insights/marketing-measurement-and-attribution.md) | Understand the incremental impact of every marketing channel and campaign so that you can allocate spend to optimize ROI. | Analyst, Business user |

## Skills and limitations

The following skills are available for analyzing Customer Journey Analytics or Adobe Analytics data.

| Skill | Use it to | Required permissions | Out of scope |
| --- | --- | --- | --- |
| `cja`, `aa` | Query Customer Journey Analytics data views (`cja`) or Adobe Analytics report suites (`aa`) in real time:<ul><li>Pull metrics, dimensions, segments, data views, and report suites</li><li>Compare channels, time periods, or segments side by side</li><li>Run multi-step funnel and fallout analysis</li><li>Forecast metrics based on historical trends</li></ul> | View access to the data view or report suite you want to query | <ul><li>Creating or editing data view or report suite components</li><li>Data outside the data views or report suites you have access to</li><li>Predictive modeling beyond metric forecasting</li></ul> |
| `cja-root-cause-analysis`, `aa-root-cause-analysis` | Investigate why a metric changed instead of just reporting that it changed:<ul><li>Investigate a change in a known metric over a known period</li><li>Surface the dimensions and segments that contributed to the change</li></ul> | View access to the data view or report suite being analyzed | <ul><li>Detecting anomalies you haven't asked about (no automated or real-time alerting)</li><li>Root cause analysis for metrics outside a data view or report suite you have access to</li></ul> |
| `cja-executive-summary` | Produce stakeholder-ready summaries of your data:<ul><li>Summarize performance over a specified period</li><li>Generate prescriptive recommendations based on the data</li><li>Outline content for a slide deck or stakeholder readout</li></ul> | View access to the data views or report suites covered in the summary | <ul><li>Building the final slide deck or presentation file</li><li>Summaries that span data views or report suites you don't have access to</li></ul> |
| `aa-cja-validation` | Compare, audit, and reconcile data between [!DNL Adobe Analytics] and Customer Journey Analytics:<ul><li>Compare metric values between a report suite and a data view</li><li>Flag discrepancies between the two data sources</li></ul> | View access to the [!DNL Adobe Analytics] report suite and the Customer Journey Analytics data view being compared | <ul><li>Resolving the underlying cause of a data discrepancy</li><li>Validating data sources other than [!DNL Adobe Analytics] and Customer Journey Analytics</li></ul> |
| `cja-skill-creator` | Turn an analysis you've already run into a reusable skill:<ul><li>Convert a completed analysis into a named, reusable skill</li><li>Make a saved skill available across your future chat sessions</li></ul> | Manage skills | <ul><li>Sharing a saved skill with other users automatically (organization-level skill libraries require admin setup)</li><li>Editing the data view or report suite components a skill references</li></ul> |

## Best practices when analyzing data with Coworker Chat

### Organization-level best practices

* Appoint an analyst from your organization as a Coworker champion.

* Create a library of vetted prompts and skills that correlate with the data and components that are available to users.

* Create one or more skills that direct Coworker Chat to use only those components that you want used in analyses. This helps Coworker Chat give users in your organization the most relevant data.

* Educate users on when to ask Coworker Chat for a quick answer versus when to use it for deep thought work.

### User-level best practices

* Use plan mode.

  This mode is especially useful for complex tasks, but can also yield better results for simple tasks because it allows Coworker to ask follow-up questions before acting. For more information, see [Plan mode](/help/chat/ui-guide.md#plan-mode).

* When creating a prompt, be as specific as possible:

  * Name the dimensions, metrics, and date range you want analyzed.
  * Reference components by their exact name.
  * Specify any segments, audiences, channels, or devices you want included, excluded, or compared.
  * State whether you want a specific visualization type, such as a funnel, trend, or cohort table.
  * Ask for recommended next steps if you want Coworker Chat to suggest follow-up questions.
  * Ask for a forecast horizon, such as "next 30 days," when projecting metrics.
  * Mention any hypothesis you already have, so Coworker Chat can validate or rule it out.
  * Ask for the contributing dimensions if you want a breakdown of a metric change.
  * Specify the audience for a summary, such as leadership or the marketing team, and request a slide deck outline if you plan to present the findings.
  * Name the specific report suite and data view you want to compare when validating data.
  * Complete an analysis first, then ask Coworker Chat to save it as a skill, giving it a clear, descriptive name and noting how often you plan to reuse it.

* Add standard directions to the Coworker Chat memory. For example, if you always use data from the same data views or report suites, add that to the memory. For more information, see [Add a data view or report suite preference in Memory](/help/chat/use-cases/data-insights/analytics-chat.md#add-a-data-view-or-report-suite-preference-in-memory) in Get started analyzing data with Coworker Chat.

## Next steps

* To set up Coworker Chat and walk through a working example, see [Get started analyzing data with Coworker Chat](/help/chat/use-cases/data-insights/analytics-chat.md).
* To see every Coworker Chat workflow and the skills behind it, see [Coworker Chat workflows](/help/chat/use-cases/workflows.md).


