---
title: CX Enterprise Coworker in AI Platforms
description: Learn how to set up Adobe CX Enterprise Coworker in Microsoft Copilot, Claude, and ChatGPT to bring marketing insights into your everyday tools.
hide: true
index: false
product_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: CX Enterprise Coworker
feature_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: CX Enterprise Coworker
---

# CX Enterprise Coworker in AI Platforms

Marketers and business practitioners often lack direct access to Adobe products, so getting the insights, assets, and workflows they need for a campaign can take weeks or months. CX Enterprise Coworker in AI Platforms closes that gap by bringing Coworker directly into the AI tools you already use: [!DNL Microsoft 365 Copilot], [!DNL Claude], and [!DNL ChatGPT]. Ask questions in natural language and get insights and assets from Coworker in seconds, without switching tools or learning a new interface.

There's no additional cost to use Coworker in AI platforms. It's included in your CX Enterprise Coworker license, and usage draws from the same AI credits as other Coworker features. For more information, see [Adobe Experience Platform agent jobs and AI credits consumption](https://experienceleague.adobe.com/en/docs/cx-enterprise-ai/experience-cloud-ai/overview/ai-credit-consumption){target="_blank"}.

<!-- TODO: architecture diagram pending from engineering. KT page notes "to be provided on 8/28"; still outstanding as of 8/31. Insert here once received. -->

## Prerequisites {#prerequisites}

Before you can use Coworker in an AI platform, confirm you have the following.

* Adobe CX Enterprise Coworker provisioned for your organization, and your own access to it in Adobe.
* Adobe Experience Platform and at least one of Adobe Real-Time CDP, Adobe Journey Optimizer, or Adobe Customer Journey Analytics.
* [!DNL Microsoft 365 Copilot], [!DNL Claude], or [!DNL ChatGPT], depending on the platform you plan to use.

## Data access and permissions {#data-access-and-permissions}

Coworker in AI platforms reflects the same data and access level tied to your Adobe identity. What you can query and see matches what you're already entitled to in Experience Platform and its associated solutions. Coworker inherits those permissions, so no separate permissions setup is required for the AI platform integration. Coworker returns read-only insights and does not modify your customer data. Review any generated summaries and analyses before you use them to make business decisions.

<!-- Confirmed by PM (Siddhartha Srivastava) on 2026-09-02: this permissions model applies to all three platforms, since Coworker in AI platforms is the same underlying product regardless of which platform surfaces it. -->

## Key use cases {#key-use-cases}

Use Coworker in AI platforms to speed up common marketing workflows without leaving your everyday tools.

| Use case | Description |
| --- | --- |
| Plan and review campaigns | Plan campaigns, including partner campaign reviews and audience forecasting. Compare campaign performance over time and identify which touchpoints drive conversions. |
| Monitor journeys and campaign readiness | Review and monitor active campaigns, analyze customer journeys, and assess campaign readiness. Track journey performance and drop-offs to pinpoint opportunities for optimization. |
| Retrieve operational insights | Identify which audiences are largest or most engaged so you can prioritize where to focus your efforts, and track how your segments grow or shrink over time. |
| Optimize workflows and content | Optimize workflows and identify asset and content needs for CX campaigns. Generate visual reports on campaign performance without manually building queries or dashboards. |
| Collaborate and decide faster | Use suggested prompts to explore audiences, campaigns, and web traffic. Share insights with your team during planning meetings, and answer ad hoc questions in real time while reviewing plans or decks. |

<!-- Use case detail repurposed from help/agents/ama-ms.md (Adobe Marketing Agent for Microsoft 365 Copilot) per PM Siddhartha Srivastava, 2026-08-31 approval. Confirmed by PM on 2026-09-02 that these use cases apply to all three platforms, not just Microsoft 365 Copilot. -->

## Set up Coworker {#set-up-coworker}

Setup steps vary by platform. Select your platform below for instructions, then see [Example prompts](#example-prompts) to get started.

>[!BEGINTABS]

>[!TAB Microsoft 365 Copilot]

**Set up Coworker for your organization**

An administrator must complete these steps before end users can access Coworker in [!DNL Microsoft 365 Copilot].

1. In the [!DNL Microsoft 365 admin center], confirm that your tenant settings allow apps and agents built by external publishers.
1. Approve Coworker, which appears as an agent, in both the [!DNL Microsoft 365 admin center] and the [!DNL Teams admin center]. You can typically find it through the [!DNL Microsoft Commercial Marketplace] or your organization's [!DNL Integrated Apps] list.
1. Deploy the agent to end users. You can deploy it to specific users or groups, or to your entire organization. The number of users you enable does not affect setup or cost.

>[!NOTE]
>
>If [!DNL Microsoft] releases an update to Coworker that requires new permissions, your administrator must approve the update in the [!DNL Agent Registry] before it rolls out to your users.

**Access Coworker in [!DNL Copilot]**

Once your administrator enables Coworker, you can access it across [!DNL Microsoft 365 Copilot] surfaces, including [!DNL Teams], [!DNL Word], [!DNL Excel], [!DNL PowerPoint], and web chat.

1. Find Coworker in your list of agents, or search for **CX Enterprise Coworker** in the [!DNL Microsoft 365 Copilot Agent Store].
1. Select **[!UICONTROL Add]**, then open the agent.
1. Sign in using your Adobe credentials. Copy the code that Coworker provides and paste it into the Adobe sign-in flow.

<!-- TODO: screenshot placeholder for step 1 above. File: ./assets/copilot-agent-store.png. Alt text: "Adobe CX Enterprise Coworker agent card in the Microsoft 365 Copilot Agent Store, with the Add button visible." As of 2026-09-02, PM confirmed the live catalog still shows the predecessor product name ("Adobe Marketing Agent"), not "CX Enterprise Coworker" -- wait to capture until the UI is rebranded, or capture and swap later. Once captured, replace this comment with: ![Adobe CX Enterprise Coworker agent card in the Microsoft 365 Copilot Agent Store, with the Add button visible.](./assets/copilot-agent-store.png) -->

>[!TAB Claude]

<!-- PUBLISHING NOTE: as of 2026-09-02, Coworker for Claude is still pending approval on Anthropic's side. PM (Siddhartha Srivastava) is following up. Do NOT publish this tab until approval comes through and these steps are confirmed against the live product. -->

**Set up Coworker for your organization**

1. Ask your [!DNL Claude] administrator to approve the CX Enterprise Coworker connector for select users or for your entire organization.

**Access Coworker in [!DNL Claude]**

1. Find Coworker listed as a connector in the [!DNL Claude] MCP Connector Catalog and select **[!UICONTROL Add]**.
1. Sign in with your Adobe credentials, then start prompting.

<!-- TODO: screenshot placeholder for step 1 above. File: ./assets/claude-connector-catalog.png. Alt text: "CX Enterprise Coworker listed as a connector in the Claude MCP Connector Catalog." Cannot capture until the connector is approved for Claude (pending as of 2026-09-02). Once captured, replace this comment with: ![CX Enterprise Coworker listed as a connector in the Claude MCP Connector Catalog.](./assets/claude-connector-catalog.png) -->

>[!TAB ChatGPT]

**Set up Coworker for your organization**

1. Ask your [!DNL ChatGPT] administrator to approve the CX Enterprise Coworker plugin for select users or for your entire organization.

**Access Coworker in [!DNL ChatGPT]**

1. Find Coworker listed as a plugin in the [!DNL ChatGPT] plugin catalog and select **[!UICONTROL Add]**.
1. Sign in with your Adobe credentials, then start prompting.

<!-- TODO: screenshot placeholder for step 1 above. File: ./assets/chatgpt-plugin-catalog.png. Alt text: "CX Enterprise Coworker listed as a plugin in the ChatGPT plugin catalog." As of 2026-09-02, PM confirmed the live catalog still shows the predecessor product name ("Adobe Marketing Agent"), not "CX Enterprise Coworker" -- wait to capture until the UI is rebranded, or capture and swap later. Once captured, replace this comment with: ![CX Enterprise Coworker listed as a plugin in the ChatGPT plugin catalog.](./assets/chatgpt-plugin-catalog.png) -->

>[!ENDTABS]

<!-- Setup steps above reflect the real customer-facing flow confirmed by PM (Siddhartha Srivastava) on 2026-09-02: an org admin approves the connector or plugin, then end users find and add it in their platform's catalog and sign in. The previous version of this file described a manual MCP-connector setup for ChatGPT (Settings > Connectors > paste server URL) -- PM clarified that flow is for internal testing only, not the customer path, so it was removed here. -->

## Example prompts {#example-prompts}

After you set up Coworker in your AI platform of choice, try one of these prompts, or write your own in natural language. The same prompts work across [!DNL Microsoft 365 Copilot], [!DNL Claude], and [!DNL ChatGPT].

* Show your top five audiences.
* Show a metric for the last month.
* Show your active Workfront projects.
* Show journeys with loyalty audiences.

## Known limitations {#known-limitations}

Coworker in AI platforms does not support every integration pattern.

* You cannot connect Coworker to your own agentic harness using MCP.

## Troubleshoot Coworker in AI platforms {#troubleshoot}

Try these steps if you run into issues using Coworker in an AI platform.

* If you see an error, sign out and sign in again with your Adobe credentials. Re-authenticating resolves most issues.
* If you cannot access Coworker or specific data, contact your Adobe administrator to confirm your product access and permissions.
