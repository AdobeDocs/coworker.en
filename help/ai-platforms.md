---
title: Adobe CX Enterprise Coworker for AI Platforms
description: Learn about Adobe CX Enterprise Coworker for AI Platforms, including Copilot, ChatGPT, Claude, and Gemini. Explore marketing insights and platform setup guidance.
hide: true
index: false
product_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: CX Enterprise Coworker
feature_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: CX Enterprise Coworker
---

# Adobe CX Enterprise Coworker for AI Platforms

Use [!DNL Adobe CX Enterprise Coworker for AI Platforms] to get marketing insights in the AI tools you already use. Ask questions in natural language without switching tools. Find the product listed as [!DNL Adobe CX Enterprise Coworker] in each platform.

Use the setup guidance for [!DNL Microsoft 365 Copilot] and [!DNL ChatGPT]. Setup guidance for [!DNL Claude] and [!DNL Gemini] is pending approval and validation.

<!-- Editorial update, 2026-10-14, from PM Siddhartha Srivastava: Copilot and ChatGPT listings are complete. Claude approval is expected by Friday, October 16, but is not confirmed. Access is expected after approval. Gemini approval is also pending. Include Gemini in this hidden draft, but do not write setup steps until the customer flow is confirmed. PM review is expected today, not complete. Keep publication gates until review and publication approval are complete. Databricks Genie, Amazon Quick, and IBM WatsonX remain outside this draft's scope. -->

