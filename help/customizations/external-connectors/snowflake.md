---
title: Snowflake External Connector
description: Learn how to set up the Snowflake external connector in CX Enterprise Coworker with a service account or per-person sign-in to use Snowflake data in chat.
role: Admin, User
level: Beginner
badgeBeta: label="Beta" type="Informative" tooltip="This connector is in beta."
product_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: CX Enterprise Coworker
hide: true
---

# Snowflake external connector {#snowflake}

Use the [!DNL Snowflake] external connector to ask questions about your [!DNL Snowflake] data in plain language in Adobe CX Enterprise Coworker. The connector links Coworker to a [!DNL Snowflake]-managed Model Context Protocol (MCP) server in your [!DNL Snowflake] account. Coworker can then use the tools that the server exposes, such as [!DNL Cortex Analyst], [!DNL Cortex Search], and SQL tools.

>[!AVAILABILITY]
>
>The [!DNL Snowflake] external connector is in beta. The documentation and the functionality are subject to change.

## Connector configuration {#connector-configuration}

The connector configuration process has two separate parts:

* **Organization setup:** An administrator connects Coworker to an existing [!DNL Snowflake] MCP server, chooses how people sign in, and selects the tools that members can use.
* **Member access:** Members use the connection with either a shared organization identity or their own [!DNL Snowflake] identity, depending on the sign-in option.

The administrator chooses one of the following sign-in options:

| Option | What the administrator provides | How access works |
| --- | --- | --- |
| **[!UICONTROL Organization service account]** | A [!DNL Snowflake] programmatic access token (PAT) for a service account. | All members use the permissions of the service account. Token expiration or revocation affects all members. |
| **[!UICONTROL Each person signs in]** | The client ID and client secret of a [!DNL Snowflake] OAuth integration, and an optional [!DNL Snowflake] role. | Each member signs in with their own [!DNL Snowflake] identity, and access follows their [!DNL Snowflake] permissions. |

Neither option grants [!DNL Snowflake] privileges that the selected identity does not already have. [!DNL Snowflake] enforces permissions on every request.

## Prerequisites {#prerequisites}

Coworker connects to an existing [!DNL Snowflake] MCP server. It does not create the server or its tools. Before you begin, make sure that you have the following:

* **For organization setup:** An account with permission to manage organization connectors in Coworker.
* **For the [!DNL Snowflake] MCP server:** The full HTTPS URL of the server, including its database, schema, and server name.
* **For the service account option:** A PAT for a dedicated service account. The service account role should have only the privileges needed for the MCP server and its tools.
* **For the per-person sign-in option:** A [!DNL Snowflake] OAuth integration with its client ID and client secret. You also need a [!DNL Snowflake] administrator who can register the Coworker redirect URL and configure the integration.

>[!IMPORTANT]
>
>Never share PATs, OAuth client secrets, or other credentials in screenshots, chats, or support tickets. Use organization secrets and a least-privileged [!DNL Snowflake] identity.

### Configure your Snowflake MCP server {#configure-snowflake-mcp-server}

A [!DNL Snowflake] administrator must complete the following tasks in [!DNL Snowflake] before you configure the connector:

1. Create the MCP server and define the tools it exposes.
1. Grant the required roles access to the MCP server, its tools, and the underlying objects.

   Access to the MCP server does not automatically grant access to every tool or object.

1. Set up authentication for the sign-in option you plan to use:

   * For the service account option, create a PAT for the service account.
   * For the per-person sign-in option, create an OAuth integration that issues refresh tokens.

For instructions, see the following [!DNL Snowflake] documentation:

