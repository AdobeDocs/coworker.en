---
title: Detect Experience Platform Anomalies with Coworker
description: Learn how to detect anomalies in Adobe Experience Platform with Coworker Chat. Explore prompts for ingestion, segmentation, and destination activation metrics.
feature: AI Tools
role: User
level: Intermediate
doc-type: Tutorial
jira: PLAT-313965
product_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: CX Enterprise Coworker
---

# Detect Experience Platform anomalies

Use [!DNL Adobe CX Enterprise Coworker] Chat to identify spikes and drops in supported Adobe Experience Platform metrics. Ask about data flows and audiences to find deviations from a baseline.

Start with a broad question, then focus on a flow or audience that needs attention. Review the reported metric and its baseline before deciding what to investigate.

>[!AVAILABILITY]
>
>Anomaly detection is in limited availability. General availability is planned for the first quarter of 2027.

>[!NOTE]
>
>Anomaly detection provides information without changing your data or configuration.

## Available diagnostic skills

Use the `baseline-anomalies` plugin to detect anomalies, compare trends, and review flow health or current job failures. The plugin is configured by default with the Experience Platform and Apps offering in [!DNL Coworker].

Choose the type of question based on the information you need.

| Skill | Purpose |
| --- | --- |
| [!UICONTROL Baseline Anomalies Search Flow Anomalies] | Detect spikes or drops in record volume and failed records across ingestion, segmentation, export, and destination stages. |
| [!UICONTROL Baseline Anomalies Search Audience Anomalies] | Detect spikes or drops in realized audience profile counts, and spikes in exited profile counts. |
| [!UICONTROL Baseline Anomalies Summarize Flow Trend] | Compare recent and typical flow throughput without an anomaly verdict. |
| [!UICONTROL Baseline Anomalies Summarize Audience Trend] | Compare recent and typical qualified and exited profile counts for batch segmentation, without an anomaly verdict or expected range. |
| [!UICONTROL Baseline Anomalies Inspect Flow Health] | Review deduplicated succeeded and failed run counts, plus failed record totals by activity or flow. |
| [!UICONTROL Baseline Anomalies Search Failed Jobs] | Review currently failed jobs and their failure reasons, excluding recovered failures and details for individual records. |

Trend summaries describe changes but do not determine whether those changes are anomalies. Use anomaly questions when you need a spike or drop assessment.

## Before you begin

The plugin is configured by default. To check its status before asking diagnostic questions, follow these steps.

1. Go to **[!UICONTROL Customizations]**.

1. Select **[!UICONTROL Plugins]**.

1. Open **[!UICONTROL baseline-anomalies]** and confirm that its status is **[!UICONTROL Active]**.

Identify the sandbox and area you want to check. For a specific resource, have its flow, segment, or destination name or identifier ready.

For general chat instructions, see [Get started with Chat](/help/chat/ui-guide.md).

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
| Check realized profile spikes | Are any audiences seeing a spike in realized profiles today? |
| Check failed record anomalies | Are failed records abnormally high on flow CustomerImport? |

The broad question checks both data flows and audiences. Confirm the sandbox and time period identified in the response.

<!-- Author review: Confirm exact supported time windows, defaults, time zone handling, and data freshness. -->

## Review anomaly results

Compare the reported value with its baseline for the affected resource and time period. Use the difference to identify what needs further investigation, rather than treating an anomaly as a confirmed cause.

For example, a decrease in ingestion input records identifies a volume change. That change alone does not explain why fewer records arrived.

Results can appear as tables or a written summary. Tables can group anomalies under [!UICONTROL High risk] and [!UICONTROL Medium risk].

![Anomaly results group ingestion and destination volume spikes and drops by high and medium risk, with resource names and values redacted.](assets/anomaly-detection/anomaly-detection-results.png){width="900" zoomable="yes"}

This example groups flow anomalies by risk and suggests investigating run counts or trend history. Resource names and values are redacted.

| Result detail | What to review |
| --- | --- |
| [!UICONTROL When (UTC)] | The event time or time window in Coordinated Universal Time. |
| [!UICONTROL Stage] | The affected processing stage, such as ingestion or destination. |
| [!UICONTROL Flow] | The affected flow, identified by name or identifier. |
| [!UICONTROL What happened] | The change detected, such as a volume spike or drop. |
| [!UICONTROL Actual vs. expected] | The observed value compared with the baseline or expected range. |

Review the explanation alongside the risk grouping. For audience anomalies, High indicates a large departure from normal. Medium indicates a clear but moderate departure. Only High and Medium anomalies are returned.

Audience results exclude Medium anomalies when the baseline history is highly variable. Any returned anomaly with highly variable history therefore has a High risk tier.

Use risk tiers to prioritize investigation, not to establish a root cause.

For example, one response identifies 10 input records against an expected range of one to four as a medium risk spike. The usual level is about one record, so the deviation is large relative to the baseline. The absolute volume remains small.

Check event times before treating a historical anomaly as a current issue. An event outside the last 24 hours does not establish whether the underlying condition recovered.

<!-- Author review: Confirm flow risk tier definitions and whether persistence is reported. -->