There's no additional cost to use Coworker in AI platforms. It's included in your CX Enterprise Coworker license, and usage draws from the same AI credits as other Coworker features. For more information, see [Adobe Experience Platform agent jobs and AI credits consumption](https://experienceleague.adobe.com/en/docs/cx-enterprise-ai/experience-cloud-ai/overview/ai-credit-consumption){target="_blank"}.

<!-- TODO: architecture diagram pending from engineering. KT page notes "to be provided on 8/28"; still outstanding as of 8/31. Insert here once received. -->

## Prerequisites {#prerequisites}

Before you can use Coworker in an AI platform, confirm you have the following.

* Adobe CX Enterprise Coworker provisioned for your organization, and your own access to it in Adobe.
* Adobe Experience Platform and at least one of Adobe Real-Time CDP, Adobe Journey Optimizer, or Adobe Customer Journey Analytics.
* [!DNL Microsoft 365 Copilot] or [!DNL ChatGPT], depending on the platform you plan to use.

<!-- Add Claude and Gemini prerequisites after approval, access, and any platform-specific requirements are confirmed. -->

## Data access and permissions {#data-access-and-permissions}

Coworker in AI platforms reflects the same data and access level tied to your Adobe identity. What you can query and see matches what you're already entitled to in Experience Platform and its associated solutions. Coworker inherits those permissions, so no separate permissions setup is required for the AI platform integration. Coworker returns read-only insights and does not modify your customer data. Review any generated summaries and analyses before you use them to make business decisions.

<!-- Confirmed by PM (Siddhartha Srivastava) on 2026-09-02: this permissions model applies to Microsoft 365 Copilot, Claude, and ChatGPT, since Coworker in AI platforms is the same underlying product regardless of which platform surfaces it. Gemini was added to the draft scope on 2026-10-14. Confirm that this model also applies to Gemini before publication. -->

## Key use cases {#key-use-cases}

Use Coworker in AI platforms to speed up common marketing workflows without leaving your everyday tools.

| Use case | Description |
| --- | --- |
| Plan and review campaigns | Plan campaigns, including partner campaign reviews and audience forecasting. Compare campaign performance over time and identify which touchpoints drive conversions. |
| Monitor journeys and campaign readiness | Review and monitor active campaigns, analyze customer journeys, and assess campaign readiness. Track journey performance and drop-offs to pinpoint opportunities for optimization. |
| Retrieve operational insights | Identify which audiences are largest or most engaged so you can prioritize where to focus your efforts, and track how your segments grow or shrink over time. |
| Optimize workflows and content | Optimize workflows and identify asset and content needs for CX campaigns. Generate visual reports on campaign performance without manually building queries or dashboards. |
| Collaborate and decide faster | Use suggested prompts to explore audiences, campaigns, and web traffic. Share insights with your team during planning meetings, and answer ad hoc questions in real time while reviewing plans or decks. |

<!-- Use case detail repurposed from help/agents/ama-ms.md (Adobe Marketing Agent for Microsoft 365 Copilot) per PM Siddhartha Srivastava, 2026-08-31 approval. Confirmed by PM on 2026-09-02 that these use cases apply to Microsoft 365 Copilot, Claude, and ChatGPT. Confirm applicability to Gemini before publication. -->

## Set up Coworker {#set-up-coworker}

Setup steps vary by platform. Select your platform for setup guidance and approval status, then review the [example prompts](#example-prompts).

>[!BEGINTABS]

>[!TAB Microsoft 365 Copilot]

Use [!DNL Adobe CX Enterprise Coworker for Copilot] to get marketing insights in [!DNL Microsoft 365 Copilot].

**Set up Coworker for your organization**

An administrator must complete these steps before end users can access Coworker in [!DNL Microsoft 365 Copilot].

1. In the [!DNL Microsoft 365 admin center], confirm that your tenant settings allow apps and agents built by external publishers.
1. Approve **[!UICONTROL Adobe CX Enterprise Coworker]** in both the [!DNL Microsoft 365 admin center] and the [!DNL Teams admin center]. You can typically find the agent through the [!DNL Microsoft Commercial Marketplace] or your organization's **[!UICONTROL Integrated Apps]** list.
1. Deploy the agent to end users. You can deploy it to specific users or groups, or to your entire organization. The number of users you enable does not affect setup or cost.

>[!NOTE]
>
>If [!DNL Microsoft] releases an update to Coworker that requires new permissions, your administrator must approve the update in the [!DNL Agent Registry] before it rolls out to your users.

**Access Coworker in [!DNL Copilot]**

Once your administrator enables Coworker, you can access it across [!DNL Microsoft 365 Copilot] surfaces, including [!DNL Teams], [!DNL Word], [!DNL Excel], [!DNL PowerPoint], and web chat.

1. Find **[!UICONTROL Adobe CX Enterprise Coworker]** in your list of agents, or search in the [!DNL Microsoft 365 Copilot Agent Store].
1. Select **[!UICONTROL Add]**, then open the agent.
1. Sign in using your Adobe credentials. Copy the code that Coworker provides and paste it into the Adobe sign-in flow.

<!-- Visual follow-up, 2026-10-14: PM confirmed the Copilot listing is complete and the intended catalog name is Adobe CX Enterprise Coworker. Verify the displayed name during the live walkthrough. Follow the documentation image policy: link to platform documentation for third-party UI rather than capturing catalog screenshots. -->

>[!TAB Claude]

This tab covers [!DNL Adobe CX Enterprise Coworker for Claude].

>[!AVAILABILITY]
>
>Approval for [!DNL Claude] is pending. Setup instructions remain a draft and require validation before publication.

<!-- PUBLISHING NOTE, updated 2026-10-14: PM expects Anthropic approval by Friday, October 16, and access after approval. Neither approval nor access is confirmed. Do not publish this tab until approval is confirmed and these steps are validated against the live product. -->

**Set up Coworker for your organization**

* Ask your [!DNL Claude] administrator to approve **[!UICONTROL Adobe CX Enterprise Coworker]** for selected users or your entire organization.

**Access Coworker in [!DNL Claude]**

1. Find **[!UICONTROL Adobe CX Enterprise Coworker]** in the [!DNL Claude] MCP Connector Catalog and select **[!UICONTROL Add]**.
1. Sign in with your Adobe credentials, then start prompting.

<!-- Visual follow-up, 2026-10-14: Verify the Adobe CX Enterprise Coworker listing and customer flow after Claude approval and access are confirmed. Link to platform documentation for third-party UI rather than capturing catalog screenshots. -->

>[!TAB ChatGPT]

Use [!DNL Adobe CX Enterprise Coworker for ChatGPT] to get marketing insights in [!DNL ChatGPT].

**Set up Coworker for your organization**

* Ask your [!DNL ChatGPT] administrator to approve **[!UICONTROL Adobe CX Enterprise Coworker]** for selected users or your entire organization.

**Access Coworker in [!DNL ChatGPT]**

1. Find **[!UICONTROL Adobe CX Enterprise Coworker]** in the [!DNL ChatGPT] plugin catalog and select **[!UICONTROL Add]**.
1. Sign in with your Adobe credentials, then start prompting.

<!-- Visual follow-up, 2026-10-14: PM confirmed the ChatGPT listing is complete and the intended catalog name is Adobe CX Enterprise Coworker. Verify the displayed name and current catalog terminology during the live walkthrough. Link to platform documentation for third-party UI rather than capturing catalog screenshots. -->

>[!TAB Gemini]

This tab covers [!DNL Adobe CX Enterprise Coworker for Gemini].

>[!AVAILABILITY]
>
>Approval for [!DNL Gemini] is pending. Setup instructions will be added after approval and validation.

<!-- Setup placeholder, 2026-10-14: Confirm Gemini approval and obtain access. Validate organization approval, catalog discovery, the Adobe CX Enterprise Coworker listing name, sign-in, permissions, supported use cases, and example prompts before adding customer instructions. Do not infer the flow from another platform. Link to platform documentation for third-party UI. -->

>[!ENDTABS]

<!-- Setup steps above reflect the real customer-facing flow confirmed by PM (Siddhartha Srivastava) on 2026-09-02: an org admin approves the connector or plugin, then end users find and add it in their platform's catalog and sign in. The previous version of this file described a manual MCP-connector setup for ChatGPT (Settings > Connectors > paste server URL) -- PM clarified that flow is for internal testing only, not the customer path, so it was removed here. -->

## Example prompts {#example-prompts}

After you set up Coworker, try one of these prompts, or write your own in natural language. These prompts apply to [!DNL Microsoft 365 Copilot], [!DNL Claude], and [!DNL ChatGPT]. Confirm [!DNL Claude] availability before you begin.

<!-- Gemini prompt support has not been confirmed. Validate these examples before extending the shared prompt statement to Gemini. -->

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
