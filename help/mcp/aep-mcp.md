---
title: Experience Platform Tools in CX Coworker Gateway
description: Learn which Adobe Experience Platform tools are available through CX Coworker Gateway.
hide: true
---

# Adobe Experience Platform tools in Adobe CX Coworker Gateway {#aep-mcp}

You can use the Adobe Experience Platform product tools to inspect schemas, datasets, data governance configuration, Query Service resources, and audit events from an MCP-compatible client. These tools are available through the [Adobe CX Coworker Gateway](overview.md) when your organization is enabled and your user account has the required Experience Platform permissions.

>[!AVAILABILITY]
>
>The Experience Platform product tool is in Beta. Access is by invitation only and requires Adobe organization enablement. See [Access CX Coworker Gateway tools](access.md).

## Summary

| Tool | Description | Resource | Capabilities | Status |
| --- | --- | --- | --- | --- |
| `search_allowed_ip_ranges` | Retrieve Query Service IP access restrictions | Data Distiller Auth · IP ranges | list | Active |
| `search_audit` | List user activity audit events across Experience Platform | Audit Query · audit events | list, filter by asset type, action, status, time range | Active |
| `search_datasets` | Query dataset and batch ingestion metadata | Catalog API · dataSets, batches | list, get, filter, list last, list files | Active |
| `search_class_relations` | Search Experience Platform business class relationships | Class Relations · static YAML index | search by token, multi-term, partial match | Active |
| `search_data_access` | List files from failed ingestion batches | Data Access API · failed batches | list failed files | Active |
| `search_data_lake` | Inspect dataset metadata and batch health | Data Lake API · datasets, batches | get, get size, list failed batches | Active |
| `search_dule` | Query data governance labels, policies, actions | Data Governance · labels, policies, marketing_actions | list, get, list enabled, evaluate | Active |
| `search_query_service` | Query SQL queries, templates, schedules, alerts | Query Service · queries, templates, schedules, alerts | list, get, filter, get connection params | Active |
| `search_sandbox_health_assessment` | Retrieve the latest Run and Operate health check assessment results for the current sandbox | Run and Operate · health check assessments | list, get by check name | Active |
| `search_schema_registry` | Query XDM schemas, field groups, classes, types | Schema Registry · schemas, fieldgroups, classes, data_types, descriptors | list, get, filter by container | Active |
| `execute_observability_metrics_query` | Query [!DNL Observability Insights] metrics for the current sandbox or across all sandboxes | Observability Insights · metrics | time-series and aggregate queries, multi-metric requests, tag filters, groupBy/exclude, per-metric downsample | Active |
| `inspect_observability_breaches` | Detect [!DNL Observability Insights] breach intervals where a metric exceeded its configured baseline | Observability Insights · breaches | list breach intervals per series, org and sandbox scope | Active |

## Tool Reference

### search_allowed_ip_ranges

**Resource:** Data Distiller Auth · IP ranges
**Status:** Active

Retrieve all configured IP access restrictions for Query Service in the current sandbox. Returns the organization ID and the list of allowed IP ranges. Only available to customers with the Data Distiller add-on.

**Capabilities:** list allowed IP ranges for Query Service

No parameters.

### search_audit

**Resource:** Audit Query · audit events
**Status:** Active

List timestamped records of user activities across Experience Platform services. Returns action type, user email, asset information, and event status. Use `asset_type` and `action` to narrow results. Defaults to the last 7 days when no time range is specified. Limited to the last 1000 records and events from the past 90 days.

**Capabilities:** list audit events, filter by asset type, action, status, time range, paginate

**Parameters:**

