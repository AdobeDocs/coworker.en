---
title: Journey Optimizer Tools in CX Coworker Gateway
description: Learn which Adobe Journey Optimizer tools are available through the CX Coworker Gateway.
hide: true
---
# Adobe Journey Optimizer tools in CX Coworker Gateway {#ajo-mcp}

Use the Adobe Journey Optimizer product tools to inspect campaigns, journeys, and channel configurations from an MCP-compatible client. These tools are available through the [CX Coworker Gateway](overview.md) when your organization is enabled and your user account has the required Journey Optimizer permissions.

For more information, see [Work with MCP clients](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/combine/ajo-mcp){target="_blank"} in the Adobe Journey Optimizer documentation.

For a conversational, agentic experience to create, analyze, and simulate journeys, see the [Journey Agent](https://experienceleague.adobe.com/en/docs/cx-enterprise-ai/experience-cloud-ai/agents/ajo-agent) instead.

>[!AVAILABILITY]
>
>The Journey Optimizer product tools are in Beta. Access is by invitation only and requires Adobe organization enablement. See [Access CX Coworker Gateway tools](access.md).

## Key capabilities {#mcp-capabilities}

Journey Optimizer tools provide a read-only surface for campaign, journey, and channel configuration review. You can:

- List Journey Optimizer campaigns and filter by status.
- Retrieve campaign details, including targeting, schedule, channel, and content configuration metadata.
- List and inspect journeys in your sandbox, including branching, conditions, and actions.
- List channel configurations for email, SMS, push, and WhatsApp channels.
- List marketing actions available for data governance policy enforcement.
- Review campaign, journey, and channel setup in natural language without navigating product screens.

>[!IMPORTANT]
>
>All Journey Optimizer tools in the current Beta are read-only. Creating, updating, deleting, starting, stopping, or publishing campaigns or journeys is not supported.

## Available tools {#mcp-tools}

| Tool | Description |
| --- | --- |
| `ajo_campaign_list` | Browse Journey Optimizer marketing campaigns. Supports filtering by status, such as `DRAFT`, `LIVE`, `STOPPED`, and `COMPLETED`. |
| `ajo_campaign_get` | Fetch details and configuration for a specific campaign by ID, including audience targeting, schedule, channel, and content settings metadata. |
| `ajo_journey_list` | Browse all journeys in your Journey Optimizer sandbox. |
| `ajo_journey_get` | Fetch full details for a specific journey by ID, including its branching, conditions, and actions. |
| Journey visualization | Render a journey's structure and flow for interactive, visual exploration. |
| `ajo_channel_configuration_list`, `ajo_channel_configuration_get` | View surface presets and branding settings for email, SMS, push, or [!DNL WhatsApp] channels. |
| `ajo_channel_configuration_resource_list`, `ajo_channel_configuration_resource_get` | List and retrieve supporting configuration resources referenced by channel configurations, such as push credentials, email subdomains, IP pools, SMS credentials, and [!DNL WhatsApp] credentials. |
| `ajo_marketing_action_list` | List available marketing actions for data governance policy enforcement. |

## Example prompts {#mcp-use-cases}

| Goal | Example prompt |
| --- | --- |
| Campaign overview | "Show me all my Journey Optimizer campaigns." |
| Status audit | "Which campaigns are currently live?" |
| Campaign details | "Get the full details of campaign `[campaign ID]`." |
| Journey overview | "Show me all my Journey Optimizer journeys." |
| Journey details | "Get the full details of journey `[journey ID]`, including branching and conditions." |
| Audience and targeting | "What audience is targeted in campaign `[campaign ID]`?" |
| Schedule and timing | "When is campaign `[campaign ID]` scheduled to run?" |
| Troubleshooting | "Review the setup of campaign `[campaign ID]` and flag possible issues." |
| Channel configuration | "What email channel configurations are available?" |
| Channel audit | "Which channel configurations are missing or incomplete?" |
| Governance | "What marketing actions are available in my sandbox?" |

## Content management tools {#mcp-content-management}

In addition to the read-only product tools above, Journey Optimizer users can discover and manage content assets — content templates, fragments, landing pages, and journey or campaign inline message content — directly from CX Coworker using natural language prompts. This capability is powered by a separate set of read- and write-capable MCP tools for Journey Optimizer content, and is available to all customers who have access to CX Coworker.

For more information, see [Content Management tools](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/get-started/essentials/ajo-coworker-skills#content-management){target="_blank"} in the Adobe Journey Optimizer documentation.

Content management tools let you:

- Browse content templates, fragments, and landing pages, and retrieve their structure, metadata, and status.
- Retrieve the inline message content configured on a journey or campaign action node.
- Create and update content templates for any channel.
- Create, update, clone, and publish fragments.
- Replace a channel variant on a journey or campaign action node's inline message.

>[!IMPORTANT]
>
>Unlike the read-only product tools above, content management tools support write operations. Full-text search across templates or fragments, template or fragment validation, creating or publishing landing pages, and deleting content templates, fragments, or landing pages are not supported.

## Product context and permissions {#mcp-context}

Your user account must have permission to view the Journey Optimizer campaigns, journeys, and channel configurations you query. The MCP does not bypass product permissions.

If your organization uses multiple sandboxes, specify the sandbox or environment context in your prompt when you need results from a specific sandbox.

## Known limitations {#mcp-limitations}

| Limitation | Description | Workaround |
| --- | --- | --- |
| Read-only surface | Journey Optimizer tools only expose retrieve operations. You cannot create, update, delete, start, stop, or publish campaigns or journeys. | Use the Journey Optimizer UI or APIs for write operations. |
| No engagement or performance metrics | Tools do not return reporting data such as impressions, click-through rates, conversions, or delivery stats. | Use Journey Optimizer reporting, Customer Journey Analytics tools, or Adobe Analytics tools for performance metrics. |
| Campaign list pagination is limited | Campaign listing returns the first page of results, up to 50 campaigns sorted alphabetically. Offset and limit values are not applied. | Use `Get Campaign` directly if the campaign ID is known. Use the Journey Optimizer UI for full browsing and filtering. |
| No server-side filtering by date, channel, or schedule | Campaign listing supports status filtering, but not publish date, schedule date, channel, or campaign type filtering. | Use the Journey Optimizer UI campaign list for native date and channel filtering. |
| Message content retrieval unavailable via product tools | Message HTML, subject lines, personalization tokens, and offer content are not available through the read-only product tools above. | Use the [content management tools](#mcp-content-management) to retrieve and update inline message content, or view it directly in the Journey Optimizer UI. |