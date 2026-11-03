---
title: Access Control for Coworker
description: Learn about access control for Adobe CX Enterprise Coworker and permissions in connected Adobe products. Find administrator controls and get help with access.
role: Admin
product_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: CX Enterprise Coworker
---
# Access control for Coworker {#access-control}

Use Adobe CX Enterprise Coworker access control to manage who can use Coworker and which capabilities they can use.

## How access is determined {#how-access-is-determined}

Coworker starts with an organization-wide default.

| Access type | What it determines |
| --- | --- |
| Organization-wide default | Provides access for everyone and allows read, write, and destructive MCP operations. |
| User and group settings | Override the organization-wide default for individual users or groups. |
| Connected application permissions | Which data and actions a user can access in connected Adobe products. Coworker does not grant additional product permissions. |

Read-only mode and entity deletion settings are in **[!UICONTROL Customizations]** > **[!UICONTROL Org]** > **[!UICONTROL General]**. Custom roles are not available.

Coworker access works alongside permissions in the Adobe products you connect to. A person who can open Coworker might still need additional permissions for a connected application.

## Manage access {#manage-access}

Only organization admins can manage Access control settings.

1. Open the standalone Coworker experience. For instructions, see [Sign in to Coworker](/help/chat/ui-guide.md#sign-in).
1. Open the profile menu and select **[!UICONTROL Admin settings]**.

   ![Coworker home with the profile menu control highlighted.](./assets/access-control/coworker-home.png)

   ![Coworker profile menu with Admin settings highlighted.](./assets/access-control/admin-settings.png)

1. Select **[!UICONTROL Access control]**.

   ![Admin settings with the Access control card highlighted.](./assets/access-control/access-control.png)

1. Use **[!UICONTROL Users]** and **[!UICONTROL User groups]** to review or change settings that override the organization-wide default.

   Access settings have three states:

   * **[!UICONTROL Allow]** grants access only to people who already have a Coworker license. It does not assign a license.
   * **[!UICONTROL Deny]** blocks all Coworker access and takes precedence over any grant.
   * **[!UICONTROL Inherit]** clears the override so the applicable group setting or organization-wide default determines access.

   Changes take effect after a short propagation delay.

1. To manage read-only mode or entity deletion, go to **[!UICONTROL Customizations]** > **[!UICONTROL Org]** > **[!UICONTROL General]**.

## Connected application permissions {#connected-application-permissions}

Connected Adobe products continue to enforce their own permissions. These products include Adobe Experience Platform, Adobe Journey Optimizer, [!DNL Adobe Workfront], and [!DNL Adobe Experience Manager].

If you cannot perform an action in a connected product, using Coworker does not grant you that permission.

In [!DNL Workfront], access levels, object permissions, and system preferences may also affect the Coworker panel and available actions. For details, see [Use CX Enterprise Coworker in Workfront](https://experienceleague.adobe.com/en/docs/workfront/using/basics/coworker-in-workfront/use-coworker-in-workfront){target="_blank"}.

## Get help with access {#get-help-with-access}

If you do not see [!UICONTROL Access control], contact your Adobe administrator or Adobe representative. They can confirm whether the feature is enabled for your organization and whether you have access to its settings.

If you are denied access, ask your administrator to review the organization-wide default and any user or group settings. For a connected application, ask them to check the permissions managed separately for that application.

## More help on this topic {#more-help}

Use these resources for more information about Coworker and administration.

* [Coworker Chat overview](/help/chat/overview.md)
* [Get started with Coworker Chat](/help/chat/ui-guide.md)
* [Manage plugins and marketplaces](/help/customizations/plugins/manage-plugins-for-your-org.md)
