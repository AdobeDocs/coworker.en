---
title: Plan Your Customer Journey Analytics or Streaming Media Implementation with Coworker
description: Learn how Coworker's implementation guide skills turn a discovery conversation into a personalized, ordered implementation plan with exportable checklists.
hold: true
---

# Plan your implementation with Coworker

Adobe CX Enterprise Coworker includes five implementation guide skills, one for each product surface: Customer Journey Analytics, an Adobe Analytics to Customer Journey Analytics upgrade, Content Analytics (ACA), Marketing Campaign Analytics (MCA), and Streaming Media. Each skill turns a short discovery conversation into a personalized, dependency-aware implementation plan, complete with an interactive checklist and ready-to-use exports, all within a single Coworker Chat conversation.

If you're standing up or migrating to any of these products, you can use these skills to get an ordered, step-by-step plan, without manually researching Adobe's implementation requirements or building a project plan from scratch.

>[!NOTE]
>
>Consider the following:
>
>* These implementation guide skills are part of a larger, optional workflow: Custom implementation or upgrade steps (these guides), Implementation (see [Generate an implementation checklist with Coworker Projects](./intelligent-checklist.md)), and Validation (for example, [Validate your Adobe Analytics to Customer Journey Analytics upgrade](./data-validation-aa-cja.md) or [Validate your Streaming Media implementation](./streaming-media-validation.md)). You don't need to use all three stages. For example, you can validate your data without ever generating a plan or a checklist.
>* These skills don't access your Adobe systems or make any changes. They help you plan your implementation. They don't perform it or verify it against a live tenant.

Use these skills to:

* Get a personalized, ordered plan for standing up Customer Journey Analytics from scratch, including owners, effort estimates, and dependencies for each step.

* Get a migration plan for upgrading from Adobe Analytics to Customer Journey Analytics, including Adobe Analytics feature-parity mapping, historical backfill sequencing, and a validation gate before you decommission Adobe Analytics.

* Get a guided plan for implementing Content Analytics (ACA), including licensing, privacy and PII scoping, and the guided configuration wizard.

* Get an onboarding plan for Marketing Campaign Analytics (MCA) that adapts to your ingestion path, whether you use Adobe source connectors, your own dataset, or a hybrid approach.

* Get an implementation plan for Streaming Media collection on the Edge, including datastream configuration, per-platform SDK/API implementation, and the media event model.

## Before you begin

<!-- FLAG: Best guess, not confirmed by source docs. Requirements doc doesn't state explicit prerequisites for starting a discovery conversation — verify with skills-overview.md or SME before publishing. -->

### Information needed

To start an implementation guide conversation, you need:

* Which of the five implementation paths applies to you: Customer Journey Analytics (net-new), an Adobe Analytics to Customer Journey Analytics upgrade, Content Analytics (ACA), Marketing Campaign Analytics (MCA), or Streaming Media.

* Basic details about your current environment, such as whether you have an existing Adobe Analytics implementation, your licensing status, or your planned data ingestion path. The discovery conversation asks for these details, but having them ready speeds up the process.

### Limitations

Before you use these skills, keep the following limitations in mind:

* **Planning only**: These skills don't access your Adobe systems or make any changes. They don't perform the implementation or verify it against a live tenant.
* **One product surface per skill**: Each skill covers a single implementation path. If your request applies to a different product surface, the skill directs you to the correct one instead of answering directly.
* **Not a project-tracking experience on its own**: These skills generate a plan and exports, but don't track ongoing status, collaboration, or approvals by themselves. To track your plan over time, transform it into a Coworker Project using a predefined playbook. See [Generate an implementation checklist with Coworker Projects](./intelligent-checklist.md).

## Start an implementation planning session

1. Sign in to Coworker.

1. Select [!UICONTROL **New chat**].

1. In the text field, describe the implementation or migration you want to plan. For example:

   **Prompt**

   > Help me plan my implementation of Customer Journey Analytics.

   Your request is routed to the matching implementation guide skill, which starts an interactive discovery conversation.

1. (Conditional) If the skill can't determine which implementation path applies to you, answer the clarifying question it asks, then continue.

## Choose your implementation path

Each implementation guide skill covers one product surface.

### Customer Journey Analytics

Get a personalized, ordered implementation plan for standing up Customer Journey Analytics from scratch, without an existing Adobe Analytics deployment to migrate. Your plan includes owners, effort estimates, and dependencies for each step.

Example prompts:

* Help me plan my implementation of Customer Journey Analytics.
* I'm standing up Customer Journey Analytics from scratch. Build me an implementation plan.

### Adobe Analytics to Customer Journey Analytics upgrade

Get a migration plan that maps Adobe Analytics feature parity to Customer Journey Analytics, sequences historical backfill, and includes a validation and parallel-run gate before you decommission Adobe Analytics.

Example prompts:

* Help me plan my upgrade from Adobe Analytics to Customer Journey Analytics.
* Build me a migration plan from Adobe Analytics to Customer Journey Analytics.

### Content Analytics (ACA)

Get a guided plan for implementing Content Analytics (ACA), including licensing, privacy and PII scoping, and the guided configuration wizard. Because ACA doesn't have DULE, CMK, or HIPAA coverage, your plan includes privacy gating steps.

Example prompts:

* Help me plan my implementation of Content Analytics.
* Build me an ACA implementation plan.

### Marketing Campaign Analytics (MCA)

Get an onboarding plan for Marketing Campaign Analytics (MCA) Essentials that adapts to your ingestion path, whether you use Adobe source connectors, your own dataset, or a hybrid approach, so funnel mapping and data alignment steps match your environment.

Example prompts:

* Help me plan my implementation of Marketing Campaign Analytics.
* Build me an MCA onboarding plan using my own dataset.

### Streaming Media

Get an implementation plan for Streaming Media collection on the Edge, covering datastream configuration, per-platform SDK/API implementation, and the media event model, so you correctly instrument sessions, pings, and completions for Customer Journey Analytics and/or Adobe Analytics reporting.

Example prompts:

* Help me plan my Streaming Media implementation.
* Build me a plan for instrumenting Streaming Media on the Edge.

## Review the results

Coworker returns your implementation plan as an interactive checklist and a summary in the same conversation.

**Interactive checklist**

An HTML checklist that groups your implementation steps into phases and milestones. For each step, the checklist includes:

* An effort estimate
* A primary owner and any supporting owners
* Hard dependencies on other steps
* Whether the step can be skipped
* A link to the relevant Experience League or developer.adobe.com documentation

**Exports**

Download your plan in the format that fits your workflow:

| Export | What it includes |
| --- | --- |
| CSV | A plain list of steps |
| Jira-import CSV | Steps formatted with story points, priority, and labels for import into Jira |
| Workfront CSV | Steps formatted with durations and predecessors for import into Workfront |
| Markdown | A checklist you can paste into documentation or wikis |

**In-chat summary**

Along with the checklist, Coworker provides a three-part summary directly in the conversation:

1. An overview of your plan
1. The full step table
1. Download links for each export

## How the plan is built

Each implementation guide skill follows the same four-stage process:

* **Discovery**: A staged conversation asks 5 to 9 sets of questions, specific to your implementation path, to learn about your environment and goals.
* **Compute**: An LLM determines which conditional steps and dependency overrides apply to your answers. It doesn't write the plan itself.
* **Assemble and render**: A deterministic process resolves dependencies between steps, orders them, calculates the critical path (the longest chain of dependent steps), and generates your checklist and exports.
* **Deliver**: Coworker provides download links and an in-chat summary of your plan.

This combination of guided discovery and deterministic assembly means your plan is generated consistently from your answers, rather than written freehand.
