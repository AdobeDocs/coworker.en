---
title: Detect Experience Platform Anomalies with Coworker
description: Learn how to detect anomalies in Adobe Experience Platform with Coworker Chat. Explore prompts for ingestion, segmentation, and destination activation metrics.
feature: AI Tools
role: User
level: Intermediate
doc-type: Tutorial
jira: PLAT-313965
hide: true
product_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: CX Enterprise Coworker
feature_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: CX Enterprise Coworker
---

# Detect Experience Platform anomalies

Use [!DNL Adobe CX Enterprise Coworker] Chat to identify spikes and drops in supported Adobe Experience Platform metrics. Ask about data flows and audiences to find deviations from a baseline.

Start with a broad question, then focus on a flow or audience that needs attention. Review the reported metric and its baseline before deciding what to investigate.

>[!AVAILABILITY]
>
>Anomaly detection is in limited availability.

>[!NOTE]
>
>Anomaly detection provides information without changing your data or configuration.

## Available diagnostic skills

Use the `baseline-anomalies` plugin to detect anomalies, compare trends, and review flow health or current job failures. The plugin belongs to the `baseline-anomalies-extensions` marketplace.

Choose the type of question based on the information you need.

| Skill | Purpose |
| --- | --- |
| [!UICONTROL Baseline Anomalies Search Flow Anomalies] | Detect spikes or drops in record volume and failed records across ingestion, segmentation, export, and destination stages. |
| [!UICONTROL Baseline Anomalies Search Audience Anomalies] | Detect spikes or drops in realized and exited audience profile counts. |
| [!UICONTROL Baseline Anomalies Summarize Flow Trend] | Compare recent and typical flow throughput without an anomaly verdict. |
| [!UICONTROL Baseline Anomalies Summarize Audience Trend] | Compare recent and typical audience profile counts without an anomaly verdict. |
| [!UICONTROL Baseline Anomalies Inspect Flow Health] | Review deduplicated succeeded and failed run counts, plus failed record totals by activity or flow. |
| [!UICONTROL Baseline Anomalies Search Failed Jobs] | Review currently failed jobs and their failure reasons, excluding recovered failures and details for individual records. |

Trend summaries describe changes but do not determine whether those changes are anomalies. Use anomaly questions when you need a spike or drop assessment.

<!-- Author review: Skill descriptions and plugin names are visible in the supplied plugin screenshot. Confirm that this plugin version and its export and job failure capabilities match the intended release. -->

## Before you begin

Confirm that the `baseline-anomalies` plugin is active before asking diagnostic questions.

1. Go to **[!UICONTROL Customizations]**.

1. Select **[!UICONTROL Plugins]**.

1. Open **[!UICONTROL baseline-anomalies]** and confirm that its status is **[!UICONTROL Active]**.

Identify the sandbox and area you want to check. For a specific resource, have its flow, segment, or destination name or identifier ready.

For general chat instructions, see [Get started with Chat](/help/chat/ui-guide.md).

<!-- Author review: Confirm availability wording, publication date, required permissions, and plugin installation steps before publication. The screenshot shows an installed, active plugin, not its installation workflow. -->

## Ask about anomalies

Describe the area or resource you want to check and the time period you want to examine.

Use the following example prompts as a starting point. Replace example names with names from your organization.

| Goal | Example prompt |
| --- | --- |
| Check across supported areas | Are there any anomalies in the last 24 hours? |
| Check ingestion | Are there any anomalies with my ingestion in the last 24 hours? |
| Check a specific flow | Are there any anomalies with ingestion flow CustomerImport in the last 24 hours? |
| Check segmentation | Are there any anomalies with my segmentation in the last 24 hours? |
| Check a specific segment | Are there any anomalies with segment LoyaltyMembers in the last 24 hours? |
| Check destination activation | Are there any anomalies with my destination activation in the last 24 hours? |

The broad question checks both data flows and audiences. Confirm the sandbox and time period identified in the response.

<!-- Author review: The broad 24-hour prompt is shown in the supplied conversation screenshot. Validate the remaining entity-specific examples. Confirm supported time windows, defaults, time zone handling, and data freshness. -->

## Review anomaly results

Compare the reported value with its baseline for the affected resource and time period. Use the difference to identify what needs further investigation, rather than treating an anomaly as a confirmed cause.

For example, a decrease in ingestion input records identifies a volume change. That change alone does not explain why fewer records arrived.