| Parameter | Required | Description |
| --- | --- | --- |
| `action` | No | Filter by action type. Common values (comma-separate for OR): `Create`, `Delete`, `Update`, `Enable`, `Disable` |
| `asset_type` | No | Filter by asset type. Must be one of: `Dataset`, `Schema`, `Segment`, `Destination`, `Source Data Flow`, `Merge Policy`, `Identity Namespace`, `Identity Graph`, `Sandbox`, `Role`, `Query`, `Scheduled Query`, `Datastream`, `Computed Attribute`, `Field Group`, `Class`, `Data Types`, `Account`, `Product Profile`, `Query Template`, `Work Order`, `Audit Logs`, `Access Control Policy` |
| `status` | No | Filter by event status. Values: `Success`, `Failure`, `Allow`, `Deny`. Comma-separate for OR |
| `start_time` | No | Earliest timestamp. ISO 8601 UTC with ms, e.g. `2024-01-15T00:00:00.000Z` |
| `end_time` | No | Latest timestamp. ISO 8601 UTC with ms |
| `property_filter` | No | Raw filter expression, e.g. `action==create`. Prefer the dedicated parameters above |
| `orderby` | No | Sort order: `timestamp` (asc) or `-timestamp` (desc) |
| `limit` | No | Maximum number of results (3–1000, default 50) |
| `start` | No | Pagination offset. Increment by limit value for each page |
| `query_id` | No | Query ID from a previous response to repeat the same query |

### search_datasets

**Resource:** Catalog API · dataSets, batches
**Status:** Active

Unified dispatch tool for the Experience Platform Catalog Service. Query dataset metadata (schema refs, tags, creation info) or batch ingestion records (status, metrics, file listings). Use `dataset/list` to discover datasets, `batch/list` to check ingestion health, and `batch/list_files` or `batch/get_meta_files` to inspect specific batch contents. All operations are read-only.

**Capabilities:** list datasets, get dataset, list batches, get batch, list last batch per dataset, list batch files, get batch meta files (row errors, input files)

**Parameters:**

| Parameter | Required | Description |
| --- | --- | --- |
| `entity_type` | Yes | `dataset` or `batch` |
| `operation` | Yes | `list`, `get`, `list_last`, `list_files`, `get_meta_files`. Valid combos: dataset → list, get; batch → all five |
| `resource_id` | No | Dataset or batch ID. Required for `dataset/get`, `batch/get`, `batch/list_files`, `batch/get_meta_files` |
| `query_params.limit` | No | Max results per page (max 100). Applies to all list operations |
| `query_params.start` | No | Pagination offset. Applies to all list operations |
| `query_params.order_by` | No | Sort direction, e.g. `asc:created,updated`. Applies to all list operations |
| `query_params.properties` | No | Comma-separated property allowlist. Applies to dataset/list, dataset/get, batch/list, batch/list_last |
| `query_params.name` | No | Filter datasets by name (dataset/list only) |
| `query_params.tags` | No | Filter datasets by tags, e.g. `unifiedProfile:enabled:true` (dataset/list only) |
| `query_params.property_filter` | No | Regex filter on response objects (dataset/list and batch/list) |
| `query_params.status` | No | Filter batches by status: `success`, `failed`, `loading`, `active` (batch/list only) |
| `query_params.dataset_id` | No | Scope batches to a specific dataset (batch/list and batch/list_last) |
| `query_params.created_after` | No | Filter batches created after Unix timestamp in ms (batch/list only) |
| `query_params.created_before` | No | Filter batches created before Unix timestamp in ms (batch/list only) |
| `query_params.last_batch_status` | No | Filter by last batch status (batch/list_last only) |
| `query_params.aggregate` | No | Return aggregated metrics at root level (batch/get only) |
| `query_params.path` | No | Meta file to download: `row_errors`, `input_files`, `row_errors_sample.json` (batch/get_meta_files only) |

### search_class_relations

**Resource:** Class Relations · static YAML index
**Status:** Active

Search for Experience Platofrm business class relationships by name using the static `class_relations_v1.yaml` index. No Experience Platofrm API calls are made. Accepts a single term or comma-separated terms; each term is matched against class names using partial token matching. Returns matching classes with forward relations (what each class points to) and reverse relations (which classes point back to it). Use this to understand entity relationships before building queries, dataflows, or schema compositions.

**Capabilities:** search by token, multi-term comma-separated search, partial token match, bidirectional synonym expansion

**Parameters:**

| Parameter | Required | Description |
| --- | --- | --- |
| `query` | Yes | Business class name or object type to search for. Supports partial token matches (`dat` matches `dataset`, `data_type`, etc.). Pass multiple comma-separated terms to search for several classes at once (e.g. `dataset, schema`) |
| `n` | No | Maximum number of matched results to return (default 5, min 1) |

### search_data_access

**Resource:** Data Access API · failed batches
**Status:** Active

