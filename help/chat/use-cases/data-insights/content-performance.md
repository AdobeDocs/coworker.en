---
title: Analyze Content and Creative Performance with Coworker Chat
description: Use Coworker Chat to find what winning content has in common, attribute revenue to the images customers see, and compare creative across channels and audiences.
product_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: CX Enterprise Coworker
feature_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: CX Enterprise Coworker
---

# Content performance overview

<!-- FLAG: Confidence: High for the first sentence and "Best for" (carried over from analytics-overview.md). Medium for the second sentence, which summarizes the row descriptions from the slides. -->

Use Adobe CX Enterprise Coworker Chat to understand which content wins and why, down to the attributes of each asset, so you can invest in what works. Go beyond which files got clicks to see which imagery, messaging, and themes drive engagement and revenue across channels and audiences.

Content performance is one of several analysis domains in Coworker Chat. To see all domains, see [Start analyzing in Coworker Chat](/help/chat/use-cases/data-insights/analytics-overview.md#start-analyzing-in-coworker-chat) in Analyze data with Coworker Chat.

**Best for:** Business user

## Prerequisites

<!-- FLAG: Confidence: High for the first two bullets (sourced from analytics-chat.md and the Skills and limitations table). Low for the third bullet: the attribute-level and image exposure descriptions suggest that these use cases rely on Content Analytics data in Customer Journey Analytics, and implementation-guide.md lists Content Analytics as an implementation path, but no source confirms this. It's a shared bullet rather than a table row because it would apply to every use case on this page. The paid channel row ("Compare Meta ad creative to our web banners") may need an additional data source, which would become an "Additional prerequisite" note on that row in the Use cases table. Confirm with the PM. -->

To use the use cases on this page, you need:

* Coworker Chat connected to your Customer Journey Analytics data views or Adobe Analytics report suites. See [Get started analyzing data with Coworker Chat](/help/chat/use-cases/data-insights/analytics-chat.md).
* View access to the data views or report suites that you want to analyze. Coworker Chat inherits your permissions from Customer Journey Analytics or Adobe Analytics.
* Content Analytics set up in Customer Journey Analytics, so that Coworker Chat can analyze content attributes and image exposure. To plan a Content Analytics implementation, see [Plan your implementation with Coworker](/help/chat/use-cases/data-insights/implementation-guide.md).

## Use cases

| Use case | Function |
| --- | --- |
| Find what winning content has in common<p>![Find what winning content has in common](assets/content-performance.png)</p> | Shows which imagery and messaging work at the attribute level, not just which files got clicks.<p>**Sample prompts:**</p><ul><li>"What do our best-performing images have in common?"</li><li>"Which content attributes drive the most engagement?"</li></ul> |
| Attribute revenue to the content customers see | Ties image exposure to revenue, conversions, and engagement with algorithmic attribution.<p>**Best for:** Analyst, Business user</p><p>**Sample prompts:**</p><ul><li>"Which hero images drove the most revenue last quarter?"</li><li>"How much revenue is tied to this banner?"</li></ul> |
| Compare creative across paid and owned channels | Shows which visuals and themes win across web, mobile, and paid channels in one view.<p>**Sample prompts:**</p><ul><li>"Which creative themes win in paid and on our site?"</li><li>"Compare Meta ad creative to our web banners"</li></ul> |
| Know which visuals move each audience | Shows which visuals work for each audience to guide personalization and creative briefs.<p>**Sample prompts:**</p><ul><li>"Which visuals perform best for each segment?"</li><li>"What imagery works for first-time visitors?"</li></ul> |

<!--
HIDDEN until the skills are confirmed. To publish, remove this comment wrapper.

## Skills used

FLAG: Confidence: Low. No source in the repo (workflows.md, the Skills and limitations table, or any data insights article) names the skills behind these use cases. Get the skill IDs from the PM, replace the placeholder rows, and add the skills to the Skills and limitations table on analytics-overview.md so that the link above the table covers them. When you unhide this section, wrap this FLAG note in its own HTML comment.

Coworker uses the following skills for the use cases described in this article. For a list of all analytics skills, including the permissions they require and what they don't cover, see [Skills and limitations](/help/chat/use-cases/data-insights/analytics-overview.md#skills-and-limitations) in Analyze data with Coworker Chat.

| Skill | Used for |
| --- | --- |
| *[Skill to be confirmed]* | Find what winning content has in common<br>Attribute revenue to the content customers see<br>Compare creative across paid and owned channels<br>Know which visuals move each audience |

-->

## Tips for better results

<!-- FLAG: Confidence: Medium. The first two bullets are adapted from the best practices in analytics-overview.md. The third bullet is inferred from the row descriptions. -->

* Name the metric and date range you want to analyze, such as revenue last quarter.
* Specify the segments, audiences, or channels that you want compared.
* Ask about content attributes, such as imagery, themes, or messaging, rather than individual files when you want to know why content performs well.

## Next steps

* For an overview of data analysis with Coworker Chat, including the other analysis domains and best practices, see [Analyze data with Coworker Chat](/help/chat/use-cases/data-insights/analytics-overview.md).
* To set up Coworker Chat and walk through a working example, see [Get started analyzing data with Coworker Chat](/help/chat/use-cases/data-insights/analytics-chat.md).