### Baselines and expected ranges

Hourly anomaly comparisons use the same hour over the previous 14 days. This accounts for typical patterns by hour, but does not account for broader seasonality.

For audience anomalies, the expected range centers on the median and widens according to variation in the historical counts. If the calculated lower bound is negative, the range uses the lowest historical count instead. The range can therefore extend farther above the median than below it.

Realized profile counts above the expected range are spikes. Counts below the range are drops. A count of zero when profiles are normally present is a High risk drop.

Exited profile counts produce spike verdicts only. Fewer exits are treated as normal, not as drop anomalies.

### No anomalies returned

A response can report that no High or Medium anomalies were returned for the requested audience and period.

![An audience anomaly summary reports no High or Medium anomalies over 168 hours and includes a warning about excluded history.](assets/anomaly-detection/anomaly-detection-no-anomalies.png){width="900" zoomable="yes"}

This example includes a warning about insufficient or mostly zero history. It does not confirm that every hour was evaluated or that this audience was excluded. The audience name and identifier are redacted.

### Insufficient baseline history

Baseline history affects whether an audience can be evaluated for anomalies.

Audience anomaly detection does not evaluate rows with fewer than five days of history or a history containing mostly zeros.

>[!IMPORTANT]
>
>No reported anomalies does not mean that every resource was evaluated. The response might not confirm whether an audience was evaluated or skipped.

<!-- Author review: Confirm flow minimum history requirements and whether audience evaluation status or excluded resources can be retrieved. -->

## Refine your question

Focus your next question on the affected resource. For example, after a broad ingestion check, ask about anomalies for a named flow.

After asking about the last 24 hours, extend the period with this follow-up:

```text
What about in the past two weeks?
```

The response can identify historical anomalies even when none appear in the last 24 hours.

For a closer investigation, ask about flow run counts, flow trends, audience trends, or currently failed jobs. You can also ask about individual jobs as you investigate.

Choose your next question based on the information you need. Trend and health summaries do not provide anomaly verdicts.

| Goal | Example prompt | What to expect |
| --- | --- | --- |
| Review audience trends | How have my audiences changed over the last week? | Recent and typical qualified and exited profile counts for batch segmentation, without an expected range. |
| Review flow trends | How has ingestion volume changed over the last week? | Recent throughput compared with typical throughput, without an anomaly verdict. |
| Review flow health | How many runs succeeded or failed for my ingestion flows in the last 24 hours? | Deduplicated run counts and aggregate failed record totals, without failure reasons. |
| Investigate failed jobs | Which export jobs failed in the last 24 hours, and why? | Jobs whose latest state is failed within the requested scope, with job failure reasons. |
| Investigate a flow failure | What's the error on flow CustomerImport? | Failure reasons for currently failed jobs associated with the flow, without details for individual records. |

Audience trend history is retained for approximately two weeks, or 336 hours. The typical value is the median for that hour over the previous 14 days.

For currently failed jobs, an empty result means that no jobs are currently failing within the requested scope. It does not mean that no failures occurred during the requested period. Jobs that failed and later succeeded are excluded.

Continue investigating with health check skills, or use alert skills to enable an alert for a supported asset. These actions use separate skills, not anomaly detection itself.

For related alert workflows, see [Customer alert skills](/help/chat/use-cases/customer-alerts/customer-alerts.md).

<!-- Author review: Validate a complete public example response and the supported alert assets and setup before adding an alert procedure. -->

## Metric reference

The limited release includes the following seven metrics across ingestion, segmentation, and destination activation. Use this reference to identify the counts associated with each area.

| Area | Metric identifier | Count measured |
| --- | --- | --- |
| Ingestion | `input_record_count` | Count of input records for an ingestion flow. |
| Ingestion | `failed_record_count` | Count of failed records for an ingestion flow. |
| Segmentation | `__segment_{segment_id}__realized_profiles` | Count of profiles that qualify for a segment. |
| Segmentation | `__segment_{segment_id}__exited_profiles` | Count of profiles that exit a segment. |
| Destination activation | `{destination}_input_record_count` | Count of input records for a destination. |
| Destination activation | `{destination}_skipped_record_count` | Count of skipped records for a destination. |
| Destination activation | `{destination}_output_record_count` | Count of output records for a destination. |

<!-- Author review: Confirm metric aggregation intervals and identifier visibility. -->

## Scope and limitations

Use anomaly detection to identify deviations, not to confirm a root cause or repair a resource.

You can ask about flows, segments, and destinations by name or identifier. Flow anomaly detection covers ingestion, segmentation, export, and destination stages.

Use the failed job skill for currently failed jobs and their failure reasons. Recovered failures are excluded. Job diagnostics do not include details for individual records or anomaly verdicts.

Flow health provides aggregate counts, not failure reasons. Trend summaries describe recent and typical values, not anomaly verdicts. Audience trend summaries cover batch segmentation only.

Anomaly detection does not change your data or configuration. Use separate skills for supported alert actions and deeper health investigations.

<!-- Author review: Confirm job identifier support and any recommendation capabilities before adding examples. -->
