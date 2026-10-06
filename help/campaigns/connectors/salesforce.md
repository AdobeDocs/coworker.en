---
description: Description.
title: Connect to Salesforce
product_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: CX Enterprise Coworker
feature_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: CX Enterprise Coworker
---
# Connect to Salesforce {#salesforce}

Adobe Coworker Campaigns allows you to connect your Salesforce account to access your leads and contacts.

>[!PREREQUISITES]
>
>To use this connector, you must first have:
>
>* An active Salesforce account
>* The following permissions in Salesforce: `api`, `sobjects.Contact.read`, `sobjects.Campaign.read`, `sobjects.CampaignMember.read`
>* Your Salesforce Instance URL, [Client ID, and Client secret](https://help.salesforce.com/s/articleView?id=xcloud.remoteaccess_oauth_client_credentials_flow.htm&type=5#:~:text=DESCRIPTION-,client_id,-The%20consumer%20key) handy

## How to connect

1. On the [Coworker Campaigns homepage](https://coworker-campaigns.experience.adobe.com/), click **Customize** and select **Connectors**.

   ![Coworker Campaigns left navigation with Customize expanded and Connectors highlighted](./assets/salesforce-1.png)

1. Click **Add integration**.

   ![Add integration button in the Connectors screen](./assets/salesforce-2.png)

   >[!NOTE]
   >
   >If this is not your first integration, the button will read "Add connector."

1. In the Salesforce row, click **Connect**.

   ![](./assets/salesforce-3.png)

1. Enter your Salesforce **instance URL**, **Client ID**, and **Client secret**. Click **Connect**.

   >[!NOTE]
   >
   >* In Salesforce, Client ID = Consumer Key and Client secret = Consumer Secret.
   >
   >* While in your Salesforce account, you can find your Instance URL in your browser's address bar, or by navigating to **Setup** > **Company Settings** > **My Domain**.

   ![](./assets/salesforce-4.png)

After connection, Salesforce appears in the Connectors list and can be selected when linking a lead or contact list to sync from Salesforce.

**To disconnect:**

1. In the Connectors screen, find the Salesforce tile and click **Manage**.

   ![](./assets/salesforce-5.png)

1. Click **Disconnect** (no need to re-enter your Client secret at this time).

   ![](./assets/salesforce-6.png)

1. Click **Disconnect** again to confirm.

   ![](./assets/salesforce-7.png)
