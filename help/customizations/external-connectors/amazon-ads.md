---
title: Amazon Ads External Connector
description: Learn how to set up the Amazon Ads external connector in CX Enterprise Coworker for your organization and sign in with Amazon to use Amazon Ads tools in chat.
role: Admin, User
level: Beginner
badgeBeta: label="Beta" type="Informative" tooltip="This connector is in beta."
product_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: CX Enterprise Coworker
hide: true
---

# Amazon Ads external connector {#amazon-ads}

Use the [!DNL Amazon Ads] external connector to work with your [!DNL Amazon Ads] data in Adobe CX Enterprise Coworker. After you set up the connector, ask Coworker which advertising accounts you can access, and review campaigns, reports, billing, and other account information. The connector is a Model Context Protocol (MCP) server hosted by [!DNL Amazon].

>[!AVAILABILITY]
>
>The [!DNL Amazon Ads] external connector is in beta. The documentation and the functionality are subject to change.

## Connector configuration {#connector-configuration}

The connector configuration process has two separate parts:

* **Organization setup:** An administrator configures the connector once for the whole organization. The administrator chooses the [!DNL Amazon Ads] region and the OAuth application, and selects the tools that members can use.
* **Member sign-in:** Each member signs in with their own [!DNL Amazon] account. Members can access only the advertising accounts that their [!DNL Amazon] account has permission to use.

Saving the organization configuration does not sign in any members or grant access to advertising accounts. Each member must sign in separately.

## Prerequisites {#prerequisites}

Before you begin, make sure that you have the following:

