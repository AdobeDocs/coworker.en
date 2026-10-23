---
title: Ask Questions About Your Content with Coworker Chat
description: Ask Coworker Chat about your content in plain language, from general to specific, and get accurate Content Analytics answers without analyst expertise.
product_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: CX Enterprise Coworker
---

# Ask questions about your content

<!-- FLAG: Confirm with the PM: (1) availability (GA, beta, or experimental) and whether this page needs an AVAILABILITY note or `hide: true` until launch, and (2) any required Coworker entitlement. Content Analytics itself has no separate permission: users get access through data views that are configured for Content Analytics (Access control section of analytics-platform.en/help/content-analytics/config/configuration.md). -->

Use Adobe CX Enterprise Coworker Chat to get accurate answers about your content from Adobe Content Analytics. Ask a specific question, such as "Which hero images drove the most revenue last quarter?", or a general one, such as "What kind of content should I prioritize?". Coworker turns your question into a sound analysis.

Coworker understands how Content Analytics data is structured and applies the reporting rules that an experienced analyst would, so marketers and other business users get reliable results without deep Content Analytics expertise.

For other content performance use cases, see [Content performance overview](/help/chat/use-cases/data-insights/content-performance.md).

**Best for:** Business user, Analyst

## Prerequisites

<!-- FLAG: Confidence: High. The first two bullets match the other data insights pages. The third bullet follows the Content Analytics docs in analytics-platform.en: Content Analytics components are available only in data views that are configured for Content Analytics (report/report.md), and there's no separate Content Analytics permission (config/configuration.md). -->

To ask questions about your content, you need:

* Coworker Chat connected to your Customer Journey Analytics data views. See [Get started analyzing data with Coworker Chat](/help/chat/use-cases/data-insights/analytics-chat.md).
* View access to the data views that you want to analyze. Coworker Chat inherits your permissions from Customer Journey Analytics.
* A data view that's configured for Content Analytics. See [Configure Content Analytics](https://experienceleague.adobe.com/en/docs/analytics-platform/using/content-analytics/configuration/configuration) in the Customer Journey Analytics guide.

## Ask a content question

1. Sign in to Coworker.

1. Select **[!UICONTROL New chat]**.

1. In the text field, ask a question about your content. For example:

   **Prompt**

   > What kind of content should I prioritize?

   <!-- FLAG: The skill includes activation words and phrases, but they weren't provided. Confirm with the PM whether customers need to use specific words to trigger the skill, or whether any content question routes to it automatically. If specific words are needed, list them here. -->

   Coworker uses the `analyze-content` skill to answer content questions.

1. (Conditional) If your question is open to more than one interpretation, answer the clarifying questions that Coworker asks, such as which content type, channel, or date range you mean.

1. Review the results. 

