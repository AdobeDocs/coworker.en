---
description: Connect your HubSpot account to Coworker for teams using a service key to sync contact lists, then manage or disconnect the integration anytime.
title: Connect to HubSpot
product_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: CX Enterprise Coworker
---
# Connect to HubSpot {#hubspot}

Adobe Coworker for teams allows you to connect your HubSpot account to pull in contact lists.

>[!PREREQUISITES]
>
>To use this connector, you must first have:
>
>* An active HubSpot account
>* A [service key](https://developers.hubspot.com/docs/apps/developer-platform/build-apps/authentication/account-service-keys#create-a-service-key) created with the following scopes added: `crm.objects.contacts.read`, `crm.objects.leads.read`, `crm.schemas.contacts.read`, `crm.lists.read`, `crm.export`

## How to connect

1. On the [Coworker for teams homepage](https://coworker-campaigns.experience.adobe.com/), click **Context** and select **Connectors**.

   ![Customize menu expanded in the sidebar with Connectors selected](./assets/hubspot-1.png)

1. Click **Add integration**.

   ![Add integration button on the Connectors screen](./assets/hubspot-2.png)

   >[!NOTE]
   >
   >If this is not your first integration, the button will read "Add connector."

1. In the HubSpot row, click **Connect**.

   ![HubSpot tile with the Connect button highlighted](./assets/hubspot-3.png)

1. A modal appears showing the necessary permissions (listed in the Prerequisites at the top of this article). Click **Continue**.

1. Enter your HubSpot **Service key** and click **Connect**.

   ![Connect HubSpot dialog with the Service key field and Connect button](./assets/hubspot-4.png)

After connection, HubSpot appears in the Connectors list and can be selected when linking a contact list to sync from HubSpot.

**To disconnect:**

1. In the Connectors screen, find the HubSpot tile and click **Manage**.

   ![Connectors screen showing HubSpot connected with the Manage button highlighted](./assets/hubspot-5.png)

1. Click **Disconnect** (no need to re-enter your service key at this time).

   ![Manage HubSpot dialog with the Disconnect button highlighted](./assets/hubspot-6.png)

1. Click **Disconnect** again to confirm.

   ![Disconnect connection confirmation dialog with the Disconnect button highlighted](./assets/hubspot-7.png)
