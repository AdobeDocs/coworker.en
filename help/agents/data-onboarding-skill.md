---
title: Onboard Data with Coworker
description: Learn how to use the Data Onboarding Skill in CX Coworker to onboard new data sources into Adobe Experience Platform through a conversational workflow.
hide: true
---

# Onboard data with Coworker

>[!AVAILABILITY]
>
>The Data Onboarding Skill is in beta. The documentation and the functionality are subject to change.
>
>The Data Onboarding Skill is available to customers with access to Adobe CX Enterprise Coworker, where it must also be enabled for your organization. <!-- VERIFY BEFORE PUBLISH: confirm exact permission/entitlement name with Umesh Gohil, PLAT-296546. -->

Use the Data Onboarding Skill in CX Coworker to onboard new data into Adobe Experience Platform through a single conversational workflow. Instead of navigating multiple screens to connect a source and build a schema by hand, describe your intent and Coworker guides you through source selection, data quality, semantic enrichment, schema mapping, schema creation, and dataflow creation.

<!-- VERIFY BEFORE PUBLISH: confirm the loaded skill name ("Onboard Data to Experience Platform") and the exact post-landing prompt/flow with Umesh Gohil once flag access is arranged. -->

## Prerequisites {#prerequisites}

Before you begin, ensure that you have:

- Access to Adobe Experience Platform and the appropriate organization and sandbox.
- Access to Adobe CX Enterprise Coworker, with the Data Onboarding Skill enabled for your organization.
- Permission to create schemas in Adobe Experience Platform.

For instructions on installing plugins, see the [Coworker UI guide](https://experienceleague.adobe.com/en/docs/cx-enterprise-ai/experience-cloud-ai/coworker/chat/ui-guide).

## Use the Data Onboarding Skill {#use-the-data-onboarding-skill}

Today, the Data Onboarding Skill starts from schema creation in the Experience Platform UI, which opens Coworker with your intent already filled in.

To use the Data Onboarding Skill:

1. In Adobe Experience Platform, navigate to **[!UICONTROL Schemas]**, then select **[!UICONTROL Create schema]**.
1. In the **[!UICONTROL Create a schema]** dialog, select **[!UICONTROL Onboard data with AI]**, then select **[!UICONTROL Select]**.

   ![The Create a schema dialog with the Onboard data with AI option selected.](./assets/data-onboarding-skill/create-a-schema-dialog.png)

1. CX Coworker opens in a new browser tab with a prompt pre-populated from your schema-creation intent, so you do not need to restate it.
1. Choose a source to onboard from when prompted, for example [!DNL Amazon S3], [!DNL Data Landing Zone], [!DNL Delta Share], or [!DNL Marketo].

   <!-- VERIFY BEFORE PUBLISH: screenshot of the Coworker landing/session-start state does not exist yet anywhere. Capture once flag access is confirmed. -->

1. Continue the conversation with Coworker through data quality review, semantic enrichment, schema mapping, and schema creation, confirming each step as you go.

For more information about using CX Coworker, see the [Coworker UI guide](https://experienceleague.adobe.com/en/docs/cx-enterprise-ai/experience-cloud-ai/coworker/chat/ui-guide).

## Supported use cases {#supported-use-cases}

Explore the parts of the onboarding workflow the Data Onboarding Skill helps you complete.

### Select and connect a source

Instead of manually locating and configuring a source connector, describe the data you want to bring in and let Coworker help identify the right source.

### Review data quality

Coworker surfaces data quality signals for the selected source before you commit to a schema, so you can catch issues earlier in the process.

### Enrich data semantically

Coworker suggests semantic meaning for incoming fields, reducing the manual work of mapping raw fields to standard definitions.

### Map and create a schema

Coworker maps reviewed fields to a new or existing schema and creates it directly in Adobe Experience Platform as part of the same conversation.

### Create a dataflow

Coworker completes onboarding by creating the dataflow needed to bring the data in on an ongoing basis.

## Next steps {#next-steps}

After reading this guide, you should understand how to start the Data Onboarding Skill from schema creation and what it helps you accomplish in CX Coworker.

For the Experience Platform UI procedure and access/eligibility scenarios, see [Onboard data with AI](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/ui/resources/schemas#data-onboarding-skill) in the schemas UI guide.
