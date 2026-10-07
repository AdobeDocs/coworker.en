---
title: Analyze Customer Journey Analytics Data with Coworker Chat
description: Learn how to use Adobe CX Enterprise Coworker Chat to analyze Customer Journey Analytics data, build funnels, and find where customers drop off in the journey.
hold: true
product_v2:
    internal-label: CX Enterprise Coworker
feature_v2:
    internal-label: CX Enterprise Coworker
---

# Analyze data with Coworker Chat

The information on this page provides an overview of Adobe CX Enterprise Coworker Chat and how it can help you analyze data for your organization.

Coworker Chat enables teams to automate Adobe product tasks using natural language, quickly turning ideas into actions with flexible planning, customizable skills, and intelligent execution. For more general information about Coworker, see [CX Enterprise Coworker overview](/help/home.md).

>[!VIDEO](https://video.tv.adobe.com/v/3503519/?learn=on&enablevpops)

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

The following use cases are grouped by what you want to accomplish. Each group lists the roles it's best suited for.

### Measure performance

**Best for:** Analyst, Business user

| Use case | Function |
| --- | --- |
| [Analyze Customer Journey Analytics and Adobe Analytics data](/help/chat/use-cases/data-insights/analytics-chat.md)<p>![Analyze Customer Journey Analytics and Adobe Analytics data](../../assets/coworker-funnel-response-card.png)</p> | Answers natural-language questions about your data views or report suites, builds funnels and other visualizations, and finds where customers drop off. You can open any visualization in Analysis Workspace for further analysis.<p>**Sample prompt:** "Show me page views for the last 30 days"</p><p>For more information, see [Get started analyzing data with Coworker Chat](/help/chat/use-cases/data-insights/analytics-chat.md).</p> |
| [Compare performance](#skills-and-limitations) | Compare metrics across channels, time periods, or segments side by side.<p>**Sample prompt:** "Compare revenue by channel month over month"</p><p>For more information, see [Skills and limitations](#skills-and-limitations).</p> |
| [Measure campaign performance](/help/chat/use-cases/overview.md#data-insights) | See how campaigns, channels, and web properties performed over a given period.<p>**Sample prompt:** "How did our Acrobat web campaigns perform last month?"</p><p>For more information, see [Data insights](/help/chat/use-cases/overview.md#data-insights) in Coworker Chat use cases.</p> |
| [Analyze funnels](#skills-and-limitations) | Walk through multi-step conversion funnels and see the drop-off at each stage.<p>**Best for:** Analyst</p><p>**Sample prompt:** "Walk me through the checkout funnel"</p><p>For more information, see [Skills and limitations](#skills-and-limitations).</p> |

### Find out why metrics changed

**Best for:** Analyst

| Use case | Function |
| --- | --- |
| [Explore trends and root causes](/help/chat/use-cases/data-insights/root-cause-analysis.md)<p>![Explore trends and root causes](../../assets/data-validation-aa-cja/trend-line-card.png)</p> | Identifies trends in your Customer Journey Analytics and Adobe Analytics data and the factors that drive changes in performance, without manual queries.<p>**Sample prompt:** "Why did conversions drop last week?"</p><p>For more information, see [Customer Journey Analytics & Coworker](/help/chat/use-cases/data-insights/root-cause-analysis.md).</p> |
| [Analyze operational trends and causes](/help/chat/use-cases/overview.md#data-insights) | Query historical time-series data for audiences, datasets, and journeys, and identify what caused a change.<p>**Best for:** Admin, Analyst</p><p>**Sample prompt:** "Show me audience size trends over the last 90 days"</p><p>For more information, see [Data insights](/help/chat/use-cases/overview.md#data-insights) in Coworker Chat use cases.</p> |

### Predict future performance

**Best for:** Analyst

| Use case | Function |
| --- | --- |
| [Forecast metrics](#skills-and-limitations) | Project future metric values from historical Customer Journey Analytics or Adobe Analytics data, such as whether you're on track to hit a revenue goal.<p>**Sample prompt:** "Forecast sessions for the next 30 days"</p><p>For more information, see [Skills and limitations](#skills-and-limitations).</p> |

### Share insights with stakeholders

**Best for:** Analyst, Business user

| Use case | Function |
| --- | --- |
| [Create executive summaries and KPI digests](#skills-and-limitations) | Produce stakeholder-ready performance summaries, recommendations, and slide deck outlines.<p>**Sample prompt:** "Give me an executive summary of last month"</p><p>For more information, see [Skills and limitations](#skills-and-limitations).</p> |

### Plan your implementation or upgrade

**Best for:** Admin

| Use case | Function |
| --- | --- |
| [Plan your implementation](/help/chat/use-cases/data-insights/implementation-guide.md)<p>![Plan your implementation](../../assets/ui-guide-6.png)</p> | Creates a personalized, step-by-step plan for implementing Customer Journey Analytics, upgrading from Adobe Analytics, or setting up Content Analytics, Marketing Campaign Analytics, or Streaming Media collection on the Edge. Plans include details such as owners, effort estimates, dependencies, and validation steps.<p>**Sample prompt:** "Help me plan my implementation of Customer Journey Analytics"</p><p>For more information, see [Plan your implementation with Coworker](/help/chat/use-cases/data-insights/implementation-guide.md).</p> |
| [Generate an implementation checklist](/help/chat/use-cases/data-insights/intelligent-checklist.md)<p>![Generate an implementation checklist](../../assets/data-validation-aa-cja/date-detail.png)</p> | Turns your Customer Journey Analytics implementation plan into a checklist in Coworker Projects, where your team can assign steps, track status, and add approval gates.<p>For more information, see [Generate an implementation checklist with Coworker Projects](/help/chat/use-cases/data-insights/intelligent-checklist.md).</p> |

### Confirm that your data is accurate

**Best for:** Admin

| Use case | Function |
| --- | --- |
| [Validate data when upgrading from Adobe Analytics to Customer Journey Analytics](/help/chat/use-cases/data-insights/data-validation-aa-cja.md)<p>![Validate data when upgrading from Adobe Analytics to Customer Journey Analytics](../../assets/data-validation-aa-cja/trend-bar-card.png)</p> | Compares dimensions, metrics, and trends between your Adobe Analytics report suites and Customer Journey Analytics data views, then recommends fixes to support your upgrade.<p>**Best for:** Admin, Analyst</p><p>**Sample prompt:** "Compare my AA report suite to my CJA data view"</p><p>For more information, see [Validate data with Coworker when upgrading from Adobe Analytics to Customer Journey Analytics](/help/chat/use-cases/data-insights/data-validation-aa-cja.md).</p> |
| [Validate your Streaming Media implementation](/help/chat/use-cases/data-insights/streaming-media-validation.md)<p>![Validate your Streaming Media implementation](../../assets/ui-guide-8.png)</p> | Checks your datastream, schema, dataset, data view, and session data to confirm that streaming media tracking is configured and collecting data correctly.<p>**Sample prompt:** "How healthy is my streaming media implementation overall?"</p><p>For more information, see [Validate your Streaming Media implementation with Coworker](/help/chat/use-cases/data-insights/streaming-media-validation.md).</p> |
| [Validate dataset quality for Customer Journey Analytics](/help/chat/use-cases/data-insights/validate-dataset-quality-for-cja.md)<p>![Validate dataset quality for Customer Journey Analytics](../../assets/data-validation-aep/dataset-validation.png)</p> | Identifies the datasets that feed your Customer Journey Analytics reporting, then checks schemas, identity quality, and field quality so you can resolve issues before you build dashboards.<p>For more information, see [Validate Customer Journey Analytics data with the data validation skill in Coworker](/help/chat/use-cases/data-insights/validate-dataset-quality-for-cja.md).</p> |
| [Validate data after ingestion into Experience Platform](/help/chat/use-cases/data-insights/data-validation-aep.md)<p>![Validate data after ingestion into Experience Platform](../../assets/data-validation-aep/null-values.png)</p> | Runs statistical and semantic checks on Experience Platform datasets and fields to find data quality issues, such as invalid values or mapping problems.<p>**Sample prompt:** "Validate the dataset Electronics Sample 1000"</p><p>For more information, see [Validate your Experience Platform data with Coworker](/help/chat/use-cases/data-insights/data-validation-aep.md).</p> |

### Automate analyses that you repeat

**Best for:** Analyst

| Use case | Function |
| --- | --- |
| [Create custom Customer Journey Analytics skills](#skills-and-limitations) | Turn an analysis that you repeat into a reusable skill that persists across sessions.<p>**Sample prompt:** "Turn this weekly revenue analysis into a reusable skill"</p><p>For more information, see [Skills and limitations](#skills-and-limitations).</p> |

For more information about these use cases, including the skills they use and more sample prompts, see [Data insights use cases](/help/chat/use-cases/overview.md#data-insights).

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

To set up Coworker Chat and walk through a working example, see [Get started analyzing data with Coworker Chat](/help/chat/use-cases/data-insights/analytics-chat.md).


