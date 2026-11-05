---
title: Analyze root causes with Adobe Analytics and Customer Journey Analytics
description: Use Adobe CX Enterprise Coworker to investigate metric changes, identify contributing dimensions and segments, and test hypotheses in Adobe Analytics and CJA.
feature: AI Tools
role: User
level: Beginner
doc-type: Feature Video
duration: 186
last-substantial-update: 2026-08-10T00:00:00.000Z
jira: KT-22082
product_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: Coworker
---

# Analyze root causes with [!DNL Adobe Analytics] and [!DNL Customer Journey Analytics]

Use Adobe CX Enterprise Coworker Chat to investigate why a metric changed in Adobe Analytics or Customer Journey Analytics (CJA). Coworker analyzes the change you specify, surfaces contributing dimensions and segments, and helps you test hypotheses using natural language.

## Use Customer Journey Analytics data for root cause analysis

The following video demonstrates how Coworker combines conversational AI with Customer Journey Analytics. Learn how to ask questions in natural language, visualize results, identify meaningful trends, and uncover factors that drive performance without building manual queries.

>[!VIDEO](https://video.tv.adobe.com/v/3496847/?learn=on&enablevpops)

### Prerequisites

Before you start:

1. **Have access to Coworker Chat and connect Customer Journey Analytics.** Confirm that your organization has configured the required integration.
1. **Have view access to the CJA data view you want to analyze.** Coworker can use only the data views and components available to you.
1. **Choose the data view that contains the relevant metric and dimensions.** If you can access multiple data views, name the one you want Coworker to use.
1. **Identify the change you want investigated.** Specify the metric, date range, and comparison period. You can also provide dimensions, segments, or a hypothesis to focus the analysis.

### Sample prompts for Customer Journey Analytics

Replace the bracketed text with component names and time periods from your data view.

* In the **[data view name]** data view, why did **[metric]** change during **[date range]** compared with **[comparison date range]**? Break down the change by **[dimension]** and show the segments that contributed most.
* In the **[data view name]** data view, did **[dimension or segment]** contribute to the decrease in **[metric]** from **[date range A]** to **[date range B]**? Compare the values for both periods and explain what changed.
* In the **[data view name]** data view, compare **[metric]** for **[segment A]** and **[segment B]** during **[date range]**. Which dimensions contributed most to the difference?
* In the **[data view name]** data view, test this hypothesis: **[state your hypothesis]**. Analyze **[metric]** for **[date range]**, and show the dimensions or segments that support or do not support it.

## Use Adobe Analytics data for root cause analysis

Coworker can investigate why a metric changed in an Adobe Analytics report suite. It uses the `aa-root-cause-analysis` skill to analyze a change you specify and identify the dimensions and segments that contributed to it.

### Prerequisites

Before you start:

1. **Have access to Coworker Chat and connect Adobe Analytics.** In Coworker, go to **Customizations > Integrations** and confirm that the `aa-mcp` integration is listed and connected. If it is not available, ask your administrator to check your organization's setup. See [Get started analyzing data with Coworker Chat](https://experienceleague.adobe.com/en/docs/coworker/content/chat/use-cases/data-insights/analytics-chat) for setup guidance.
1. **Have view access to the Adobe Analytics report suite you want to analyze.** Coworker inherits your Adobe Analytics permissions and can use only the report suites and components available to you in Analysis Workspace.
1. **Choose the report suite that contains the relevant data.** If you can access multiple report suites, name the report suite you want Coworker to use.
1. **Identify the change you want investigated.** Specify the metric and time period. For a more focused analysis, include a comparison period, relevant dimensions or segments, and any hypothesis you want Coworker to test.

### Sample prompts for Adobe Analytics

Replace the bracketed text with component names and time periods from your report suite.

* In the **[report suite name]** report suite, why did **[metric]** change during **[date range]** compared with **[comparison date range]**? Break down the change by **[dimension]** and show the segments that contributed most.
* In the **[report suite name]** report suite, did **[dimension or segment]** contribute to the decrease in **[metric]** from **[date range A]** to **[date range B]**? Compare the values for both periods and explain what changed.
* In the **[report suite name]** report suite, compare **[metric]** for **[segment A]** and **[segment B]** during **[date range]**. Which dimensions contributed most to the difference?

## Related resources

* [Analyze data with Adobe CX Enterprise Coworker Chat](https://experienceleague.adobe.com/en/docs/coworker/content/chat/use-cases/data-insights/analytics-overview)
* [Get started analyzing data with Coworker Chat](https://experienceleague.adobe.com/en/docs/coworker/content/chat/use-cases/data-insights/analytics-chat)
