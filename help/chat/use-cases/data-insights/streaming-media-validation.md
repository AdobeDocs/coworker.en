---
title: Validate Your Streaming Media Implementation with Coworker
description: Learn how Coworker's Streaming Media Validation skill checks your configuration, sessions, and logs to confirm your implementation is tracking correctly.
hold: true
---

# Validate your Streaming Media implementation with Coworker

Adobe CX Enterprise Coworker includes a Streaming Media Validation skill that checks your Adobe Streaming Media (Video and Audio Analytics) implementation on the Edge Network, feeding Customer Journey Analytics and/or Adobe Analytics. Instead of manually cross-referencing Assurance, dataset configuration, XDM schema field groups, Customer Journey Analytics Data View setup, and raw network logs, you get a single validation report.

If you're implementing or troubleshooting streaming media tracking, you can use this skill to confirm your implementation is configured correctly, collecting data as expected, and capturing what you intended to track, all within a single Coworker Chat conversation.

>[!NOTE]
>
>Consider the following:
>
>* This skill is part of a larger, optional workflow: Custom implementation or upgrade steps (see [Plan your implementation with Coworker](./implementation-guide.md)), Implementation (see [Generate an implementation checklist with Coworker Projects](./intelligent-checklist.md)), and Validation (this skill). You don't need to use all three stages. For example, you can validate your streaming media implementation without ever generating a plan or a checklist.
>* This skill validates and diagnoses issues. It doesn't fix your configuration or data. Use its findings to guide your own remediation.

Use this skill to:

* Run a configuration audit across your Datastream, XDM schema, dataset, and Customer Journey Analytics Data View, with the first broken checkpoint flagged as the likely cause.

  This feature is currently in Limited Availability.

* Validate a specific video session ID, and see exactly which hop, dataset ingestion or Customer Journey Analytics mapping, a discrepancy occurred at.

* Validate a session from an uploaded Charles or HAR log, or a simpler URL list, without needing a live Assurance session.

  This feature is currently in Limited Availability.

* Get an overall health check with a single prompt, no session ID or log required, that rolls up your configuration and a sample of recent sessions.

## Before you begin

<!-- FLAG: General access prerequisite is inferred, not stated explicitly in source docs. Per-mode inputs (session ID, log file) are directly sourced from Functional Requirements. -->

### Information needed

To validate your streaming media implementation, you need:

* Access to Coworker with your organization's Adobe Experience Platform and Customer Journey Analytics data connected.

* For a session-ID validation, the video session ID you want to check.

* For a log-based validation, a Charles or HAR log file, or a simpler URL list in .txt, .md, or .json format.

No specific input is required for a configuration audit or an overall health check. Coworker reads your existing configuration and samples recent sessions automatically.

### Limitations

Before you use this skill, keep the following in mind:

* **Diagnosis only**: This skill doesn't fix your configuration or data. It identifies issues; you make the change.
* **Streaming Media only**: This skill covers streaming media implementations on the Edge Network. Non-media datasets and standard web or app Analytics implementations are covered by other Coworker validation skills.
* **On-demand only**: This skill doesn't provide real-time or continuous monitoring. Run it when you want a check, rather than as ongoing alerting.
* **No built-in crawler**: This skill doesn't crawl your site or app for you. If you want to validate as-crawled coverage, provide crawler or headless-browser output as evidence.
* **Edge Network implementations only**: Legacy Media SDK and Analytics-only implementation paths aren't supported.
* **Broader capabilities aren't included yet**: Live event and heartbeat stream validation, customer playbook or scenario validation, a multi-platform historical dashboard rollup, and downstream Real-Time CDP or Adobe Journey Optimizer activation validation are planned for later releases.

## Start a validation session

1. Sign in to Coworker.

1. Select [!UICONTROL **New chat**].

1. In the text field, describe what you want to validate. For example:

   **Prompt**

   > Validate video session ID #123.

   Your request is routed to the Streaming Media Validation skill, which runs the matching validation mode.

