---
title: Google BigQuery External Connector
description: Learn how to set up the Google BigQuery external connector in CX Enterprise Coworker with your Google OAuth app and sign in to query BigQuery data in chat.
role: Admin, User
level: Beginner
badgeBeta: label="Beta" type="Informative" tooltip="This connector is in beta."
product_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: CX Enterprise Coworker
hide: true
---

# Google BigQuery external connector {#google-bigquery}

Use the [!DNL Google BigQuery] external connector to explore and query your [!DNL BigQuery] data in Adobe CX Enterprise Coworker. After you set up the connector, ask Coworker to list datasets and tables, explain a table schema, and run read-only SQL queries. The connector is a Model Context Protocol (MCP) server hosted by [!DNL Google] at `https://bigquery.googleapis.com/mcp`.

>[!AVAILABILITY]
>
>The [!DNL Google BigQuery] external connector is in beta. The documentation and the functionality are subject to change.

## Connector configuration {#connector-configuration}

The connector configuration process has three separate parts:

* **[!DNL Google Cloud] preparation:** A [!DNL Google Cloud] administrator prepares a query project, enables the [!DNL BigQuery] API, and grants members the required Identity and Access Management (IAM) roles.
* **Organization setup:** A Coworker administrator configures the connector once for the whole organization. The administrator connects the [!DNL Google] OAuth app of the organization and selects the tools that members can use.
* **Member sign-in:** Each member signs in with their own [!DNL Google] account. Members can access only the projects and datasets that their [!DNL Google] identity can access.

The connector uses an OAuth app that your organization owns. Adobe does not provide a [!DNL Google] OAuth app for this connector. Saving the organization configuration does not sign in any members or grant [!DNL BigQuery] permissions. A successful [!DNL Google] sign-in also does not grant dataset access, because [!DNL Google Cloud] IAM controls access to your data.

## Prerequisites {#prerequisites}

Before you begin, make sure that you have the following:

* **For [!DNL Google Cloud] preparation:** A [!DNL Google Cloud] administrator who can enable APIs, grant IAM roles, and create an OAuth client in the [!DNL Google Auth Platform].
* **For organization setup:** An account with permission to manage organization connectors in Coworker. You also need the client ID and client secret of a [!DNL Google] OAuth web application client, or existing organization secrets that contain them.
* **For member sign-in:** A [!DNL Google] identity that the audience of the OAuth app allows and that has the required IAM roles.

Know the ID of the query project and the datasets that members should read. The query project runs query jobs and pays for them. The data can live in a different project, and the OAuth client can belong to a separate project too. For a pilot, one project can hold the OAuth client, the query jobs, and the datasets.

## Prepare [!DNL Google Cloud] {#prepare-google-cloud}

Before you configure the connector in Coworker, prepare your project and member access in [!DNL Google Cloud]. Creating the OAuth app and granting data access are separate tasks. Members who use the connector do not need permission to edit the OAuth app.

### Prepare the query project {#prepare-query-project}

A [!DNL Google Cloud] administrator prepares the project that runs query jobs:

