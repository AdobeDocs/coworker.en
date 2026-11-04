---
title: Access Control for Coworker
description: Learn about access control for Adobe CX Enterprise Coworker and permissions in connected Adobe products. Find administrator controls and get help with access.
last-substantial-update: 2026-11-04
level: beginner
role: Admin
jira: KT-22980
product_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: Coworker
---
# Access control for Coworker {#access-control}

Use Adobe CX Enterprise Coworker access control to manage who can use Coworker and which capabilities they can use.

## How access is determined {#how-access-is-determined}

Coworker access is controlled by an organization-wide setting and optional user or group overrides. The organization-wide setting enables or disables Coworker access for users in your organization. Access is enabled for everyone by default. Users must already have a Coworker license to access Coworker. Enabling access does not assign a license.

| Setting | How it affects access |
| --- | --- |
| Organization-wide setting | Enable Coworker access for everyone or disable it for your organization. The default policy allows read, write, and destructive MCP operations. |
| User or group override | Enable activates access for a user or group. Disable blocks Coworker access and takes precedence over any grant. Inherit clears the override and uses the applicable group or organization-wide setting. |
| Connected application permissions | The access users have in the Adobe applications connected to Coworker. |

User groups do not sync with your IMS organization. Custom roles are not available.

Coworker inherits your user permissions from the Adobe applications you connect. Coworker respects your access in those applications.

## Add Coworker admins {#add-coworker-admins}

Before managing Coworker access, assign each Coworker admin the **[!UICONTROL Admin]** role for [!DNL Adobe Experience Platform] in [!DNL Adobe Admin Console].

Use this video to learn how to add Coworker admins.

>[!VIDEO](https://video.tv.adobe.com/v/3507041?learn=on)

## Manage user access {#manage-user-access}

1. Open the standalone Coworker experience. For instructions, see [Sign in to Coworker](/help/chat/ui-guide.md#sign-in).
1. Open the profile menu and select **[!UICONTROL Admin settings]**.

   ![Coworker home with the profile menu control highlighted.](./assets/access-control/coworker-home.png)

   ![Coworker profile menu with Admin settings highlighted.](./assets/access-control/admin-settings.png)

1. Select **[!UICONTROL Access control]**.

   ![Admin settings with the Access control card highlighted.](./assets/access-control/access-control.png)

   Use this video to learn how to manage Coworker users.

   >[!VIDEO](https://video.tv.adobe.com/v/3507151?learn=on)

1. Use **[!UICONTROL Users]** and **[!UICONTROL User groups]** to review or change settings that override the organization-wide default.

   The Users list includes users in your organization. Coworker access is enabled for these users by default, but each user must already have a Coworker license.

   Access overrides have three states:

   * **Allow:** Select **[!UICONTROL Enable]** to make the user or group status active. Allow applies only to users with an existing Coworker license.
   * **Deny:** Select **[!UICONTROL Disable]** to make the user or group status inactive. This blocks all Coworker access and takes precedence over any grant.
   * **Inherit:** Clear the override to use the applicable group or organization-wide setting.

   Changes may take a short time to take effect.

## Connected application permissions {#connected-application-permissions}

Connected Adobe products continue to enforce their own permissions. These products include Adobe Experience Platform, Adobe Journey Optimizer, [!DNL Adobe Workfront], and [!DNL Adobe Experience Manager].

If you cannot perform an action in a connected product, using Coworker does not grant you that permission.

If you do not have permission to access a dataset in Adobe Experience Platform, Coworker cannot retrieve it or act on it for you.

## Get help with access {#get-help-with-access}

If you do not see [!UICONTROL Access control], contact your Adobe administrator or Adobe representative. They can confirm whether the feature is enabled for your organization and whether you have access to its settings.

If you are denied access, ask your administrator to review the organization-wide default and any user or group settings. For a connected application, ask them to check the permissions managed separately for that application.

## More help on this topic {#more-help}

Use these resources for more information about Coworker and administration.

* [Coworker Chat overview](/help/chat/overview.md)
* [Get started with Coworker Chat](/help/chat/ui-guide.md)
* [Manage plugins and marketplaces](/help/customizations/plugins/manage-plugins-for-your-org.md)
