---
title: Adobe CX Enterprise Coworker for AI Platforms
description: Learn about Adobe CX Enterprise Coworker for AI Platforms. Explore supported platforms, setup instructions, and example prompts to get marketing insights.
product_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: Coworker
---

# Adobe CX Enterprise Coworker for AI Platforms

Use Adobe CX Enterprise Coworker for AI Platforms to get marketing insights in the AI tools you already use. Ask questions in natural language without switching tools. Find the product listed as Adobe CX Enterprise Coworker in each platform.

Find available platforms and their setup instructions in [Set up Coworker](#set-up-coworker).

There's no additional cost to use Coworker in AI platforms. It's included in your CX Enterprise Coworker license, and usage draws from the same AI credits as other Coworker features. For more information, see [Adobe Experience Platform agent jobs and AI credits consumption](https://experienceleague.adobe.com/en/docs/cx-enterprise-ai/experience-cloud-ai/overview/ai-credit-consumption){target="_blank"}.

<!-- TODO: architecture diagram pending from engineering. KT page notes "to be provided on 8/28"; still outstanding as of 8/31. Insert here once received. -->

## Prerequisites {#prerequisites}

Before you can use Coworker in an AI platform, confirm you have the following.

* Adobe CX Enterprise Coworker provisioned for your organization, and your own access to it in Adobe.
* Adobe Experience Platform and at least one of Adobe Real-Time CDP, Adobe Journey Optimizer, or Adobe Customer Journey Analytics.
* Access to an AI platform listed in [Set up Coworker](#set-up-coworker).

## Data access and permissions {#data-access-and-permissions}

Coworker in AI platforms reflects the same data and access level tied to your Adobe identity. What you can query and see matches what you're already entitled to in Experience Platform and its associated solutions. Coworker inherits those permissions, so no separate permissions setup is required for the AI platform integration. Coworker returns read-only insights and does not modify your customer data. Review any generated summaries and analyses before you use them to make business decisions.

<!-- Confirmed by PM (Siddhartha Srivastava) on 2026-09-02 for Microsoft 365 Copilot, Claude, and ChatGPT. Validate this permissions model for each additional platform before adding its setup section. -->

## Key use cases {#key-use-cases}

Use Coworker in AI platforms to speed up common marketing workflows without leaving your everyday tools.

| Use case | Description |
| --- | --- |
| Plan and review campaigns | Plan campaigns, including partner campaign reviews and audience forecasting. Compare campaign performance over time and identify which touchpoints drive conversions. |
| Monitor journeys and campaign readiness | Review and monitor active campaigns, analyze customer journeys, and assess campaign readiness. Track journey performance and drop-offs to pinpoint opportunities for optimization. |
| Retrieve operational insights | Identify which audiences are largest or most engaged so you can prioritize where to focus your efforts, and track how your segments grow or shrink over time. |
| Optimize workflows and content | Optimize workflows and identify asset and content needs for CX campaigns. Generate visual reports on campaign performance without manually building queries or dashboards. |
| Collaborate and decide faster | Use suggested prompts to explore audiences, campaigns, and web traffic. Share insights with your team during planning meetings, and answer ad hoc questions in real time while reviewing plans or decks. |

<!-- Use cases approved by PM Siddhartha Srivastava on 2026-08-31 and confirmed for Microsoft 365 Copilot, Claude, and ChatGPT on 2026-09-02. Validate applicability for each additional platform before adding its setup section. -->

## Set up Coworker {#set-up-coworker}

Select an available platform for setup instructions. After setup, try the [example prompts](#example-prompts).

* [Microsoft 365 Copilot](#microsoft-365-copilot)
* [ChatGPT](#chatgpt)
* [Claude](#claude)
* [Gemini Enterprise](#gemini-enterprise)
* [Amazon Quick](#amazon-quick)
* [IBM watsonx Orchestrate](#ibm-watsonx-orchestrate)
* [Databricks](#databricks)

### [!DNL Microsoft 365 Copilot] {#microsoft-365-copilot}

Use [!DNL Adobe CX Enterprise Coworker for Copilot] to get marketing insights in [!DNL Microsoft 365 Copilot].

Before you begin, confirm you have access to [!DNL Microsoft 365 Copilot].

#### Set up organization access {#copilot-organization-setup}

An administrator must complete these steps before end users can access Coworker in [!DNL Microsoft 365 Copilot].

1. In the [!DNL Microsoft 365 admin center], confirm that your tenant settings allow apps and agents built by external publishers.
1. Approve **[!UICONTROL Adobe CX Enterprise Coworker]** in both the [!DNL Microsoft 365 admin center] and the [!DNL Teams admin center]. You can typically find the agent through the [!DNL Microsoft Commercial Marketplace] or your organization's **[!UICONTROL Integrated Apps]** list.
1. Deploy the agent to end users. You can deploy it to specific users or groups, or to your entire organization. The number of users you enable does not affect setup or cost.

>[!NOTE]
>
>If [!DNL Microsoft] releases an update to Coworker that requires new permissions, your administrator must approve the update in the [!DNL Agent Registry] before it rolls out to your users.

#### Access Coworker {#copilot-access}

Once your administrator enables Coworker, you can access it across [!DNL Microsoft 365 Copilot] surfaces, including [!DNL Teams], [!DNL Word], [!DNL Excel], [!DNL PowerPoint], and web chat.

In [!DNL Microsoft 365 Copilot], select **[!UICONTROL Agents]**, then select **[!UICONTROL More agents]**.

![Microsoft 365 Copilot with the Agents menu open and More agents highlighted.](./assets/ai-platforms/copilot/copilot-agents.png)

Next, select **[!UICONTROL Adobe CX Enterprise Coworker]** in the agent catalog.

![Microsoft 365 Copilot agent catalog with the Adobe CX Enterprise Coworker listing highlighted.](./assets/ai-platforms/copilot/copilot-select-agent.png)

Finally, select **[!UICONTROL Add]** to add Coworker to your agents.

![Adobe CX Enterprise Coworker details in Microsoft 365 Copilot with the Add button highlighted.](./assets/ai-platforms/copilot/copilot-add-coworker.png)

### [!DNL ChatGPT] {#chatgpt}

Use [!DNL Adobe CX Enterprise Coworker for ChatGPT] to get marketing insights in [!DNL ChatGPT].

Before you begin, confirm you have access to [!DNL ChatGPT].

#### Set up organization access {#chatgpt-organization-setup}

Your administrator must approve Coworker before you add it.

* Ask your [!DNL ChatGPT] administrator to approve **[!UICONTROL Adobe CX Enterprise Coworker]** for selected users or your entire organization.

#### Access Coworker {#chatgpt-access}

In [!DNL ChatGPT], select **[!UICONTROL Plugins]**.

![ChatGPT navigation with Plugins highlighted.](./assets/ai-platforms/chatgpt/gpt-plugins.png)

Next, find and select **[!UICONTROL Adobe CX Enterprise Coworker]** in the plugin catalog.

![ChatGPT plugin catalog with the Adobe CX Enterprise Coworker listing highlighted among the search results for Adobe.](./assets/ai-platforms/chatgpt/gpt-select-plugins.png)

Finally, select **[!UICONTROL Install plugin]** to add Coworker to [!DNL ChatGPT].

![Adobe CX Enterprise Coworker details in ChatGPT with the Install plugin button highlighted.](./assets/ai-platforms/chatgpt/gpt-install-coworker.png)

### [!DNL Claude] {#claude}

Use Coworker to get marketing insights in [!DNL Claude].

Before you begin, confirm you have access to [!DNL Claude].

#### Set up organization access {#claude-organization-setup}

Your administrator must approve Coworker before you add it.

* Ask your [!DNL Claude] administrator to approve **[!UICONTROL Adobe CX Enterprise Coworker]** for selected users or your entire organization.

#### Access Coworker {#claude-access}

1. In [!DNL Claude], select **[!UICONTROL Customize]**.

   ![Claude navigation with Customize highlighted.](./assets/ai-platforms/claude/claude-customize.png)

1. Select **[!UICONTROL Connectors]**, then **[!UICONTROL Discover]**, and use **[!UICONTROL Search]** to find Adobe CX Enterprise Coworker.

   ![Claude Customize page with the Connectors tab highlighted and the Discover catalog open.](./assets/ai-platforms/claude/claude-connectors.png)

1. Select **[!UICONTROL Adobe CX Enterprise Coworker]**, then select **[!UICONTROL Connect to Claude]**.

   ![Adobe CX Enterprise Coworker connector details in Claude with Connect to Claude highlighted.](./assets/ai-platforms/claude/claude-connect-coworker.png)

1. Sign in with your Adobe credentials to connect Coworker to [!DNL Claude].

### [!DNL Gemini Enterprise] {#gemini-enterprise}

Use Coworker to get marketing insights in [!DNL Gemini Enterprise].

Before you begin, confirm you have access to [!DNL Gemini Enterprise].

#### Set up organization access {#gemini-organization-setup}

As a [!DNL Gemini Enterprise] administrator, complete these steps to make Coworker available to your organization.

1. Go to the [Gemini Enterprise AI Agents marketplace](https://console.cloud.google.com/marketplace/browse?filter=solution-type:ai-agent-service).
1. Search for Adobe CX Enterprise Coworker, then select the **[!UICONTROL Adobe CX Enterprise Coworker]** agent card.
1. On the agent card, select **[!UICONTROL Contact Sales]**.

   ![Gemini Enterprise marketplace agent listing with the Contact Sales button.](./assets/ai-platforms/gemini-enterprise/gemini-contact-sales.png){width="700"}

1. Complete the form to submit your request to Adobe.

   ![Email Adobe Inc form with contact and project fields, a consent checkbox, and the Send Email button.](./assets/ai-platforms/gemini-enterprise/gemini-contact-adobe.png){width="600"}

   Adobe creates a private offer at no cost and emails you a link.

1. Open the emailed link and approve the private offer.

   After you approve the offer, Adobe enables the agent for your [!DNL Gemini Enterprise] account.

1. Publish the agent to selected users or all enterprise users in your organization.

#### Access Coworker {#gemini-access}

After your administrator publishes Coworker to you, open it in [!DNL Gemini Enterprise] to start asking questions.

1. In [!DNL Gemini Enterprise], go to the **[!UICONTROL Agents]** catalog.
1. Search for Adobe CX Enterprise Coworker.
1. Select **[!UICONTROL Adobe CX Enterprise Coworker]** and enter a prompt to get started.

For ideas, explore the [key use cases](#key-use-cases) and [example prompts](#example-prompts).

### [!DNL Amazon Quick] {#amazon-quick}

Use Coworker to get marketing insights in [!DNL Amazon Quick].

Before you begin, confirm you have access to [!DNL Amazon Quick] and your Adobe account.

#### Connect Coworker {#amazon-quick-connection}

Connect Coworker in [!DNL Amazon Quick] using Model Context Protocol (MCP). Adobe has already approved [!DNL Amazon Quick] for this connection.

1. In [!DNL Amazon Quick], go to **[!UICONTROL Connectors]**.
1. Search for MCP and open the connector setup.
1. Enter `https://mcp.coworker.experience.adobe.io` as the MCP server URL.

   Allow a few minutes for the connection to complete and register.

1. Follow the setup prompts and sign in with your Adobe credentials.
1. Confirm that the connection is successful before you start asking questions.

#### Access Coworker {#amazon-quick-access}

After you connect Coworker, use it in [!DNL Amazon Quick] to ask questions about your Adobe data.

For ideas, explore the [key use cases](#key-use-cases) and [example prompts](#example-prompts).

### [!DNL IBM watsonx Orchestrate] {#ibm-watsonx-orchestrate}

Use Coworker to get marketing insights in [!DNL IBM watsonx Orchestrate].

Before you begin, confirm you have access to [!DNL IBM watsonx Orchestrate] and your Adobe account.

You also need permission to manage connections, register MCP servers, and edit an agent. Confirm your OAuth client settings with your Adobe representative before setup.

#### Create your Coworker connection {#ibm-connection}

Connect Coworker using OAuth, then authenticate with your Adobe account. The following steps prepare the connection for testing in the draft environment.

1. In [!DNL IBM watsonx Orchestrate], go to **[!UICONTROL Connections]**, then select **[!UICONTROL Add connection]**.
1. Enter a **[!UICONTROL Connection ID]**, **[!UICONTROL Display name]**, and optional **[!UICONTROL Connection description]**, then select **[!UICONTROL Save and continue]**.
1. In **[!UICONTROL Configure draft environment]**, select **[!UICONTROL OAuth2 Authorization Code]** as the **[!UICONTROL Authentication type]**.
1. Enter the connection settings.

   | Field | Value |
   | --- | --- |
   | [!UICONTROL Server URL] | `https://mcp.coworker.experience.adobe.io` |
   | [!UICONTROL Token URL] | The token endpoint confirmed for your OAuth client. |
   | [!UICONTROL Authorization URL] | The authorization endpoint confirmed for your OAuth client. |
   | [!UICONTROL Client ID] | Your approved OAuth client ID. |
   | [!UICONTROL Client Secret] | Your approved OAuth client secret. |

   ![IBM watsonx Orchestrate connection settings with OAuth2 Authorization Code authentication and the Coworker server address.](./assets/ai-platforms/ibm/ibm-add-connection.png){width="700"}

1. Select **[!UICONTROL PKCE]** and **[!UICONTROL Member credentials]**, then select **[!UICONTROL Next]**.
1. Complete **[!UICONTROL Configure live environment]**, then select **[!UICONTROL Finish]** to save the connection.

<!-- Confirm the customer process for obtaining OAuth settings before publication. -->

#### Sign in with Adobe {#ibm-sign-in}

Add your member credential to authenticate the connection with your Adobe identity.

1. Go to **[!UICONTROL Settings]** > **[!UICONTROL Member credentials]**, then select **[!UICONTROL Add member credential]**.
1. Select your Coworker connection and proceed to **[!UICONTROL Set credential]**.
1. Select **[!UICONTROL Connect and save]**, then sign in with your Adobe credentials when prompted.
1. Return to [!DNL IBM watsonx Orchestrate] and confirm that your credential was added successfully.

#### Register the MCP server {#ibm-register-server}

Register Coworker through Model Context Protocol (MCP) to import its tools into [!DNL IBM watsonx Orchestrate].

1. Go to **[!UICONTROL AI GATEWAY]** > **[!UICONTROL MCP servers]**, then select **[!UICONTROL Register server]**.
1. Enter the server settings.

   | Field | Value |
   | --- | --- |
   | [!UICONTROL Server name] | A descriptive name, such as `cx-coworker`. |
   | [!UICONTROL Transport type] | [!UICONTROL Streamable HTTP] |
   | [!UICONTROL MCP server URL] | `https://mcp.coworker.experience.adobe.io` |
   | [!UICONTROL Connection] | The Coworker connection you authenticated. |

1. Select **[!UICONTROL Register]** and wait for the server registration and tool import to finish.

   ![IBM watsonx Orchestrate registering the Coworker server with Streamable HTTP transport and the authenticated connection.](./assets/ai-platforms/ibm/ibm-register-mcp.png){width="700"}

#### Add tools to your agent {#ibm-agent-tools}

Add the imported tools to your agent, then test the connection before deploying the agent.

1. Go to **[!UICONTROL Active inventory]** > **[!UICONTROL Agents]** and open the agent you want to configure.
1. In **[!UICONTROL Build]**, select **[!UICONTROL Tools]**, then **[!UICONTROL Add Tool]**.
1. Select **[!UICONTROL MCP server]** and find the tools from your registered Coworker server.
1. Select the Coworker tools you need, then select **[!UICONTROL Add to agent]**.
1. Enter a prompt in **[!UICONTROL Draft Preview]** and review the response to confirm that the connection works.

For ideas, explore the [key use cases](#key-use-cases) and [example prompts](#example-prompts).

### [!DNL Databricks] {#databricks}

Use Coworker to get marketing insights in [!DNL Databricks Genie One].

Before you begin, confirm you have access to [!DNL Databricks Genie One] and your Adobe account. You also need permission to install an MCP service in your chosen [!DNL Unity Catalog] catalog and schema.

Confirm your OAuth client settings with your Adobe representative before setup.

#### Install Coworker {#databricks-install}

Install the Coworker MCP service from [!DNL Databricks Marketplace].

1. In [!DNL Databricks], go to **[!UICONTROL Marketplace]** and search for Adobe Coworker.
1. Select **[!UICONTROL Adobe CX Enterprise Coworker]**, then select **[!UICONTROL Install]**.
1. Select a **[!UICONTROL Catalog]** and **[!UICONTROL Schema]**, then enter an **[!UICONTROL MCP service name]**.
1. Keep the connection settings supplied by the listing, including the following values.

   | Field | Value |
   | --- | --- |
   | [!UICONTROL Host] | `https://mcp.coworker.experience.adobe.io` |
   | [!UICONTROL Base path] | `/mcp` |
   | [!UICONTROL Credential type] | [!UICONTROL OAuth U2M] |

   ![Databricks Marketplace installation dialog for Adobe CX Enterprise Coworker with catalog, schema, connection, and credential fields.](./assets/ai-platforms/databricks/databricks-install.png){width="700"}

1. Enter your **[!UICONTROL Client ID]** and **[!UICONTROL Client secret]**.
1. Review and accept the terms, then select **[!UICONTROL Install]**.

<!-- Confirm the customer process for obtaining OAuth settings before publication. -->

#### Connect your Adobe account {#databricks-adobe-connection}

Each user signs in with their Adobe account. Coworker requests use that user's Adobe permissions.

1. In **[!UICONTROL Catalog]**, open the installed Coworker service under your selected catalog and schema.
1. Complete Adobe sign-in when prompted.
1. Confirm that the service **[!UICONTROL Status]** is **[!UICONTROL Active]** and that its tools are listed.
1. In **[!UICONTROL Get started]**, select **[!UICONTROL Genie]**, then **[!UICONTROL Genie One]**, and select **[!UICONTROL Add to Genie One]**.

#### Access Coworker {#databricks-access}

Confirm your connector is available before asking questions in [!DNL Genie One].

1. In [!DNL Genie One], go to **[!UICONTROL Customizations]** > **[!UICONTROL Connectors]** and open your Coworker connector.
1. Confirm that the connector shows **[!UICONTROL Connected]**. Review tool approval settings according to your organization's policies.

   ![Coworker connector in Databricks Genie One showing Connected status, available tools, and tool approval settings.](./assets/ai-platforms/databricks/databricks-connectors.png){width="700"}

1. Select **[!UICONTROL New chat]** and enter a prompt, such as "Using Adobe Coworker, list the published audiences".

For ideas, explore the [key use cases](#key-use-cases) and [example prompts](#example-prompts).

<!-- Setup steps for Microsoft 365 Copilot, ChatGPT, and Claude reflect the real customer-facing flow confirmed by PM (Siddhartha Srivastava) on 2026-09-02: an org admin approves the connector or plugin, then end users find and add it in their platform's catalog and sign in. The previous version of this file described a manual MCP-connector setup for ChatGPT (Settings > Connectors > paste server URL) -- PM clarified that flow is for internal testing only, not the customer path, so it was removed here. -->

<!-- Amazon Quick setup follows PM guidance from the October 28, 2026 email, "Coworker in AI Platforms screenshots - Gemini / Amazon Quick." End users connect through MCP and sign in with Adobe credentials. -->

## Example prompts {#example-prompts}

After you set up Coworker in a supported platform, try these prompts, or write your own in natural language.

* Show your top five audiences.
* Show a metric for the last month.
* Show your active Workfront projects.
* Show journeys with loyalty audiences.

## Known limitations {#known-limitations}

Coworker in AI platforms does not support all capabilities available in the Coworker interface.

* You cannot connect Coworker to a custom agentic harness outside the supported AI platforms listed in this document. To request support for additional AI platforms or agentic harnesses through MCP, contact your Adobe representative.
* The Firefly Image Generation skill is not available when you access Coworker through Claude. The skill remains available in the Coworker interface and other supported AI platforms described in this document. To use the Firefly Image Generation skill, access Coworker through the Coworker interface or another supported AI platform.

## Troubleshoot Coworker in AI platforms {#troubleshoot}

Try these steps if you run into issues using Coworker in an AI platform.

* If you see an error, sign out and sign in again with your Adobe credentials. Re-authenticating resolves most issues.
* If you cannot access Coworker or specific data, contact your Adobe administrator to confirm your product access and permissions.

<!--
Editorial maintenance, 2026-10-27:
Only approved platforms with validated setup guidance belong in the platform sections.
Databricks setup follows the supplied "Adobe Coworker in Genie One.mp4" walkthrough. Confirm marketplace availability and customer OAuth provisioning before publication.

To add an approved platform:
* Confirm approval and obtain access to the customer flow.
* Validate prerequisites, organization approval, catalog discovery, listing name, installation, and Adobe sign-in.
* Confirm the shared licensing, permissions, use cases, prompts, limitations, and troubleshooting guidance applies.
* Add an H3 platform section with an explicit anchor under Set up Coworker and add it to the linked platform list.
* Follow the existing order: introduction, platform prerequisites, setup tasks, and user access. Use H4 task headings with unique anchors.
* Document any platform-specific requirements or exceptions within that section.
* Preview the section and verify its links and image references.
Keep the article introduction, metadata, and shared prerequisites free of platform lists so adding a section does not require duplicate updates.

Gemini Enterprise follow-up:
Administrator setup and end user access steps are documented. Confirm applicability of the shared guidance before expanding the section.
-->