1. In the [Google Cloud console](https://console.cloud.google.com/), select or create a project.
1. Enable the [!DNL BigQuery] API, if it is not already enabled. Enabling the API also enables the [!DNL BigQuery] remote MCP server.
1. Choose billing or the [BigQuery sandbox](https://docs.cloud.google.com/bigquery/docs/sandbox), and then set appropriate daily [custom query quotas](https://docs.cloud.google.com/bigquery/docs/custom-quotas) on the query project.

>[!IMPORTANT]
>
>Read-only queries can still incur charges. [!DNL BigQuery] costs depend on the bytes that a query scans, not on the number of rows it returns. A `LIMIT` clause controls the rows returned, but it does not generally reduce the scanned bytes. Use dry runs, explicit columns, partition filters, and daily query quotas to control costs.

For more information, see [Use the BigQuery remote MCP server](https://docs.cloud.google.com/bigquery/docs/use-bigquery-mcp) in the [!DNL Google Cloud] documentation.

### Grant IAM roles {#grant-iam-roles}

Grant the following roles to the [!DNL Google] identities of your members. Use a managed group where possible, and prefer dataset-level data access.

| Role | Where to grant it | Purpose |
| --- | --- | --- |
| [!UICONTROL MCP Tool User] (`roles/mcp.toolUser`) | The projects used for MCP calls | Make MCP tool calls. |
| [!UICONTROL BigQuery Job User] (`roles/bigquery.jobUser`) | The query project | Run query jobs. |
| [!UICONTROL BigQuery Data Viewer] (`roles/bigquery.dataViewer`) | The authorized datasets or data projects | Read data and metadata. |

Do not grant [!UICONTROL BigQuery Data Editor], [!UICONTROL BigQuery Data Owner], or [!UICONTROL BigQuery Admin] only to use this read-only connector. As an additional safeguard, consider a [deny policy for read-write MCP tools](https://docs.cloud.google.com/mcp/prevent-read-write-tool-use). Ask your [!DNL Google Cloud] administrator to review the scope of the deny policy first, because it can affect other [!DNL Google] MCP clients and services. For more information, see [BigQuery IAM roles and permissions](https://docs.cloud.google.com/bigquery/docs/access-control).

## Configure the connector for your organization {#configure-organization}

Administrators make the [!DNL Google BigQuery] connector available to everyone in the organization. Changes on the organization page apply to all users in your organization.

1. Open **[!UICONTROL Customizations]**, select **[!UICONTROL Org]**, and then select **[!UICONTROL External Connectors]**. On the **[!UICONTROL Google BigQuery]** card, select **[!UICONTROL Configure]**.

   If the connector is already configured, the card shows **[!UICONTROL View configuration]** instead.

1. In the **[!UICONTROL Configure Google BigQuery for your organization]** dialog, copy the **[!UICONTROL Redirect URL]** under **[!UICONTROL Your Google application]**.

   The redirect URL differs between environments and regions, so always copy the exact value from the dialog. Do not use the URL of the Coworker page in your browser or the [!DNL BigQuery] MCP server URL. If one OAuth client serves several environments, register each required redirect URL separately.

1. In the [Google Auth Platform](https://console.cloud.google.com/auth/overview), prepare the OAuth client of your organization:

   1. Configure **[!UICONTROL Branding]** and **[!UICONTROL Audience]**. For an external app in testing, add the intended members as test users. Complete the publication and verification requirements of [!DNL Google] before broader use.
   1. In **[!UICONTROL Data Access]**, add the `https://www.googleapis.com/auth/bigquery` scope.
   1. Under **[!UICONTROL Clients]**, create or select an OAuth client with the **[!UICONTROL Web application]** application type.
   1. Add the redirect URL that you copied to **[!UICONTROL Authorized redirect URIs]**.
   1. Get the **[!UICONTROL Client ID]** and **[!UICONTROL Client secret]** through the approved secret-handling process of your organization.

   Members authorize this app that your organization owns, not an app that Adobe provides. Keep the client secret out of screenshots, chats, and documentation.

1. Under **[!UICONTROL Where the credentials come from]**, select one of the following options:

   * **[!UICONTROL Enter new]:** Enter the **[!UICONTROL Google OAuth client ID]** and the **[!UICONTROL Google OAuth client secret]**. Coworker stores the values that you enter as organization secrets.
   * **[!UICONTROL Use an existing secret]:** Select the saved organization secrets that contain the client ID and client secret.

   Do not use personal secrets for an organization connector.

1. Expand the **[!UICONTROL Explore and query]** tool group. Keep all seven tools selected, or select only the tools your members need. You must select at least one tool. For more information, see [Available tools](#available-tools).

1. Review the notices under **[!UICONTROL Access and permissions]**:

   * **[!UICONTROL Read-only tools]:** The OAuth scope is broad and does not prevent changes on its own. Keep the IAM roles of your members read-only.
   * **[!UICONTROL Read-only queries can incur charges]:** Use dry runs and query quotas. A `LIMIT` clause controls the rows returned, not necessarily the bytes scanned.
   * **[!UICONTROL Each person signs in separately]:** Every member needs the required IAM roles.

1. Select **[!UICONTROL Save connection]**.

   The organization card shows **[!UICONTROL Configuration saved]** and **[!UICONTROL View configuration]**.

Saving the configuration does not sign in you or any member to [!DNL Google]. Saving also does not confirm that anyone can query a dataset. To use the connector yourself, follow the steps in [Sign in as a member](#sign-in-as-a-member).

### Available tools {#available-tools}

The [!DNL Google BigQuery] connector provides the following read-only tools:

| Tool | Description |
| --- | --- |
| `list_dataset_ids` | List the datasets in a project that you specify. |
| `get_dataset_info` | Read the metadata of a dataset. |
| `list_table_ids` | List the tables and views in a dataset. |
| `get_table_info` | Read the schema and metadata of a table. |
| `execute_sql_readonly` | Run read-only SQL queries, or a dry run to estimate the bytes a query scans. |
| `get_query_results` | Retrieve the results of a query, or check a long-running query. |
| `get_job` | Check the status, errors, and statistics of a query job. |

For query workflows, keep `execute_sql_readonly`, `get_query_results`, and `get_job` selected together, so that Coworker can follow a long-running query job. Coworker does not offer the `execute_sql` and `cancel_job` tools from the [!DNL BigQuery] MCP server. Tools that [!DNL Google] adds to the server later are not enabled automatically. For tool details, see the [BigQuery MCP reference](https://docs.cloud.google.com/bigquery/docs/reference/mcp).

Consider the following limits when you use the tools:

* [!DNL Google] documents a limit of 3,000 rows for query results and a default query timeout of three minutes. Do not use the connector to export full tables.
* The tools cannot list projects. Provide a known project ID in your request.
* Read-only SQL does not support statements that change data or resources, or queries on [!DNL Google Drive] external tables.
* Query results, schemas, dataset access lists, and SQL can appear in the chat. Make sure that access follows the data-handling policy of your organization.

## Sign in as a member {#sign-in-as-a-member}

After an administrator configures the connector, each member signs in with their own [!DNL Google] account. You do not need the OAuth client secret to sign in.

1. Open **[!UICONTROL Customizations]**, select **[!UICONTROL User]**, and then select **[!UICONTROL External Connectors]**. On the **[!UICONTROL Google BigQuery]** card, select **[!UICONTROL Sign in]**.

   If the card says that an administrator needs to set up the connector, ask your administrator to [configure the connector](#configure-organization).

1. Choose the [!DNL Google] account that has the required IAM access. Then complete any sign-in steps that your organization requires, such as single sign-on (SSO) or multi-factor authentication (MFA).

   This account can differ from the account that you use for Coworker.

1. If [!DNL Google] shows **[!UICONTROL Google hasn't verified this app]**, confirm the app and its owner with your administrator. Continue only if your organization policy for test apps allows it. Otherwise, select **[!UICONTROL Back to safety]**, and ask the app owner to resolve the audience, publication, or verification requirements.

1. Review the app name and the requested access on the consent screen. Then complete the [!DNL Google] consent flow.

   [!DNL Google] asks for permission to view and manage your [!DNL BigQuery] data and to see the email address of your [!DNL Google] account. This is the standard [!DNL BigQuery] scope, even though Coworker offers only read-only tools.

   >[!IMPORTANT]
   >
   >Continue only if you recognize the app and your organization approves the requested access.

1. Return to Coworker, and then review **[!UICONTROL Tools enabled by your admin]** in the connector details. Members can view the tools but cannot change the tool selection.

1. Optionally, select **[!UICONTROL Test]** to check the connection.

A successful sign-in, test, or tool list does not confirm that you can query a specific dataset. To confirm your access, [check your BigQuery access](#check-bigquery-access). If Coworker says that the connection has ended, sign in again.

## Check your [!DNL BigQuery] access {#check-bigquery-access}

To confirm that you can read your data, start a new chat and enter a read-only prompt. Replace the placeholders with projects and tables that your [!DNL Google] identity can access.

Example prompts:

* "List the datasets in project `YOUR_PROJECT_ID`."
* "Using `YOUR_QUERY_PROJECT_ID` for query jobs, inspect the schema of `YOUR_DATA_PROJECT.YOUR_DATASET.YOUR_TABLE`, estimate the scan with a dry run, then return an aggregate summary."

Confirm that the results include the datasets or data you expect. Prefer explicit columns, aggregates, and partition filters over requests for raw table contents. Naming a project in a request does not change your signed-in identity or grant you access to that project.

## Troubleshoot access {#troubleshoot-access}

If sign-in or access fails, check the following with your administrator:

| Issue | What to check |
| --- | --- |
| The card says that the connector is not configured, or that an administrator needs to set it up | The organization configuration is saved for your active organization. |
| `redirect_uri_mismatch` | The exact **[!UICONTROL Redirect URL]** from the Coworker dialog is registered in **[!UICONTROL Authorized redirect URIs]** on the web application client. |
| `invalid_client` | The client ID and client secret belong to the web application client, and the selected organization secrets are correct. |
| `access_denied`, or a warning that [!DNL Google] has not verified the app | The app owner checks the audience, test user eligibility, and verification status. Do not approve an app that you do not recognize. |
| The connection has ended, or the token has expired | Sign in again as a member. |
| Permission denied for `mcp.tools.call` | The [!UICONTROL MCP Tool User] role, and any IAM deny policy that applies. |
| Permission denied for `bigquery.jobs.create` | The [!UICONTROL BigQuery Job User] role on the query project. |
| Access denied for a table | The [!UICONTROL BigQuery Data Viewer] role on the dataset, and the [!DNL Google] account you signed in with. |
| `SERVICE_DISABLED` | The [!DNL BigQuery] API is enabled in the project that the error identifies. |
| The daily query quota is exceeded | The query quota of the project, with the project administrator. |
| A request to insert, update, delete, create, or drop data fails | The connector is read-only and does not support changes to data or resources. |

When you contact support, do not share client secrets, access tokens, authorization codes, or customer data.