1. (Optional) Ask follow-up questions in the same conversation to go deeper, or open a visualization in Analysis Workspace for more manual control. See [Analyze in Customer Journey Analytics](/help/chat/use-cases/data-insights/analytics-chat.md#analyze-in-customer-journey-analytics).

## Example prompts

The following table shows example prompts for different types of content questions. Use them as a starting point and adapt them to your own content.

| Type of question | Example prompts |
| --- | --- |
| Broad or exploratory | <ul><li>"What kind of content should I prioritize?"</li><li>"How is our content performing?"</li></ul> |
| Attribute-level | <ul><li>"What do our best-performing images have in common?"</li><li>"Which content attributes drive the most engagement?"</li></ul> |
| Revenue and conversions | <ul><li>"Which hero images drove the most revenue last quarter?"</li><li>"How much revenue is tied to this banner?"</li></ul> |
| Channels and audiences | <ul><li>"Which creative themes win in paid and on our site?"</li><li>"What imagery works for first-time visitors?"</li></ul> |

## How Coworker answers content questions

<!-- FLAG: Confidence: High for the list of what the skill includes, metric matching, filtering pages by Experience ID, and choosing an attribution model per question (sourced from the PM's skill description and feature summary). Medium for the remaining details, which combine the skill description with the Content Analytics component reference in the Customer Journey Analytics guide. The skill's specific query defaults, attribution models, and visualization rules weren't provided. Confirm with the PM before adding them. -->

Coworker answers content questions with the `analyze-content` skill, which includes the following context and guardrails. The skill pairs with the `cja` skill and runs all queries against your Customer Journey Analytics data views through the same Customer Journey Analytics tools.

### Query defaults and clarifying questions

If your question leaves out a detail, the skill applies a sensible default. If the skill is unsure what you mean, it asks a clarifying question instead of guessing.

### Metric matching for assets and experiences

<!-- FLAG: The table covers web and mobile content. Paid media content uses separate summary metrics, such as Impressions, Clicks, and Spend with a reporting-level suffix (for example, Clicks | Asset Summary), that can't be combined with event metrics such as Asset Views (config/paid-media.md in analytics-platform.en). Confirm with the PM how the skill handles paid media, then add a row or note. -->

Content Analytics tracks two types of content: assets and experiences. Each has its own metrics. The skill always pairs the metric with the type of content that you ask about.

| Content type | What it is | Metrics the skill uses |
| --- | --- | --- |
| Assets | An individual piece of content, such as an image | Asset Views, Asset Clicks, Asset Click-Through Rate (CTR) |
| Experiences | All the text on a web page, or the combination of text, assets, and calls to action in a mobile app | Experience Views, Experience Clicks, Experience Click-Through Rate (CTR) |

### Content Analytics data architecture

The skill understands how Content Analytics data is structured. For example:

* **Experience IDs:** When you ask about a specific page, the skill filters by the Content Experience ID that identifies that page.
* **AI-generated attributes:** Each asset and experience is described by attributes such as photography style, colors, tone, and persuasion strategy. The skill uses these attributes to explain why content performs well, not just which content performs well.

For the full list of components, see [Content Analytics components](https://experienceleague.adobe.com/en/docs/analytics-platform/using/content-analytics/report/components) in the Customer Journey Analytics guide.

### Attribution

The skill chooses the attribution model that fits your question. For example, a question about clicks on an image is answered differently from a question about how much revenue that image contributed to. For more information, see [Attribution models](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/attribution/models#attribution-models) in the Customer Journey Analytics guide.

### Common analyses and workflows

The skill includes instructions for common content analyses, such as:

* Finding the attributes that top-performing assets or experiences have in common.
* Tying content exposure to conversions and revenue.
* Comparing content across web, mobile, and paid media channels.
* Comparing which content works for different audiences and segments.
* Identifying content that's overused or underused.

### Visualizations

The skill selects visualizations that fit your question and the data, so that results are easy to read and share.

## Tips for better results

* Start broad if you're not sure what to ask. Coworker can turn a general question into a focused analysis, and you can refine from there.
* Say whether you mean individual assets, such as images, or whole experiences, such as pages, when you know which one you want.
* Name the metric and date range you want to analyze, such as revenue last quarter.
* Specify the segments, audiences, or channels that you want compared.
* Ask about content attributes, such as imagery, themes, or messaging, rather than individual files when you want to know why content performs well.
* Add your preferred data view to Coworker Chat memory if you always analyze the same one. See [Add a data view or report suite preference in Memory](/help/chat/use-cases/data-insights/analytics-chat.md#add-a-data-view-or-report-suite-preference-in-memory).

## Next steps

* For more content performance use cases, see [Content performance overview](/help/chat/use-cases/data-insights/content-performance.md).
* To learn more about Content Analytics, see [Content Analytics overview](https://experienceleague.adobe.com/en/docs/analytics-platform/using/content-analytics/content-analytics) in the Customer Journey Analytics guide.
* For an overview of data analysis with Coworker Chat, including best practices, see [Analyze data with Coworker Chat](/help/chat/use-cases/data-insights/analytics-overview.md).