* [Snowflake-managed MCP server](https://docs.snowflake.com/en/user-guide/snowflake-cortex/cortex-agents-mcp){target="_blank"}
* [Create MCP server](https://docs.snowflake.com/en/sql-reference/sql/create-mcp-server){target="_blank"}
* [Overview of access control](https://docs.snowflake.com/en/user-guide/security-access-control-overview){target="_blank"}
* [Configure Snowflake OAuth for custom clients](https://docs.snowflake.com/en/user-guide/oauth-custom){target="_blank"}
* [Create security integration (Snowflake OAuth)](https://docs.snowflake.com/en/sql-reference/sql/create-security-integration-oauth-snowflake){target="_blank"}
* [Using programmatic access tokens for authentication](https://docs.snowflake.com/en/user-guide/programmatic-access-tokens){target="_blank"}

## Configure the connector for your organization {#configure-organization}

Administrators make the [!DNL Snowflake] connector available to everyone in the organization. Changes on the organization page apply to all users in your organization.

1. Open **[!UICONTROL Customizations]**, select **[!UICONTROL Org]**, and then select **[!UICONTROL External Connectors]**. On the **[!UICONTROL Snowflake]** card, select **[!UICONTROL Configure]**.

1. In the **[!UICONTROL Connect Snowflake]** dialog, enter the full URL of your [!DNL Snowflake] MCP server in **[!UICONTROL Server URL]**. The URL must use HTTPS and follow this pattern:

   ```text
   https://<account-host>/api/v2/databases/<database>/schemas/<schema>/mcp-servers/<server-name>
   ```

   Use the exact URL for your [!DNL Snowflake] account and MCP server. The account hostname must not contain an underscore, including an encoded underscore (`%5F`). Do not include credentials in the URL. Coworker checks the HTTPS scheme, host, and path before saving.

1. Under **[!UICONTROL Who signs in?]**, select a sign-in option, and then complete its settings.

   * **[!UICONTROL Organization service account]:** Requests use the permissions of the service account through a programmatic access token (PAT). Use this option for centrally managed access. Use a dedicated service account with a narrowly scoped role, not a personal account.

     ![Connect Snowflake dialog with Organization service account selected, showing the Server URL field, the Service account token options, the Programmatic access token field, and a warning that everyone acts with the permissions of the token owner.](./assets/snowflake/org-service-account.png){width="500" zoomable="yes"}

     | Setting | Description |
     | --- | --- |
     | **[!UICONTROL Service account token]** | Choose where the token comes from. Select **[!UICONTROL Enter new]** to enter a PAT, or **[!UICONTROL Use an existing secret]** to reuse an organization secret that already contains the token. An existing secret must contain the complete value for the `Authorization` header, not only the raw token. |
     | **[!UICONTROL Programmatic access token]** | Required when you select **[!UICONTROL Enter new]**. Create the token for a dedicated [!DNL Snowflake] service account with only the required permissions. For instructions, select **[!UICONTROL How to create a programmatic access token]** in the dialog. Coworker stores the token as an organization secret. |

     >[!IMPORTANT]
     >
     >Everyone who uses this connection acts with the permissions of the token owner. If the token expires or is revoked, the connection stops working for all members.

     Creating and using a PAT can be subject to [!DNL Snowflake] network and authentication policies. If token creation or authentication is blocked, ask your [!DNL Snowflake] administrator to check these policies.

   * **[!UICONTROL Each person signs in]:** Requests use the [!DNL Snowflake] permissions of each person. Use this option for governed, user-driven access.

     ![Connect Snowflake dialog with Each person signs in selected, showing the Redirect URL, the OAuth integration credentials options, the OAuth integration client ID and client secret fields, and the optional Snowflake role field.](./assets/snowflake/org-oauth.png){width="500" zoomable="yes"}

     | Setting | Description |
     | --- | --- |
     | **[!UICONTROL Redirect URL]** | Read-only. Copy this URL, and register it as the redirect URI in your [!DNL Snowflake] OAuth security integration. The value must match exactly. For instructions, select **[!UICONTROL How to create a Snowflake OAuth integration]** in the dialog. The redirect URL differs between environments, so always copy it from the dialog. |
     | **[!UICONTROL OAuth integration credentials]** | Choose where the credentials come from. Select **[!UICONTROL Enter new]** to enter the client ID and client secret, or **[!UICONTROL Use an existing secret]** to select the organization secrets that contain them. |
     | **[!UICONTROL OAuth integration client ID]** | Required when you select **[!UICONTROL Enter new]**. The client ID of your customer-managed [!DNL Snowflake] OAuth integration. |
     | **[!UICONTROL OAuth integration client secret]** | Required when you select **[!UICONTROL Enter new]**. The client secret of the same OAuth integration. Members never enter these credentials. |
     | **[!UICONTROL Snowflake role]** | Optional. The role that each session uses, requested through the OAuth scope `session:role:ROLE_NAME`. The role must be granted to your members and have access to the MCP server. Leave the field blank to use the default role of each member. |

     Coworker derives the OAuth endpoints from the account URL and requests a refresh token. Configure the OAuth integration to issue refresh tokens. The requested scope alone does not override the integration configuration.

     Coworker converts the role name to uppercase. Roles created with a quoted lowercase name cannot be used. If the OAuth integration blocks the role, or a member does not have the role, sign-in or access can fail.

1. Under **[!UICONTROL Tools available to users]**, choose the tools that members can use. Each [!DNL Snowflake] MCP server defines its own tools, so the dialog does not show a fixed list. Enter tool names as defined in your MCP server, not tool types such as `CORTEX_ANALYST_MESSAGE`. To view the tool names, run `DESCRIBE MCP SERVER` in [!DNL Snowflake].

   ![Connect Snowflake dialog showing the Snowflake role field, the Tools available to users section with Allowed tool names and Blocked tool names fields, the Access and permissions notice, and a summary with OAuth (customer integration) authentication, HTTP connection, and a 300-second tool timeout.](./assets/snowflake/org-tools.png){width="500" zoomable="yes"}

   | Setting | Description |
   | --- | --- |
   | **[!UICONTROL Allowed tool names]** | The tools that members can use. Separate names with commas or spaces. Leave the field empty to allow every tool that the server exposes, except blocked tools. |
   | **[!UICONTROL Blocked tool names]** | The tools that members can never use. Separate names with commas or spaces. Blocked tools stay unavailable even if you also allow them. |

   >[!IMPORTANT]
   >
   >If you leave **[!UICONTROL Allowed tool names]** empty, members can use every tool, including any SQL execution tool. SQL execution tools run SQL as the connected identity. Review the tool definitions on your server, and allow only the tools that your organization needs.

   Tool descriptions are not a substitute for [!DNL Snowflake] privileges or other access controls. For [!DNL Cortex Analyst] tools, set up a semantic view and the required grants, including the `SNOWFLAKE.CORTEX_USER` database role. For [!DNL Cortex Agent] tools, configure read-only tools and turn off code execution in [!DNL Snowflake]. Members cannot change the tool selection.

1. Review **[!UICONTROL Access and permissions]**, and then select **[!UICONTROL Save connection]**. The **[!UICONTROL Snowflake]** card shows **[!UICONTROL Configuration saved]**.

   Select **[!UICONTROL View configuration]** to review the server URL, authentication type, and tool policy. Then select **[!UICONTROL Test connection]** to check access and discover the server tools.

   New [!DNL Snowflake] connections use a 300-second tool timeout. An older connection without a saved timeout may use the default of 60 seconds. Check the timeout shown for an existing connection.

A successful test does not confirm that every tool or [!DNL Snowflake] object is available to every member.

## Use the connector as a member {#use-as-member}

After an administrator configures the connector, open it from your own **[!UICONTROL Customizations]** view.

1. Open **[!UICONTROL Customizations]**, select **[!UICONTROL User]**, and then select **[!UICONTROL External Connectors]**.

   If the **[!UICONTROL Snowflake]** card shows **[!UICONTROL Not configured]**, ask your administrator to [configure the connector](#configure-organization).

1. Open **[!UICONTROL Snowflake]**. The connector details are read-only for members. You cannot change the server URL, credentials, or tool selection.

1. If the connection uses an organization service account, requests use the identity of the organization. You do not need to sign in. Never enter or share the PAT.

1. If the connection uses per-person sign-in, start the sign-in and authenticate with the intended [!DNL Snowflake] account. Complete any required single sign-on (SSO) or multi-factor authentication (MFA) steps. Confirm the requested organization, application, and role, if one appears.

1. If needed, select **[!UICONTROL Test connection]**. A successful test shows **[!UICONTROL Connection successful]** and the number of available tools.

   ![Snowflake connector details showing a Connected status, a Connection successful message with five available tools, a notice that the admin set up the connector, and the server URL, sign-in option, authentication, connection, and tool timeout.](./assets/snowflake/member-details.png){width="700" zoomable="yes"}

   Before a successful test, the details may show only the tool names that your administrator allowed, or prompt you to run the test. After the test, each tool appears with its description.

   ![Snowflake connector details showing the connection type, tool timeout, Signed in status, Sign out and Refresh buttons, and five example tools enabled by the admin.](./assets/snowflake/member-tools.png){width="700" zoomable="yes"}

The tools in the example are defined by one [!DNL Snowflake] MCP server. The tools that you see depend on your server and the tool selection of your administrator.

The authentication details of the connection show whether it uses a PAT, machine OAuth, or per-person OAuth. To disconnect your [!DNL Snowflake] account, select **[!UICONTROL Sign out]**.

A **[!UICONTROL Connected]** status does not guarantee access to a specific tool or data object. [!DNL Snowflake] grants, policies, and the selected role still apply.

## Troubleshoot access {#troubleshoot-access}

If setup, sign-in, or access fails, check the following with your administrator:

| Issue | What to check |
| --- | --- |
| The server URL is rejected | The URL uses HTTPS and the full `/api/v2/databases/<database>/schemas/<schema>/mcp-servers/<server-name>` path. The account hostname has no underscores, and the URL has no credentials. |
| The PAT cannot be created or used | The network policy, authentication policy, token expiration, and role of the service account. If you use an existing secret, confirm that it contains the complete `Authorization` header value. |
| The OAuth redirect URL does not match | The [!DNL Snowflake] OAuth integration has the exact redirect URL from the same Coworker environment. |
| Sign-in succeeds, but requests fail | The role is granted to the member and allowed by the OAuth integration. The integration issues refresh tokens, and the client ID and secret belong to the intended integration. |
| A tool is missing or denied | The **[!UICONTROL Allowed tool names]** and **[!UICONTROL Blocked tool names]** settings, the tool availability on the MCP server, and the [!DNL Snowflake] grants on the server, tool, and underlying objects. |
| A tool call times out | The **[!UICONTROL Tool timeout]** on the connector details. New connections use 300 seconds. Older connections without a saved timeout may use 60 seconds. |
