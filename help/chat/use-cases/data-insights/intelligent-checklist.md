---
title: Generate an Implementation Checklist in Coworker Projects
description: Learn how Coworker Projects generates a pre-populated implementation checklist from your Implementation Guides plan, with steps you can assign and track.
hold: true
---

# Generate an implementation checklist with Coworker Projects

Adobe CX Enterprise Coworker can generate an Implementation Checklist project in Coworker Projects, pre-populated with the ordered steps from your implementation guide plan for Customer Journey Analytics, an Adobe Analytics to Customer Journey Analytics upgrade, Content Analytics (ACA), Marketing Campaign Analytics (MCA), or Streaming Media. Coworker automates or assists with as many steps as technically possible, so you and your team have a single, trackable place to work through your implementation.

If you're leading an implementation, executing technical steps, or just need visibility into progress, you can use this checklist to assign work, track status, and collaborate with your team, without leaving Coworker.

>[!NOTE]
>
>Consider the following:
>
>* This feature is part of a larger, optional workflow: Custom implementation or upgrade steps (see [Plan your implementation with Coworker](./implementation-guide.md)), Implementation (this checklist), and Validation (for example, [Validate your Adobe Analytics to Customer Journey Analytics upgrade](./data-validation-aa-cja.md) or [Validate your Streaming Media implementation](./streaming-media-validation.md)). You don't need to use all three stages, but generating this checklist does require a completed implementation guide plan.
>* Steps that Coworker executes or assists with automatically include a confidence or verification signal. Review these steps before marking them complete — Coworker doesn't present automated results as verified fact.

Use this checklist to:

* Kick off an implementation or migration with an ordered, pre-populated set of steps for your product path, instead of assembling a plan manually.

* Check status mid-implementation, including what's blocked and what's next, without asking the implementation lead directly.

* Plan a multi-platform or multi-region implementation, where steps run in parallel or in phases rather than a single straight line.

* Let Coworker execute steps directly where possible, such as running a validation check between your Adobe Analytics and Customer Journey Analytics configurations.

* Introduce approval gates for steps that need sign-off before your team moves forward.


## Before you begin

<!-- FLAG: Open question — release note confirms a "predefined playbook" transforms the guide plan into a Coworker Project, but it's unconfirmed whether Coworker runs that playbook automatically or the user has to trigger/follow it manually. Written below as if Coworker does it automatically; verify before publishing. Exact UI mechanics also unconfirmed since Coworker Projects platform documentation doesn't exist yet. -->

### Information needed

To generate an Implementation Checklist, you need:

* A completed implementation guide conversation for your product path. See [Plan your implementation with Coworker](./implementation-guide.md). Coworker transforms this plan into a Coworker Project automatically, using a predefined playbook — you don't need to export anything yourself.

* Access to Coworker Projects in your organization.

### Limitations

Before you use this feature, keep the following in mind:

* **Doesn't own the guide content**: This feature consumes plans from the implementation guide skills. It doesn't author or maintain that underlying content.
* **Sync behavior isn't fully defined yet**: The checklist is intended to stay in sync with updates to your implementation guide plan, but the exact sync mechanism is still being defined. Check for guide-plan updates manually if your implementation spans a long timeline.
* **Requires Coworker Projects**: This feature depends on the Coworker Projects platform being available in your organization.

## Generate a checklist

<!-- FLAG: Best guess, not confirmed by source docs. Coworker Projects UI isn't documented in this repo yet — verify exact navigation and UI labels once available. -->

1. Sign in to Coworker.

1. Select [!UICONTROL **Projects**] in the navigation rail.

1. Select [!UICONTROL **New project**], then select the predefined playbook that matches your implementation guide plan.

   Coworker transforms your plan into a project pre-populated with the ordered steps for your path.

## Review the results

Coworker generates your Implementation Checklist as a Coworker Project that you and your team can work from.

**Project view**

Your project groups the ordered implementation steps from your plan. For each step, you can:

* Assign an owner
* Update status, such as in progress or complete
* Mark a step as not applicable or skip it if it doesn't apply to your implementation
* Add comments and collaborate with your team
* Require approval before a step is considered complete, for steps that need sign-off

**Automated and assisted steps**

Where technically feasible, Coworker executes or assists with a step directly, such as surfacing configuration or status data from Adobe Analytics or Customer Journey Analytics. These steps include a confidence or verification signal, as described above.

**Exports**

Export your checklist or its summary-level progress to Jira, Workfront, or Excel, so you can fold it into your existing project management workflow.

**Multiple checklists**

If you're managing multiple concurrent implementations, such as multiple report suites, regions, or brands, you can maintain multiple Implementation Checklist projects instead of being limited to one.
