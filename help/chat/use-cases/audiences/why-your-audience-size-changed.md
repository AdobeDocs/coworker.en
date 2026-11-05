---
title: Analyze Adobe Experience Platform Audience Changes with CX Enterprise Coworker
description: Learn how CX Enterprise Coworker uses the Operational Stats and Causal Analysis skill to explain audience changes, identify likely causes, assess downstream impact, and recommend next steps.
feature: AI Tools
role: User
level: Beginner
doc-type: Feature Video
duration: 216
last-substantial-update: 20261105
jira: KT-22454
autotag-review: '2026-11-05T15:16:40.881Z'
TQID: 'https://experienceleague.adobe.com/mj3rSj7AxRsmhxipLJLR69bzfujK-eCVaXQMFlgg-NA'
product_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: Coworker
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
---

# Why did my Experience Platform audience size spike/drop?

Learn how [!DNL CX Enterprise Coworker] can help investigate unexpected changes to key [!DNL Adobe Experience Platform] objects using the Operational Stats and Causal Analysis skill.

## What you'll learn

In this video, you'll see how to use plain-language prompts in Coworker to investigate an unexpected increase in an Adobe Experience Platform audience before a campaign launch. The walkthrough shows how causal analysis can connect audience-size changes with operational data, rule out configuration changes, and surface likely explanations without waiting for an Engineering investigation.

>[!VIDEO](https://video.tv.adobe.com/v/3507342/?learn=on&enablevpops)

You'll learn how to:

- Run a cause analysis using the Operational Stats and Causal Analysis skill.
- Compare audience-size changes with changes in the sandbox's total profile count.
- Understand how audience qualification rules can cause newly ingested profiles to enter an audience automatically.
- Check pipeline and configuration activity to determine whether the audience setup changed.
- Use Coworker's suggested next steps to refine audience criteria and continue investigating the source of profile growth.
- Evaluate downstream impact by identifying dependent audiences, campaigns, destinations, and unpublished journeys.
- Identify what to validate before launch when an upstream audience change affects targeting.

## How the analysis works

The example follows an audience whose size changes unexpectedly over several days. Coworker analyzes the selected time window and compares possible causes. The analysis finds that the audience's daily changes align with growth in the sandbox's total profile population.

Because the audience includes profiles without a loyalty ID, newly ingested profiles that meet that condition can qualify automatically. Coworker also checks the pipeline and configuration history to help distinguish incoming-data changes from changes made to the audience setup.

## Assess downstream impact

Finding the cause is only part of the investigation. The video also demonstrates how to ask Coworker what the audience change affects downstream. Coworker examines dependent objects and highlights where the larger audience could influence future targeting, including related audiences and journeys.

This gives marketing operations teams a faster path from detecting an unexpected audience change to understanding its likely cause, potential impact, and the checks to make before launch.

## Key takeaway

CX Enterprise Coworker can help explain why important Adobe Experience Platform objects change over time by combining operational statistics, causal analysis, dependency information, and recommended follow-up actions in a conversational workflow.