Access files from failed Experience Platofrm data ingestion batches. Use `failed_batch/list_failed` to list the files belonging to a failed batch for failure diagnosis. Requires a batch ID for all operations. Note: `file/get` and `dataset/preview` are disabled as they expose actual record data. All operations are read-only.

**Capabilities:** list files from a failed ingestion batch

**Parameters:**

| Parameter | Required | Description |
| --- | --- | --- |
| `entity_type` | Yes | `failed_batch` — list files from a failed ingestion batch |
| `operation` | Yes | `list_failed` — the only supported operation |
| `resource_id` | Yes | Batch ID of the failed batch |
| `query_params.start` | No | Paging start index, e.g. `1` |
| `query_params.limit` | No | Number of results per page, e.g. `10` |
| `query_params.path` | No | Full file name filter, e.g. `profiles.csv` |


### search_data_lake

**Resource:** Data Lake API · datasets, batches
**Status:** Active

Inspect dataset and batch metadata from the Data Lake layer. Use `get` for full metadata, `get_size` for storage and ingestion size metrics, and `list_failed` to monitor ingestion failures within a time window. Defaults to the last 7 days when no time range is provided for `list_failed`. All operations are read-only and require a resource ID.

**Capabilities:** get dataset/batch metadata, get storage size metrics, list failed batches within a time window

**Parameters:**

| Parameter | Required | Description |
| --- | --- | --- |
| `entity_type` | Yes | `dataset` or `batch` |
| `operation` | Yes | `get`, `get_size`, `list_failed`. `list_failed` only supports `batch` entity type |
| `resource_id` | Yes | Dataset ID or batch ID. For `list_failed`: the dataset ID to scope failures to |
| `query_params.created_after` | No | Start of time window. Unix timestamp in ms |
| `query_params.created_before` | No | End of time window. Unix timestamp in ms |
| `query_params.limit` | No | Max results per page (max 100) |
| `query_params.order_by` | No | Sort direction, e.g. `desc:created` |

### search_dule

**Resource:** Data Governance · labels, policies, marketing_actions
**Status:** Active

Query the Policy Service API for data usage labels, policies, and marketing actions. Use `marketing_action/evaluate` to test whether a marketing action on data with specific labels would violate any governance policies. All operations are read-only.

**Capabilities:** list/get data usage labels, list/get policies, list enabled policies, list/get marketing actions, evaluate marketing action against labels

**Parameters:**

| Parameter | Required | Description |
| --- | --- | --- |
| `entity_type` | Yes | `label`, `policy`, or `marketing_action` |
| `operation` | Yes | `list`, `get`, `list_enabled` (policy only), `evaluate` (marketing_action only). `list_enabled` does not require scope |
| `scope` | No | `core` (Adobe-defined) or `custom` (org-defined). Required for `list`, `get`, `evaluate`; not used for `list_enabled` |
| `resource_id` | No | Label name, policy ID, or marketing action name. Required for `get` and `evaluate` |
| `query_params.dule_labels` | No | Comma-separated labels (e.g. `C1,C3`). Required for `marketing_action/evaluate`; optional filter for `policy/list` |
| `query_params.limit` | No | Max results |
| `query_params.start` | No | Pagination cursor from a previous response's `_page.next` value |
| `query_params.orderby` | No | Comma-separated sort fields |
| `query_params.property_filter` | No | Filter expression, e.g. `name==C1` |
| `query_params.marketing_action` | No | Restrict policy list to policies referencing this marketing action (policy/list only) |
| `query_params.include_draft` | No | Include DRAFT policies in `marketing_action/evaluate` (default: ENABLED policies only) |

### search_query_service

**Resource:** Query Service · queries, templates, schedules, schedule runs, connections, alert subscriptions
**Status:** Active

Unified tool for Query Service resources. List and retrieve ad-hoc queries, saved SQL templates, scheduled queries and their runs, interactive connection parameters (for psql/JDBC clients), and alert subscriptions. For query lists, default to `isService==false,isParentLevel==true` to filter out internal traffic. All operations are read-only.

**Capabilities:** list/get queries, list/get templates, list/get schedules, list/get schedule runs, get connection params, list alert subscriptions

**Parameters:**

| Parameter | Required | Description |
| --- | --- | --- |
| `entity_type` | Yes | `query`, `query_template`, `schedule`, `schedule_run`, `connection`, `alert_subscription` |
| `operation` | Yes | `list`, `get`, `get_connection_params`, `list_by_u...` |

