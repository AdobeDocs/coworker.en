---
description: Coworker for teams allows you to connect and query Unity Catalog tables in your Databricks workspace to build and activate campaign audiences.
title: Connect to Databricks
product_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: CX Enterprise Coworker
---
# Connect to Databricks {#databricks}

Coworker for teams allows you to connect and query Unity Catalog tables in your Databricks workspace to build and activate campaign audiences.

>[!PREREQUISITES]
>
>To use this connector, you must first have:
>
>* An active Databricks account
>* Your Databricks Workspace host, [SQL warehouse path](https://docs.databricks.com/aws/en/compute/sql-warehouse/create){target="_blank"}, [Personal access token](https://learn.microsoft.com/en-us/azure/databricks/dev-tools/auth/pat){target="_blank"}, and [Unity Catalogs](https://learn.microsoft.com/en-us/azure/databricks/discover/database-objects){target="_blank"} handy.

## How to connect

1. On the [Coworker for teams homepage](https://coworker-campaigns.experience.adobe.com/){target="_blank"}, click **Context** and select **Connectors**.

   ![Coworker for teams left navigation with Context expanded and Connectors highlighted](./assets/databricks-1.png)

1. Click **Add integration**.

   ![Add integration button in the Connectors screen](./assets/databricks-2.png)

   >[!NOTE]
   >
   >If this is not your first integration, the button will read "Add connector."

1. In the Databricks row, click **Connect**.

   ![Databricks connector tile with the Connect button](./assets/databricks-3.png)

1. Enter your Databricks **Workspace host**, **SQL warehouse path**, **Personal access token**, and **Unity catalogs**. Click **Connect**.

   >[!NOTE]
   >
   >When on your Databricks homepage, the Workspace host can be found directly in your browser's address bar. To locate all other credentials, see the links in **Prerequisites** at the top of this article.

   ![Connect Databricks dialog with fields for Workspace host, SQL warehouse path, Personal access token, and Unity catalogs](./assets/databricks-4.png)

After connection, Databricks appears in the Connectors list.

**To disconnect:**

1. In the Connectors screen, find the Databricks tile and click **Manage**.

1. Click **Disconnect** (no need to re-enter your Personal access token at this time).

1. Click **Disconnect** again to confirm.
