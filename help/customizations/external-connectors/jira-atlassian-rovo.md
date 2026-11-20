---
title: Jira / Atlassian Rovo External Connector
description: Learn how to set up the Jira / Atlassian Rovo external connector in CX Enterprise Coworker and sign in with Atlassian to read and search Jira work items.
role: Admin, User
level: Beginner
badgeBeta: label="Beta" type="Informative" tooltip="This connector is in beta."
product_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: CX Enterprise Coworker
hide: true
---

# Jira / Atlassian Rovo external connector {#jira-atlassian-rovo}

Use the [!DNL Jira] / [!DNL Atlassian Rovo] external connector to read and search your [!DNL Jira] work items in Adobe CX Enterprise Coworker. After you set up the connector, ask Coworker to find work items, read their details, and search with Jira Query Language (JQL). The connector is a Model Context Protocol (MCP) server hosted by [!DNL Atlassian].

>[!AVAILABILITY]
>
>The [!DNL Jira] / [!DNL Atlassian Rovo] external connector is in beta. The documentation and the functionality are subject to change.

## Connector configuration {#connector-configuration}

The connector configuration process has three separate parts:

* **[!DNL Atlassian] preparation:** An [!DNL Atlassian] organization administrator allows the Coworker redirect URL domain and reviews the MCP access policies.
* **Organization setup:** A Coworker administrator configures the connector once for the whole organization. The administrator chooses the read-only tools that members can use.
* **Member sign-in:** Each member signs in with their own [!DNL Atlassian] account. Members can access only the [!DNL Jira] data that their account has permission to view.

Saving the organization configuration does not sign in any members or grant [!DNL Jira] permissions. Each member must sign in separately.

The connector has no shared service account or API token option. Coworker registers the OAuth application with [!DNL Atlassian] automatically, so you do not enter a client ID or client secret.

Although the connector name includes [!DNL Atlassian Rovo], the connector requests [!DNL Jira] read and search access only. It does not request [!DNL Confluence], [!DNL Rovo]-specific, write, or destructive access. Other [!DNL Atlassian] MCP capabilities are not necessarily available through this connector.

## Prerequisites {#prerequisites}

Before you begin, make sure that you have the following:

* **For organization setup:** An account with permission to manage organization connectors in Coworker, in an organization where the [!DNL Jira] / [!DNL Atlassian Rovo] connector is available.
* **For [!DNL Atlassian] preparation:** An [!DNL Atlassian] organization administrator who can approve MCP access and the Coworker redirect URL domain.
* **For member sign-in:** [!DNL Atlassian] accounts with access to the intended [!DNL Jira] sites, projects, and work items.
* **For network access:** [!DNL Atlassian] IP allowlists and app policies that permit the connection. A successful sign-in does not confirm that tool requests are allowed.
* **[!DNL Rovo] enabled:** [!DNL Rovo] enabled for your [!DNL Atlassian] organization and the intended [!DNL Jira] sites before members use the connector. For more information, see [How to enable Rovo](https://www.atlassian.com/software/rovo/guides/admin-guide/rovo-activation) in the [!DNL Atlassian] documentation.

## Prepare [!DNL Atlassian] access {#prepare-atlassian}

Before members sign in, an [!DNL Atlassian] organization administrator prepares access in [!DNL Atlassian Administration]:

1. Open [!DNL Atlassian Administration], and select the intended organization.

1. Select **[!UICONTROL Connectors]** > **[!UICONTROL Atlassian MCP server]** > **[!UICONTROL Add domain]**.

1. Add the domain of the **[!UICONTROL Redirect URL]** shown in the Coworker setup dialog. For the dialog, see [Configure the connector for your organization](#configure-organization).

   Follow the [!DNL Atlassian] domain format rules instead of pasting the full URL. For more information, see [Available Atlassian MCP server domains](https://support.atlassian.com/security-and-access-policies/docs/available-atlassian-mcp-server-domains/) in the [!DNL Atlassian] documentation.

1. Review the MCP permission groups, app policies, and IP allowlists with the [!DNL Atlassian] administrator. For more information, see the following [!DNL Atlassian] documentation:

   * [Supported Atlassian MCP tools](https://support.atlassian.com/atlassian-ai-gateway/docs/supported-tools/), for the permission groups and scopes that each tool requires
   * [Control Atlassian MCP server settings](https://support.atlassian.com/security-and-access-policies/docs/control-atlassian-mcp-server-settings/), for authentication and IP allowlisting

Always use the redirect URL shown in the Coworker dialog for the environment that you are setting up. Do not copy a redirect URL from another environment.

## Configure the connector for your organization {#configure-organization}

Administrators make the [!DNL Jira] / [!DNL Atlassian Rovo] connector available to everyone in the organization. Changes on the organization page apply to all users in your organization.

1. Open **[!UICONTROL Customizations]**, select **[!UICONTROL Org]**, and then select **[!UICONTROL External Connectors]**. On the **[!UICONTROL Jira / Atlassian Rovo]** card, select **[!UICONTROL Configure]**. Members cannot configure or remove this connection.

1. In the **[!UICONTROL Connect Jira / Atlassian Rovo]** dialog, review the fixed **[!UICONTROL Server URL]**, `https://mcp.atlassian.com/v2/mcp`.

   Review the **[!UICONTROL Redirect URL]**, and make sure that an [!DNL Atlassian] administrator approves its domain, as described in [Prepare Atlassian access](#prepare-atlassian). You do not enter any OAuth credentials.

1. Under **[!UICONTROL Tools available to users]**, choose the tools that members can use. For more information, see [Available tools](#available-tools).

   The `getAccessibleAtlassianResources` site discovery tool is required and stays enabled. The other five tools are optional. To block an optional tool for everyone in your organization, remove it. To bring back the tools that you removed, select **[!UICONTROL Restore all tools]**. You can save the configuration with only site discovery enabled, but members then cannot read or search work items.

   ![Connect Jira / Atlassian Rovo dialog showing the server URL, a redacted Redirect URL, and six tools available to users, with the required getAccessibleAtlassianResources tool and five optional tools.](./assets/jira-atlassian-rovo/org-configure.png){width="500" zoomable="yes"}

1. Select **[!UICONTROL Save connection]**, and then review the connection details.

   The connector requests the following OAuth scopes when each member signs in:

   | Scope | Purpose |
   | --- | --- |
   | `read:me`, `read:account` | Support authorization with the [!DNL Atlassian] account of the member. |
   | `read:jira:agent-interface` | Read [!DNL Jira] data. |
   | `search:jira:agent-interface` | Search [!DNL Jira] data. |
   | `offline_access` | Refresh the sign-in token. |

   The tool timeout is 60 seconds. The first connection and tool discovery can take longer.

### Available tools {#available-tools}

The [!DNL Jira] / [!DNL Atlassian Rovo] connector provides the following read-only tools:

| Tool | Description | Administrator control |
| --- | --- | --- |
| `getAccessibleAtlassianResources` | Find the [!DNL Atlassian] sites and cloud IDs that you can access. The [!DNL Jira] tools need this tool. | Required |
| `atlassianUserInfo` | Get the account information of the signed-in user. | Optional |
| `getJiraIssue` | Get a [!DNL Jira] work item by ID or key. | Optional |
| `searchJiraIssuesUsingJql` | Search [!DNL Jira] work items with JQL. | Optional |
| `discover` | Find additional tool operations and their input schemas. | Optional |
| `executeRead` | Run read operations found through `discover`, such as reading comments, changelogs, projects, boards, and sprints. | Optional |

>[!IMPORTANT]
>
>The `discover` and `executeRead` tools give members access to additional permitted read operations as a group. You cannot turn off individual operations. If this access is not acceptable for your organization, remove both tools. The connector does not include write operations (`executeWrite`) or destructive operations (`executeDestructive`).

Removing optional tools limits their availability in Coworker. It does not reduce the OAuth scopes that the connector requests at sign-in.

Each tool needs specific [!DNL Atlassian] permission groups and scopes. For more information, see [Supported Atlassian MCP tools](https://support.atlassian.com/atlassian-ai-gateway/docs/supported-tools/) in the [!DNL Atlassian] documentation.

## Sign in as a member {#sign-in-as-a-member}

After an administrator configures the connector, each member signs in with their own [!DNL Atlassian] account. You do not need a client ID, client secret, or access token to sign in.

1. Open **[!UICONTROL Customizations]**, select **[!UICONTROL User]**, and then select **[!UICONTROL External Connectors]**.

1. Find the **[!UICONTROL Jira / Atlassian Rovo]** card. If the card shows **[!UICONTROL Not configured]** and **[!UICONTROL Not available yet. Your admin needs to set this up.]**, ask your administrator to [configure the connector](#configure-organization). Members cannot configure the connector.

1. Select **[!UICONTROL Sign in]**, and use the [!DNL Atlassian] account that has access to the intended [!DNL Jira] site. Complete any required single sign-on (SSO), multi-factor authentication (MFA), and consent prompts. Review the requested read and search access before you consent.

   >[!IMPORTANT]
   >
   >Continue only if you recognize the app and your organization approves the requested access.

1. Return to Coworker, and open the connector details. The connection is read-only for members, and you can view the tools that your administrator enabled. Select **[!UICONTROL Test connection]** to confirm the connection.

1. Optionally, run a small read-only check, as described in [Check your Jira access](#check-access).

A successful test does not confirm that you can access every [!DNL Jira] site, project, or work item.

## Check your [!DNL Jira] access {#check-access}

To confirm that the connector can read your data, start a chat and enter a read-only prompt.

Example prompt:

* "Search Jira for up to five work items assigned to me, ordered by most recently updated. Include their keys and links. Do not modify anything."

For this prompt to work, your administrator must enable a search tool, and your [!DNL Jira] account must have permission to view the work items.

## Troubleshoot access {#troubleshoot-access}

If sign-in or access fails, check the following with your administrator:

| Issue | What to check |
| --- | --- |
| Sign-in is blocked for the client or domain | Confirm that the redirect URL domain for your environment is approved in [!DNL Atlassian Administration], under the **[!UICONTROL Atlassian MCP server]** settings. |
| Consent succeeds, but tool calls are denied | Check your [!DNL Jira] permissions, the [!DNL Atlassian] MCP permission groups, app policies, and IP allowlists. For the permission groups that each tool requires, see [Supported Atlassian MCP tools](https://support.atlassian.com/atlassian-ai-gateway/docs/supported-tools/). |
| JQL search fails, but other reads work | Confirm that your administrator enabled `searchJiraIssuesUsingJql`, and that the connection requests the `search:jira:agent-interface` scope. |
| Consent returns `invalid_request` | Ask your administrator to confirm that the connection requests `read:me` and `read:account` in addition to the [!DNL Jira] scopes. |
| You still see older scopes after a change | An obsolete user-level `jira_login` authentication provider override can take precedence over the organization connection. Ask an administrator to update or remove only that obsolete override, and then sign in again. |
| A tool is missing | Ask your administrator to check the tool selection. Additional read operations need both `discover` and `executeRead`, the required scopes, and the right permissions. |
| **[!UICONTROL Test connection]** is slow or times out | Tool discovery can take longer than the 60-second tool timeout. Check whether the problem is slow discovery or a sign-in failure before you change credentials. |

When you ask for help, do not share passwords, tokens, authorization codes, or consent URLs. Do not include them in screenshots or support tickets.
