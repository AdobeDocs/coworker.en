---
title: Migrate Adobe Analytics Projects to Customer Journey Analytics
description: Use Coworker to validate, map, and migrate Adobe Analytics Workspace projects and their components to Customer Journey Analytics, then check migration status.
feature: AI Tools
role: Admin
level: Intermediate
product_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: CX Enterprise Coworker
---

# Migrate Adobe Analytics projects to Customer Journey Analytics with Coworker

<!-- FLAG: Confidence: High for the conversation flow, which is sourced from screenshots of the Coworker UI (October 2026) and the aa-mcp tool descriptions. The component migration tools run through the aa-mcp integration; there's no dedicated skill yet. Medium for statements that Coworker shares mappings and migration rules with migrations in the Adobe Analytics user interface; the user believes this is likely. Confirm with engineering. -->

Use Adobe CX Enterprise Coworker to migrate Adobe Analytics projects and their associated components to Customer Journey Analytics within a single conversation.

Coworker validates that the dimensions and metrics in your project are mapped to your Customer Journey Analytics data view, helps you map any that aren't, then re-creates the project in Customer Journey Analytics.

<!-- FLAG: Add the planned general availability date when it's confirmed. -->

>[!AVAILABILITY]
>
>The functionality described in this article is in the Limited Testing phase of release and might not be available yet in your environment. This note will be removed when the functionality is generally available.

>[!IMPORTANT]
>
>Before you migrate any projects, read [Prepare to migrate components and projects from Adobe Analytics to Customer Journey Analytics](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/component-migration/prepare-component-migration) in the Adobe Analytics documentation. It explains how to prepare for a migration, what's included, which elements cause errors, and how mappings affect your entire organization. This information applies to migrations in Coworker.

## Differences from migrating in the Adobe Analytics user interface

<!-- FLAG: Add rows as differences are confirmed. Who can migrate and How you migrate: SME Scott Tomko (October 2026); Coworker matches the Analytics 2.0 Component Migration APIs, and functionally both methods do much the same thing. Project owner: Coworker behavior is from a test conversation (October 2026); the Adobe Analytics user interface behavior is from component-migration.md in the Adobe Analytics docs. Mapping dimensions and metrics: Confidence Medium for the Coworker column, which is based on the aa-mcp tool descriptions and a test conversation, not on an observed failed validation. Confirm that Coworker suggests and updates mappings, and whether it asks for confirmation before it updates a mapping. The Adobe Analytics user interface behavior is from component-migration.md in the Adobe Analytics docs. -->

Migrating projects with Coworker differs from migrating them in the Adobe Analytics user interface in the following ways:

| | Coworker | Adobe Analytics user interface |
| --- | --- | --- |
| **Who can migrate projects** | Adobe Analytics administrators, and users with the [!UICONTROL **Component Migration**] permission | Adobe Analytics administrators only |
| **Project owner** | The user who is performing the migration | The user that you specify in the [!UICONTROL **Project owner**] field |
| **Mapping dimensions and metrics** | Coworker validates the project and lists how each dimension and metric is mapped. For any that can't be automatically mapped, Coworker suggests a dimension or metric in your data view and updates the mapping. | In the [!UICONTROL **Map schema**] section, you select each dimension or metric with a [!UICONTROL **Not mapped**] status and manually map it. |
| **How you migrate** | Describe what you want in a prompt. Coworker does the work, asking a few questions along the way. For example, Coworker can create a project with the components you name, then migrate it. See [Start from specific components](#start-from-specific-components). | Create a project in Analysis Workspace, add the components that you want to migrate, and save the project. Then, in [!UICONTROL **Component migration**], select the project, specify a project owner, map the schema for each report suite, and select [!UICONTROL **Migrate**]. |

## Prerequisites

<!-- FLAG: Confidence: High for the Adobe Analytics MCP and permission bullets, which come from the release announcement and SME Scott Tomko (October 2026): like the Analytics 2.0 Component Migration APIs, Coworker lets non-admins with the Component Migration permission migrate projects, while the Adobe Analytics UI is admin-only. Open question: Coworker makes the user who runs the migration the owner of the new project, but the aa-mcp tool description says the owner "should be an admin" and the Adobe Analytics component migration docs say the owner must be a Customer Journey Analytics administrator. Confirm whether a non-admin who runs a migration needs Customer Journey Analytics admin rights, or whether Coworker assigns a different owner. -->

To migrate projects with Coworker, you need:

* Access to the Adobe Analytics MCP. The component migration tools are enabled automatically for customers who have Adobe Analytics MCP access. To confirm that [!UICONTROL **aa-mcp**] is connected, see [Get started analyzing data with Coworker Chat](/help/chat/use-cases/data-insights/analytics-chat.md).

* Adobe Analytics administrator rights, or the [!UICONTROL **Component Migration**] permission in the Admin Console. You don't need to be an administrator.

* The [prerequisites](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/component-migration/prepare-component-migration#prerequisites) for component migration in the Adobe Analytics documentation.

* A project that uses base report suites. Virtual report suites can't be migrated.<!-- FLAG: Sourced from Coworker's response in the UI. The Adobe Analytics component migration docs don't mention virtual report suites. Confirm, and consider adding it to those docs. -->

## Review report suite mappings before you migrate

<!-- FLAG: Confidence: Medium. The recommendation to review mappings before the first migration from a report suite is inferred from the Adobe Analytics guidance to decide mappings as an organization; Coworker also validates mappings during each migration. Confirm with Scott. -->

Consider reviewing how a report suite's dimensions and metrics are mapped before your first migration from that report suite. Mappings apply to every project that your organization migrates, so settling them first helps later projects pass validation. For guidance on choosing mappings, see [Decide as an organization how you will map components](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/component-migration/prepare-component-migration#decide-as-an-organization-how-you-will-map-components) in the Adobe Analytics documentation.

To review mappings, select [!UICONTROL **Review mappings only**] on the [!UICONTROL **Scope**] tab, or ask Coworker directly:

**Prompts**

* "Show me how the dimensions and metrics in my report suite are mapped to my data view"
* "Which dimensions and metrics in my report suite aren't mapped to my data view?"

You can also ask Coworker to update mappings.

If you skip this review, Coworker still [checks the mappings for each project that you migrate](#review-the-validation-results-and-mappings).

## Start a migration

<!-- FLAG: Confidence: High that migration works at the project level and that components migrate with their project (component-migration.md in the Adobe Analytics docs), and that components that already exist in Customer Journey Analytics aren't re-created (prepare-component-migration.md). Medium-low for when to use each method and for combining them; this guidance is inferred and isn't in the Adobe Analytics docs. Confirm with Scott. Also confirm whether Coworker creates a project automatically when you ask it to migrate only components (for example, "Migrate my Spring sale segments to CJA"), or whether you must ask it to create the project. -->

Coworker always migrates a project and its associated components. To migrate specific components, ask Coworker to add them to a new project, then migrate that project.

Components that already exist in Customer Journey Analytics aren't re-created, so you can use both methods. For example, migrate your most important projects first, then migrate any remaining components. Choose where to start based on what you want in Customer Journey Analytics:

* **Migrate a project** when you want to keep the project's panels and visualizations in Customer Journey Analytics. See [Start from a project](#start-from-a-project).
* **Migrate specific components** when you want components such as segments, calculated metrics, or date ranges in Customer Journey Analytics, but don't need any of the projects that use them. For example, you might plan to build new projects in Customer Journey Analytics that include them. See [Start from specific components](#start-from-specific-components).

### Start from a project

To migrate a project and its associated components:

1. Sign in to Coworker.

1. Select **[!UICONTROL New chat]**.

1. In the text field, prompt Coworker to migrate your project. For example: 

   **Prompt**

   > I want to migrate components from Adobe Analytics to Customer Journey Analytics.

   Coworker describes what it can migrate and starts a questionnaire.

1. On the [!UICONTROL **Scope**] tab, select one of the following options, then select [!UICONTROL **Next**]:

   <!-- FLAG: Confidence: Medium for the "Plan a full upgrade" description. It likely hands off to the implementation guide skill and leaves the migration flow. Confirm with engineering. Also confirm what the Source & target tab asks; it was skipped in the screenshots. The Next and Submit buttons on the first questionnaire's Source & target and Review tabs are assumed to work like the second questionnaire. -->

   | Option | Description |
   | --- | --- |
   | [!UICONTROL **A specific AA project**] | Migrate a project that you name. Follow the remaining steps in this section. |
   | [!UICONTROL **Review mappings only**] | Check how a report suite's metrics and dimensions map to a data view, without migrating anything. See [Review report suite mappings before you migrate](#review-report-suite-mappings-before-you-migrate). |
   | [!UICONTROL **Plan a full upgrade**] | Get an end-to-end plan for moving from Adobe Analytics to Customer Journey Analytics. See [Plan your implementation with Coworker](/help/chat/use-cases/data-insights/implementation-guide.md). |

1. (Optional) Answer the questions on the [!UICONTROL **Source & target**] tab, then select [!UICONTROL **Next**].

1. On the [!UICONTROL **Review**] tab, confirm your answers, then select [!UICONTROL **Submit**].

   Coworker checks which Adobe Analytics companies you have access to and how many base report suites each one has, then starts a second questionnaire.

1. Answer the following questions, selecting [!UICONTROL **Next**] after each one:

   | Tab | Question | Additional context |
   | --- | --- | --- |
   | [!UICONTROL **Project**] | What is the name of the AA project you want to migrate? | A partial name is fine. |
   | [!UICONTROL **Report suite**] | Which report suite does the project use? | Select a report suite from the list, or type the name of another one. |
   | [!UICONTROL **Data view**] | Which CJA data view should it migrate to? | (Optional) Type the name of a data view, or leave it blank and Coworker suggests matching data views. |

1. On the [!UICONTROL **Review**] tab, confirm your answers, then select [!UICONTROL **Submit**].

   To skip the questionnaire at any step, select [!UICONTROL **Skip questionnaire**] and describe what you want in the chat instead.

1. Continue with [Review the validation results and mappings](#review-the-validation-results-and-mappings).

### Start from specific components

<!-- FLAG: Sourced from a prompt that SME Scott Tomko ran in Coworker (October 2026). The example is generalized; the original prompt named a customer. Coworker may ask a few questions along the way. Confirm what happens to the project that Coworker creates in Adobe Analytics, and to its migrated copy in Customer Journey Analytics, if you only wanted the components. -->

To migrate specific components:

1. Ask Coworker to create a project with those components and then migrate it. For example:

   **Prompt**

   > I want to migrate all of my Analytics segments with "Spring sale" in the name to CJA. Create a new Workspace project with all of these segments added, then migrate that project to CJA.

   Coworker creates the project in Adobe Analytics.

1. Continue with the following section, [Review the validation results and mappings](#review-the-validation-results-and-mappings).

## Review the validation results and mappings

<!-- FLAG: Confidence: Medium for the steps that fix a failed validation. They're based on the aa-mcp tool descriptions and on a test conversation where validation passed only after the project's panel was switched to a base report suite. Confirm how Coworker presents a failed validation, and whether it asks for confirmation before it updates a mapping. -->

Coworker validates the project against the data view you selected, then reports whether the project can be migrated. The results list each dimension and metric in the project and the Customer Journey Analytics dimension or metric that it's mapped to. For example:

* **Metric:** Occurrences becomes Events
* **Dimension:** Hour stays Hour

For the components and project elements that are migrated, see [Understand what is included in a migration](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/component-migration/prepare-component-migration#understand-what-is-included-in-a-migration) in the Adobe Analytics documentation.

If validation doesn't pass:

* **Dimensions or metrics that can't be automatically mapped:** Coworker suggests a dimension or metric in your data view to map each one to, updates the mapping, then validates the project again. You can also tell Coworker which dimension or metric to map it to, for example, "Map Page Views to web.webPageDetails.pageViews.value."

* **Unsupported elements:** Remove any unsupported elements from the project in Adobe Analytics. For example, make sure every panel uses a base report suite rather than a virtual report suite. Then ask Coworker to check the project again. For the list of unsupported elements, see [Understand unsupported elements that cause errors](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/component-migration/prepare-component-migration#understand-unsupported-elements-that-cause-errors) in the Adobe Analytics documentation.

To check mappings for a whole report suite before you migrate, see [Review report suite mappings before you migrate](#review-report-suite-mappings-before-you-migrate).

## Migrate the project

1. When validation passes, Coworker asks whether to create the Customer Journey Analytics version of your project on the data view you selected. Select [!UICONTROL **Yes, migrate**], then select [!UICONTROL **Submit**].

   To stop without migrating, select [!UICONTROL **No, stop here**].

   Coworker re-creates the project in Customer Journey Analytics, with you as the project owner. Your original Adobe Analytics project doesn't change.

1. Continue with the following section, [Check the migration status](#check-the-migration-status).

## Check the migration status

Migrations run in the background, so the new project might not be ready right away.

1. Prompt Coworker to check the status of the migration:

   **Prompt**

   > Check status

   <!-- FLAG: The Failed row links to Retry a failed migration in the Adobe Analytics docs, but those steps use the Component migration page in the Adobe Analytics UI, which is admin-only. A non-admin with the Component Migration permission can't follow them. Confirm with Scott whether Coworker can retry a failed migration (for example, "Retry the migration"). If so, replace the link with a prompt. -->

   Coworker reports one of the following statuses:

   | Status | What it means |
   | --- | --- |
   | Queued | The migration is waiting to start. |
   | Started | The migration is in progress. |
   | Completed | The migration finished. Coworker provides a summary of what was migrated, including the project name and data view. |
   | Failed | The migration failed. You can retry the migration. See [Retry a failed migration](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/component-migration/component-migration#retry-a-failed-migration) in the Adobe Analytics documentation. |

1. When the migration is complete, open the new project from your project list in Customer Journey Analytics Workspace.

1. (Optional) Transfer ownership of the project to any user in Customer Journey Analytics. For more information, see [Transfer assets](https://experienceleague.adobe.com/en/docs/analytics-platform/using/tools/asset-transfer/transfer-assets).

After a migration completes, Coworker can suggest another project to migrate next.

## Tips for better results

* Leave the data view blank in the questionnaire if you're not sure which one to use. Coworker suggests data views that match the report suite.
* After you migrate, compare your Adobe Analytics and Customer Journey Analytics data to confirm that your reports match. See [Validate data with Coworker when upgrading from Adobe Analytics to Customer Journey Analytics](/help/chat/use-cases/data-insights/data-validation-aa-cja.md).

## Next steps

* To migrate projects in the Adobe Analytics user interface instead, see [Migrate components and projects from Adobe Analytics to Customer Journey Analytics](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/component-migration/component-migration) in the Adobe Analytics documentation.
* For the other implementation and administration use cases, see [Intelligent implementation and administration overview](/help/chat/use-cases/data-insights/data-governance-and-validation.md).