Results can appear as tables or a written summary. Tables can group anomalies under [!UICONTROL High risk] and [!UICONTROL Medium risk].

| Result detail | What to review |
| --- | --- |
| [!UICONTROL When (UTC)] | The event time or time window in Coordinated Universal Time. |
| [!UICONTROL Stage] | The affected processing stage, such as ingestion or destination. |
| [!UICONTROL Flow] | The affected flow, identified by name or identifier. |
| [!UICONTROL What happened] | The change detected, such as a volume spike or drop. |
| [!UICONTROL Actual vs. expected] | The observed value compared with the baseline or expected range. |

Review the explanation alongside the risk grouping. Baseline variability, the duration of a deviation, and absolute volume provide context for your investigation.

For example, one response identifies 10 input records against an expected range of one to four as a medium risk spike. The usual level is about one record, so the deviation is large relative to the baseline. The absolute volume remains small.

Check event times before treating a historical anomaly as a current issue. An event outside the last 24 hours does not establish whether the underlying condition recovered.

<!-- Author review: Result fields, risk groups, and the numerical example are visible in the supplied response screenshots. Confirm risk scoring and persistence definitions. Obtain approval before embedding screenshots and replace resource identifiers with synthetic examples. -->

### No anomalies reported

A response can report no material anomalies for the requested period while excluding resources with insufficient baseline history.

>[!IMPORTANT]
>
>An empty result covers only flows and audiences with enough history to build a baseline. Newer resources can be excluded. No reported anomalies does not mean that every resource was evaluated.

<!-- Author review: Confirm the minimum history requirement and whether excluded resources can be listed. -->

## Refine your question

Focus your next question on the affected resource. For example, after a broad ingestion check, ask about anomalies for a named flow.

After asking about the last 24 hours, extend the period with this follow-up:

```text
What about in the past two weeks?
```

The response can identify historical anomalies even when none appear in the last 24 hours.

For a closer investigation, ask about flow run counts, flow trends, audience trends, or currently failed jobs. These questions use different diagnostic skills from anomaly detection.

The example responses suggest questions about run counts and trends, but do not show the completed follow-up results.

<!-- Author review: The two-week follow-up is shown in the supplied conversation screenshot, not a maximum supported window. Validate completed run count, trend, and failed job queries. Confirm history retention, allowed query windows, baseline calculation, and seasonality. -->

## Metric reference

Use this provisional reference to identify the metrics proposed for ingestion, segmentation, and destination activation. Confirm release coverage, definitions, and units before using these descriptions to interpret results.

| Area | Metric identifier | Proposed meaning |
| --- | --- | --- |
| Ingestion | `input_record_count` | Count of input records for an ingestion flow. |
| Ingestion | `failed_record_count` | Count of failed records for an ingestion flow. |
| Segmentation | `__segment_{segment_id}__realized_profiles` | Count of profiles that qualify for a segment. |
| Segmentation | `__segment_{segment_id}__exited_profiles` | Count of profiles that exit a segment. |
| Destination activation | `{destination}_input_record_count` | Count of input records for a destination. |
| Destination activation | `{destination}_skipped_record_count` | Count of skipped records for a destination. |
| Destination activation | `{destination}_output_record_count` | Count of output records for a destination. |

<!-- Author review: These seven identifiers come from the test plan, not a confirmed release contract. Validate each definition, record versus profile units, aggregation interval, and identifier visibility. Confirm whether realized profiles represents total membership or new qualifications. Replace technical identifiers with confirmed display labels if appropriate. -->

## Scope and limitations

Use anomaly detection to identify deviations, not to confirm a root cause or repair a resource.

You can ask about flows, segments, and destinations by name or identifier. Flow anomaly detection covers ingestion, segmentation, export, and destination stages.

Use the failed job skill for currently failed jobs and their failure reasons. Recovered failures are excluded. Job diagnostics do not include details for individual records or anomaly verdicts.

Do not assume that anomaly detection can create alerts, change configuration, or persistently dismiss anomalies.

<!-- Author review: Confirm whether individual jobs can be queried by identifier. Validate recommendations, root cause analysis, alert creation, and persistent dismissal separately before adding procedures or promises. The plugin screenshot includes export and job failure capabilities that the older test plan excludes. Confirm release applicability without equating destination output counts with detailed export diagnostics. -->
