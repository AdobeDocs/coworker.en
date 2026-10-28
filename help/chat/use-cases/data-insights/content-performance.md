---
title: Analyze Content and Creative Performance with Coworker Chat
description: Use Coworker Chat to find what winning content has in common, attribute revenue to the images customers see, and compare creative across channels and audiences.
product_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: CX Enterprise Coworker
---

# Content performance overview

<!-- FLAG: Confidence: High for the first sentence and "Best for" (carried over from analytics-overview.md). Medium for the second sentence, which summarizes the row descriptions from the slides. -->

Use Adobe CX Enterprise Coworker Chat to understand which content wins and why, down to the attributes of each asset, so you can invest in what works. Go beyond which files got clicks to see which imagery, messaging, and themes drive engagement and revenue across channels and audiences.

Content performance is one of several analysis domains in Coworker Chat. To see all domains, see [Start analyzing in Coworker Chat](/help/chat/use-cases/data-insights/analytics-overview.md#start-analyzing-in-coworker-chat) in Analyze data with Coworker Chat.

**Best for:** Business user

## Prerequisites

<!-- FLAG: Confidence: High for the first two bullets (sourced from analytics-chat.md and the Skills and limitations table). High for the third bullet: attribute-level and asset analysis needs Content Analytics components, which are available only in data views that are configured for Content Analytics (report/report.md in analytics-platform.en). This applies whichever skill runs the analysis. It's a shared bullet rather than a table row because it applies to every use case on this page. The SME confirmed (October 2026) that the skill doesn't support paid media yet, so the paid channel use case was rewritten for web and mobile. Support is planned, either in this skill or in a separate add-on skill (not decided). When it ships, consider restoring paid channels to that row with an "Additional prerequisite" note: paid media needs the Paid Media channel enabled in Content Analytics through an Experience Platform paid media source connector, such as Meta Ads or Google Ads, and comparing paid creative with on-site revenue needs custom tracking-key mapping (config/paid-media.md in analytics-platform.en). -->

To use the use cases on this page, you need:

* Coworker Chat connected to your Customer Journey Analytics data views or Adobe Analytics report suites. See [Get started analyzing data with Coworker Chat](/help/chat/use-cases/data-insights/analytics-chat.md).
* View access to the data views or report suites that you want to analyze. Coworker Chat inherits your permissions from Customer Journey Analytics or Adobe Analytics.
* A data view that's configured for Content Analytics. See [Configure Content Analytics](https://experienceleague.adobe.com/en/docs/analytics-platform/using/content-analytics/configuration/configuration) in the Customer Journey Analytics guide.

## Use cases

| Use case | Function |
| --- | --- |
| Find what winning content has in common<p>![Find what winning content has in common](assets/content-performance.png)</p> | Shows which imagery and messaging work at the attribute level, not just which files got clicks.<p>**Sample prompts:**</p><ul><li>"What do our best-performing images have in common?"</li><li>"Which content attributes drive the most engagement?"</li></ul> |
| Attribute revenue to the content customers see | Ties image exposure to revenue, conversions, and engagement with algorithmic attribution.<p>**Best for:** Analyst, Business user</p><p>**Sample prompts:**</p><ul><li>"Which images drove the most revenue last quarter?"</li><li>"How much revenue is tied to the image at https://www.example.com/images/spring-sale.jpg?"</li></ul> |
| Compare creative across web and mobile | Shows which visuals and themes win on your site and in your mobile app in one view.<p>**Sample prompts:**</p><ul><li>"Which creative themes win in our mobile app and on our site?"</li><li>"Compare image performance in our mobile app and on our site"</li></ul> |
| Know which visuals move each audience | Shows which visuals work for each audience to guide personalization and creative briefs.<p>**Sample prompts:**</p><ul><li>"Which visuals perform best for each segment?"</li><li>"What imagery works for first-time visitors?"</li></ul> |

## Skills used

<!-- FLAG: Confidence: Medium. The `analyze-content` skill is a foundational skill for content questions, so it's listed for every use case on this page. Confirm with the PM that it covers all four. -->

Coworker uses the following skills for the use cases described in this article. For a list of all analytics skills, including the permissions they require and what they don't cover, see [Skills and limitations](/help/chat/use-cases/data-insights/analytics-overview.md#skills-and-limitations) in Analyze data with Coworker Chat.

| Skill | Used for |
| --- | --- |
| `cja`,`analyze-content` <br/> (Limited Availability)| Find what winning content has in common<br>Attribute revenue to the content customers see<br>Compare creative across web and mobile<br>Know which visuals move each audience<p>For more information, see [Ask questions about your content](/help/chat/use-cases/data-insights/ask-content-questions.md).</p> |

## Tips for better results

<!-- FLAG: Confidence: High for the first bullet (SME feedback, October 2026). Medium for the rest: the second and third bullets are adapted from the best practices in analytics-overview.md, and the fourth bullet is inferred from the row descriptions. -->

* When you ask about a specific image, include its URL or asset ID. Coworker can't identify an image by its role on the page, such as a hero image or a banner.
* Name the metric and date range you want to analyze, such as revenue last quarter.
* Specify the segments, audiences, or channels that you want compared.
* Ask about content attributes, such as imagery, themes, or messaging, rather than individual files when you want to know why content performs well.

## Next steps

* To learn how Coworker answers content questions, see [Ask questions about your content](/help/chat/use-cases/data-insights/ask-content-questions.md) (Limited Availability).
* For an overview of data analysis with Coworker Chat, including the other analysis domains and best practices, see [Analyze data with Coworker Chat](/help/chat/use-cases/data-insights/analytics-overview.md).
* To set up Coworker Chat and walk through a working example, see [Get started analyzing data with Coworker Chat](/help/chat/use-cases/data-insights/analytics-chat.md).