### execute_observability_metrics_query

**Resource:** Observability Insights · metrics
**Status:** Active

Query [!DNL Observability Insights] metrics for the current sandbox, or across all sandboxes in your organization. Supports multiple metrics in a single request, tag-based filters, and per-metric downsampling. For `scope=org`, include at least one `groupBy` filter on every metric. All operations are read-only.

**Capabilities:** query metric datapoints, time-series or aggregate, multi-metric requests, tag filters, groupBy/exclude, per-metric downsample

**Parameters:**

| Parameter | Required | Description |
| --- | --- | --- |
| `metrics` | Yes | Array of metric specs. Each includes `name` (fully qualified metric name), `aggregator` (`sum`, `avg`, `min`, `max`, `count`, `last`, `p50`, `p95`, `p99`, histogram variants, or `absent`), optional `filters`, and optional `downsample` |
| `start` | Yes | Window start, ISO 8601, e.g. `2026-01-15T00:00:00.000Z`. Must be earlier than `end`. Max window: 31 days |
| `end` | Yes | Window end, ISO 8601. Must be later than `start` |
| `granularity` | No | Time bucket size: `MINUTE`, `FIVE_MINUTE`, `TEN_MINUTE`, `FIFTEEN_MINUTE`, `THIRTY_MINUTE`, `HOUR`, `FOUR_HOUR`, `TWELVE_HOUR`, `DAY`, `TWO_DAY`, `WEEK`, `MONTH`, or `ALL` (collapses the window into a single aggregate). Omit to let the server choose |
| `scope` | No | `sandbox` (default) queries the current sandbox. `org` queries all sandboxes in your organization and recommends a `groupBy` filter on every metric |

Each filter in `metrics[].filters` includes a `name` (tag name), `value` (exact, wildcard, or regex match), and optional `groupBy` and `exclude` booleans.

### inspect_observability_breaches

**Resource:** Observability Insights · breaches
**Status:** Active

Detect [!DNL Observability Insights] breach intervals, the time windows where a metric exceeded its configured baseline, for the current sandbox or across all sandboxes in your organization. Returns pre-matched intervals per series. Open-ended breaches still in progress at the end of the window are returned with `end: null`. All operations are read-only.

**Capabilities:** list breach intervals per series, org and sandbox scope

**Parameters:**

| Parameter | Required | Description |
| --- | --- | --- |
| `metrics` | Yes | Array of breach specs. Each includes `name` (fully qualified metric name) and optional `filters` |
| `start` | Yes | Window start, ISO 8601. Must be earlier than `end`. Max window: 31 days |
| `end` | Yes | Window end, ISO 8601 |
| `granularity` | No | Time bucket size, same values as `execute_observability_metrics_query` except `ALL`. Each bucket is evaluated independently against the baseline |
| `scope` | No | `sandbox` (default) or `org`. On `org` without a sandbox filter, include at least one filter with `groupBy: true` per metric so results are split by that dimension instead of collapsed across the org |

`inspect_observability_breaches` does not accept `aggregator` or `downsample` on `metrics[]`. The tool sets these internally to evaluate the breach condition.

>[!NOTE]
>
>Both Observability Insights tools are also limited to an estimated 10,000 datapoints per request. Narrow the time range, add filters, or use a coarser `granularity` if a request is rejected for exceeding this limit.

### search_sandbox_health_assessment

**Resource:** Run and Operate · health check assessments
**Status:** Active

Retrieve the latest Run and Operate health check assessment results for the current sandbox. Returns results across every supported category, including schemas and identities, segmentation, ingestion, and profile. To identify the root cause without a separate lookup, each result includes the affected assets behind a failing check. Only checks with a published, human-readable name are returned. All operations are read-only.

>[!NOTE]
>
>This tool only retrieves assessment results. To remediate a flagged issue, use the health check detail panel in the [!DNL Experience Platform] UI. See [Health Checks](https://experienceleague.adobe.com/en/docs/experience-platform/run-and-operate/health-checks). Automatic remediation guidance for supported health checks is available as a skill in [CX Coworker Chat](../chat/overview.md).

**Capabilities:** list all health check results for the current sandbox, get results for one named check

No parameters.
