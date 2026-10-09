---
description: Description goes here.
title: Subdomain
product_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: CX Enterprise Coworker
feature_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: CX Enterprise Coworker
---
# Add a subdomain and senders {#subdomain-senders}

A subdomain is a division of your domain that can be used to isolate your brands, or various types of traffic (for example, marketing communications).

For example, let's use the "mybrand.com" domain, which is used by your team to send marketing communications. In this situation, you can set up a specific subdomain: "marketing.mybrand.com."

By doing so, you will help preserve the reputation of your domain and other subdomains. For example, if the "marketing.mybrand.com" subdomain ended up being added an Internet Service Provider's block list due to bad deliverability practices, this would prevent the whole "mybrand.com" domain and any other subdomains you created from being added.

>[!IMPORTANT]
>
>As part of the free trial, there are a maximum of two subdomains allowed.

## How to add a subdomain

1. On the bottom of the left nav, click on your name.

   SCREENSHOT

1. Click **Settings**.

   SCREENSHOT

1. Under _Workspace_, select **Domains & senders**.

   SCREENSHOT

1. Click **Add subdomain**.

   SCREENSHOT

1. Enter your subdomain and click **Next**.

   SCREENSHOT

1. Click the copy icon PIC next to the applicable values you need to add to your DNS provider.

   SCREENSHOT

   >[!NOTE]
   >
   >If your DNS provider allows you to bulk upload the fields, you can click **Export CSV** to export all fields.

1. When you are done entering the information in your DNS provider, click **I've added these records** in Coworker Campaigns to continue.

   SCREENSHOT

   >[!NOTE]
   >
   >DNS changes can take up to 30 minutes to propagate. If you see a red X instead of a green check in any of the rows, Coworker Campaigns will check every two minutes until completed.

1. When all records are validated, a _Validation record_ table appears at the bottom of the window. Scroll down and copy all listed values and add them to your DNS provider.

   SCREENSHOT

1. When done, click **I've added this record** (or **these records** if there are multiple) in Coworker Campaigns to continue.

   SCREENSHOT

1. Enter your Sender name, Email prefix, Reply-to name, and Reply-to email, and click **Finish and set up**.

   SCREENSHOT

1. Your new subdomain appears in the list. Its status reads _In progress_, as it can take anywhere from a few minutes to two hours for the process to be completed.

   SCREENSHOT

1. When the process is completed, the status changes to _Verified_.

   SCREENSHOT

## How to add a sender

Text