* **For organization setup:** An account with permission to manage organization connectors in Coworker, and the [!DNL Amazon Ads] region of the advertising accounts you plan to use.
* **For member sign-in:** An [!DNL Amazon] account that has accepted an invitation to the advertising accounts you plan to use, with the permissions those tasks require. For more information, see [Add or remove users from your account](https://advertising.amazon.com/help/GDQVHVQMY9F88PCA) and [Manage users in a Manager account](https://advertising.amazon.com/help/G4M4JGKGV2VAY9JC) in the [!DNL Amazon Ads] documentation.
* **For your own OAuth app (optional):** A [!DNL Login with Amazon] app that is approved for the [!DNL Amazon Ads] API, its OAuth client ID and client secret, and permission to edit the app security profile. A security profile on its own does not grant [!DNL Amazon Ads] API approval. For more information, see [Connecting to the Ads MCP Server using OAuth](https://advertising.amazon.com/API/docs/en-us/mcp/oauth) in the [!DNL Amazon Ads] documentation.

## Configure the connector for your organization {#configure-organization}

Administrators make the [!DNL Amazon Ads] connector available to everyone in the organization. Changes on the organization page apply to all users in your organization.

1. Open **[!UICONTROL Customizations]**, select **[!UICONTROL Org]**, and then select **[!UICONTROL External Connectors]**. On the **[!UICONTROL Amazon Ads]** card, select **[!UICONTROL Configure]**.

   After you save the configuration, the card shows **[!UICONTROL Configuration saved]**, and **[!UICONTROL Configure]** changes to **[!UICONTROL View configuration]**.

   ![External Connectors page for the organization, showing the Amazon Ads card with a Beta label, a Configuration saved status, and a View configuration button.](./assets/amazon-ads/org-catalog.png){width="700" zoomable="yes"}

1. In the **[!UICONTROL Configure Amazon Ads for your organization]** dialog, under **[!UICONTROL Connection details]**, select the **[!UICONTROL Amazon Ads region]** that matches your advertising accounts. Coworker shows the MCP server URL for the region below the selection.

   | Region | MCP server URL |
   | --- | --- |
   | [!UICONTROL North America] | `https://advertising-ai.amazon.com/mcp` |
   | [!UICONTROL Europe] | `https://advertising-ai-eu.amazon.com/mcp` |
   | [!UICONTROL Far East] | `https://advertising-ai-fe.amazon.com/mcp` |

   Each organization can have one [!DNL Amazon Ads] connection in one region. To switch regions later, remove the connection and set it up again. Every member then needs to sign in again.

1. Select an **[!UICONTROL OAuth application]**:

   * **[!UICONTROL Adobe-managed OAuth application]:** Adobe provides the [!DNL Amazon Ads] app, so you do not need to enter app credentials. Each member still signs in with their own [!DNL Amazon] account after you save.

     ![Configure Amazon Ads for your organization dialog with the North America region, the Adobe-managed OAuth application selected, and the collapsed tool groups.](./assets/amazon-ads/org-configure.png){width="500" zoomable="yes"}

   * **[!UICONTROL Use my own OAuth application]:** Your organization provides its own [!DNL Login with Amazon] app. Members authorize your app, not the Adobe app. Under **[!UICONTROL Your Amazon application]**, complete the following steps:

     1. Copy the **[!UICONTROL Redirect URL]**. Use the exact value shown in the dialog, because the redirect URL differs between environments.
     1. In the [Login with Amazon console](https://developer.amazon.com/loginwithamazon/console/site/lwa/overview.html), open the web settings of the app security profile. Add the redirect URL to **[!UICONTROL Allowed Return URLs]**, and keep any existing URLs. For more information, see [Register for Login with Amazon](https://developer.amazon.com/docs/login-with-amazon/register-web.html) in the [!DNL Amazon] documentation.
     1. Enter the **[!UICONTROL Amazon app ID]** and **[!UICONTROL Amazon app secret]** from the same security profile. The **[!UICONTROL Amazon app ID]** field takes the OAuth client ID, not an advertiser ID, a manager account ID, or the [!DNL Amazon] application ID. Coworker stores the credentials as organization secrets. To reuse saved credentials for the same app instead, select **[!UICONTROL Use an existing secret]**, and then select the **[!UICONTROL Secret holding the app ID]** and the **[!UICONTROL Secret holding the app secret]**.

1. Under **[!UICONTROL Tools available to users]**, expand each tool group and select the tools your organization needs. By default, only the two account tools in the **[!UICONTROL Accounts and organization]** group are selected. To change all tools at once, use **[!UICONTROL Select all]** or **[!UICONTROL Clear all]**. You must select at least one tool. For more information, see [Tool groups](#tool-groups). Then select **[!UICONTROL Save connection]**.

1. Review the saved **[!UICONTROL amazon-ads]** connector details.

   | Setting | Description |
   | --- | --- |
   | **[!UICONTROL Source]** | The MCP server URL for the region you selected. |
   | **[!UICONTROL Authentication]** | The authentication method, `amazon-ads_login`. |
   | **[!UICONTROL Connection]** | The OAuth application in use and your own sign-in status. |
   | **[!UICONTROL Tools]** | The tools selected for members, with **[!UICONTROL Select all]** and **[!UICONTROL Clear]** controls and a count of selected tools. |

   ![Saved amazon-ads connector details showing the North America source, the authentication method, a Signed in connection with Sign out and Refresh buttons, and two of 47 tools selected.](./assets/amazon-ads/org-details.png){width="700" zoomable="yes"}

The **[!UICONTROL Connection]** status on the connector details refers to your own connection, not to the organization. To use the connector yourself, follow the steps in [Sign in as a member](#sign-in-as-a-member). After you sign in, select **[!UICONTROL Test]** to check that Coworker can discover the connector tools. The result shows **[!UICONTROL Connection successful]** or **[!UICONTROL Connection failed]**, along with the tools or errors returned.

To change the tools available to members later, update the selection under **[!UICONTROL Available tools]**, and then select **[!UICONTROL Save tool selection]**. To stop offering the connector to your organization, select **[!UICONTROL Remove]** on the connector details page.

### Tool groups {#tool-groups}

The [!DNL Amazon Ads] connector organizes its tools into the following groups:

| Tool group | What the tools do |
| --- | --- |
| [!UICONTROL Campaign management and targeting] | Query campaigns, ad groups, ads, targets, and portfolios, and check product eligibility. |
| [!UICONTROL Accounts and organization] | List and get advertising accounts, and query advertiser, manager, and test account information. |
| [!UICONTROL User access and security] | List users, roles, permissions, and invitations. |
| [!UICONTROL Reporting and analytics] | Retrieve reports. |
| [!UICONTROL Amazon Marketing Cloud] | Read [!DNL Amazon Marketing Cloud] workflows, data sources, and the status of existing executions. |
| [!UICONTROL Billing and financial summaries] | Read invoices, invoice summaries, billing profile usage, and billing notifications. |
| [!UICONTROL Amazon Live] | Read [!DNL Amazon Live] channel, broadcast, livestream, and promotion information. |
| [!UICONTROL Eligibility and offers] | Read program and product eligibility, promotion offers, and rewards. |

For example, the [!UICONTROL Accounts and organization] group includes the `ads_accounts-list_ads_accounts` and `ads_accounts-get_ads_account` tools. The tools in each group can change as [!DNL Amazon] updates the connector. Tools that you leave unselected, and tools that the server adds later, are not available to members until you select them.

>[!IMPORTANT]
>
>Members authorize the connector with the `advertising::campaign_management` scope, which can allow changes to advertising accounts. When you test the connection, the tool list can include tools that the server returns beyond the setup list. Review each tool before you select it, and select only the tools that your organization intends members to use.

## Sign in as a member {#sign-in-as-a-member}

After an administrator configures the connector, each member signs in with their own [!DNL Amazon] account. You do not need an app secret or access token to sign in.

1. Open **[!UICONTROL Customizations]**, select **[!UICONTROL User]**, and then select **[!UICONTROL External Connectors]**. On the **[!UICONTROL Amazon Ads]** card, select **[!UICONTROL Sign in]**.

   If the card shows **[!UICONTROL Not configured]**, ask your administrator to [configure the connector](#configure-organization).

1. If your browser blocks the sign-in pop-up, allow it. Sign in to [!DNL Amazon] with the account that has access to your advertising accounts, and complete any required prompts, such as multi-factor authentication (MFA).

1. Review the app you are authorizing and the access it requests, and then approve the request.

   With the Adobe-managed app, you authorize the Adobe app. With your own organization app, you authorize that app instead, and the prompts can differ.

   >[!IMPORTANT]
   >
   >Continue only if you recognize the app and your organization approves the requested access.

1. After [!DNL Amazon] returns you to Coworker, confirm that the connector shows **[!UICONTROL Signed in]**. A closed pop-up alone does not confirm that sign-in succeeded.

1. Select **[!UICONTROL View details]**, and then review **[!UICONTROL Tools enabled by your admin]** to view the tools you can use.

1. Select **[!UICONTROL Test]** to check that Coworker can discover the connector tools.

To disconnect your [!DNL Amazon] account from the connector, select **[!UICONTROL Sign out]**.

A **[!UICONTROL Signed in]** status does not confirm access to a specific advertising account or that every tool runs successfully. When an administrator signs in, other members are not signed in. To confirm your access, [check your advertising account access](#check-account-access).

## Check your advertising account access {#check-account-access}

To confirm which advertising accounts you can use, start a chat and enter a read-only prompt.

Example prompt:

* "Using Amazon Ads, list up to five advertising accounts I can access. Show the account name, account ID, and region. Do not change anything."

If your administrator enabled the `ads_accounts-list_ads_accounts` tool, Coworker lists the advertising accounts you can access in the configured region. Choose an accessible account before you request campaign information or reports.

An empty account list does not always mean that the connector is not working. Check that you signed in with the invited [!DNL Amazon] account, that you accepted the invitation, and that your accounts are in the configured region. A test account without campaigns can also return an empty campaign list.

## Troubleshoot access {#troubleshoot-access}

If you cannot access your [!DNL Amazon Ads] data, check the following with your administrator:

| Area | What to check |
| --- | --- |
| Connector availability | If the **[!UICONTROL Amazon Ads]** card or **[!UICONTROL Configure]** is missing, confirm that your organization has access to the connector and that you have permission to manage organization connectors. |
| [!DNL Amazon] account | You signed in with the [!DNL Amazon] account that accepted the invitation to the advertising account. |
| Account permissions | Your [!DNL Amazon] account has the permissions that each task requires. If you use a manager account, confirm which linked advertisers your access covers. [!DNL Amazon Marketing Cloud] access is separate from campaign access. |
| Region | The configured region matches the region of your advertising accounts. |
| Enabled tools | Your administrator enabled the tools you need under **[!UICONTROL Tools available to users]**. By default, only the two account tools are enabled. |
| Redirect URL | For your own OAuth app, the **[!UICONTROL Allowed Return URLs]** in [!DNL Login with Amazon] include the exact **[!UICONTROL Redirect URL]** from the Coworker dialog, including the scheme, host, and path. Do not use a redirect URL from another environment or another MCP client. |
| App credentials | For your own OAuth app, the **[!UICONTROL Amazon app ID]** is the OAuth client ID, the app ID and app secret come from the same security profile, and the app is approved for the [!DNL Amazon Ads] API. |
| Adobe-managed app | If the configuration saves but sign-in fails, contact your Adobe representative to confirm that the Adobe-managed app is available in your environment. |
| Duplicate connector name | If **[!UICONTROL Test]** reports a personal connector with the same name, follow the guidance shown to remove or rename the personal connector, with the approval of its owner. |

When you contact support, include the error text, the time of the error, the selected region, and the OAuth application option. Do not share app secrets, access tokens, authorization codes, or customer account data.
