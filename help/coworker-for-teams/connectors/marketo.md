---
description: Learn how to connect your Marketo Engage account to Coworker for teams so you can sync Marketo smart and static lists.
title: Connect to Marketo Engage
product_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: CX Enterprise Coworker
feature_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: CX Enterprise Coworker
---
# Connect to Marketo Engage {#marketo}

Adobe Coworker for teams allows you to connect your Marketo Engage account to pull in smart and static lists.

>[!PREREQUISITES]
>
>To use this connector, you must first have:
>
>* An active Marketo Engage account
>* Your Marketo **instance URL**
>* A [custom service](https://experienceleague.adobe.com/en/docs/marketo-developer/marketo/rest/custom-services#custom-services-1) created for Coworker for teams in Marketo, with its [Client ID and Client secret](https://experienceleague.adobe.com/en/docs/marketo-developer/marketo/rest/authentication#creating-an-access-token) on hand

## How to connect

1. On the [Coworker for teams homepage](https://coworker-campaigns.experience.adobe.com/), click **Customize** and select **Connectors**.

   ![Coworker for teams left navigation with Customize expanded and Connectors highlighted](./assets/marketo-1.png)

1. Click **Add integration**.

   ![Add integration button in the Connectors screen](./assets/marketo-2.png)

   >[!NOTE]
   >
   >If this is not your first integration, the button will read "Add connector."

1. In the Marketo row, click **Connect**.

   ![Marketo connector tile with the Connect button](./assets/marketo-3.png)

1. Enter your Marketo **instance URL**, **Client ID**, and **Client secret**. Click **Connect**.

   >[!NOTE]
   >
   >You can find your Marketo instance URL in your browser's address bar when viewing your My Marketo page.

   ![Connect Marketo dialog with fields for instance URL, Client ID, and Client secret](./assets/marketo-4.png)

After connection, Marketo appears in the Connectors list and can be selected when linking a contact list to sync from Marketo.

**To disconnect:**

1. In the Connectors screen, find the Marketo tile and click **Manage**.

   ![Connectors screen with the Marketo tile showing a Connected status and Manage button](./assets/marketo-5.png)

1. Click **Disconnect** (no need to re-enter your Client secret at this time).

   ![Manage Marketo dialog with instance URL and Client ID fields and a Disconnect button](./assets/marketo-6.png)

   >[!NOTE]
   >
   >After the instance URL is first added, it defaults to the REST endpoint URL, ending in `*.mktorest.com`.

1. Click **Disconnect** again to confirm.

   ![Disconnect connection confirmation dialog](./assets/marketo-7.png)