1. (Conditional) If the skill needs more information, such as a session ID or a log file, provide it when asked.

## Choose your validation mode

The Streaming Media Validation skill includes four modes.

### Configuration audit

This feature is currently in Limited Availability.

Validate your entire Adobe Experience Platform flow from Datastream through to the Customer Journey Analytics Data View, including your XDM schema, dataset, and any Data Prep rules or Customer Journey Analytics derived fields. Coworker reports a per-hop pass/fail scorecard and flags the first broken checkpoint as the likely cause.

Example prompts:

* Validate streaming media configuration for dataview, dataset, and datastream.
* Check my streaming media config end to end.
* Is my media analytics datastream set up correctly for Customer Journey Analytics?

### Session-ID validation

Cross-check Adobe Experience Platform dataset rows against the Customer Journey Analytics Data View for a specific video session, and pinpoint whether a gap is a dataset ingestion issue or a Customer Journey Analytics mapping issue.

Example prompts:

* Validate video session ID #123.
* Why isn't session abc-123 showing up in Customer Journey Analytics?
* Compare session xyz between the dataset and the Customer Journey Analytics Data View.

### Log-based validation

This feature is currently in Limited Availability.

Validate a session from a Charles or HAR log you upload, or from a simpler URL list, without needing a live Assurance session. Coworker validates endpoint patterns, response codes, event sequencing, and ping cadence, and states which checks ran at full confidence, reduced confidence, or were skipped.

Example prompts:

* Validate attached logs of streaming media data.
* Check this Charles log for session ID #456.
* Validate this list of URLs against expected media pings.

### Validation dashboard

Get an overall health check with a single prompt. Coworker rolls up the configuration audit and a lightweight, sampled session check into one status, and explicitly states that log-based checks weren't run if no log was provided.

Example prompts:

* Check streaming media data.
* Give me a report on my streaming media implementation.
* How healthy is my streaming media implementation overall?

## Review the results

Each mode returns results in a format suited to your validation.

**Configuration audit results**

A per-hop pass/fail scorecard covering Datastream, XDM schema, dataset, Customer Journey Analytics Data View, and Data Prep or derived field rules. Coworker identifies the first failing hop as the likely root cause.

**Session-ID validation results**

A Customer Journey Analytics-only reporting summary, including the session ID, content metadata, row counts by event type, key metric values, and an integrity note. If there's a gap, Coworker identifies whether it happened at dataset ingestion or at the Customer Journey Analytics mapping step.

>[!NOTE]
>
>Session IDs and authenticated identity values are excluded from any exported or shared summary by default.

**Log-based validation results**

A structural and sequencing validation of your uploaded log, covering endpoint patterns, response codes, event order, and ping cadence. Coworker states which checks ran at full confidence, which ran at reduced confidence, and which were skipped, based on whether you provided a full log capture or a simpler URL list.

**Dashboard results**

A single consolidated status labeled "Configuration + Available Data," combining your configuration audit results with a sampled check of recent sessions. Coworker names which sessions were sampled, and explicitly states that log-based checks weren't run because no log was provided.

## How validation works

Each mode maps to a dedicated engine:

* **Configuration Validation Engine**: Reads your Datastream, XDM schema, dataset, and Customer Journey Analytics Data View configuration, and evaluates it against a fixed set of checkpoints.
* **Session Cross-Check Engine**: Given a session ID, queries your dataset and Customer Journey Analytics Data View, computes the expected row count and type for that session, and compares actual results at each hop.
* **Log Parser and Validator**: Parses your uploaded log or URL list, reconstructs the request sequence and timing, and applies structural, sequencing, and network-layer checks.
* **Dashboard Aggregation Engine**: Runs the Configuration Validation Engine and a sampled run of the Session Cross-Check Engine, and combines them into a single status when you haven't provided a session ID, log, or playbook.
