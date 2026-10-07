---
title: Validate Customer Journey Analytics Data with the Data Validation Skill in Coworker
description: Learn how to validate Customer Journey Analytics data using the Data Validation skill in Coworker, and resolve issues before building dashboards.
feature: AI Tools
role: User
level: Beginner, Intermediate
doc-type: Feature Video
duration: 330
last-substantial-update: 2026-09-16
jira: KT-22622
---
# Validate Customer Journey Analytics data with the data validation skill in [!DNL Coworker]

Data quality is the foundation of accurate reporting in Adobe Customer Journey Analytics (CJA). Before building metrics, dashboards, segments, or customer journeys, it is critical to understand whether the underlying Adobe Experience Platform (AEP) data can be trusted.

In this video, you will learn how to use the **Data Validation skill in Adobe CX Enterprise Coworker** to quickly assess the quality of datasets powering your Customer Journey Analytics implementation, without writing queries or manually inspecting data.

>[!VIDEO](https://video.tv.adobe.com/v/3503519/?learn=on&enablevpops)

## Discover the datasets behind your CJA reporting

See how Coworker can identify:

- Which datasets are connected to Customer Journey Analytics
- The connections and data views associated with a specific sandbox
- The datasets actively powering reporting
- Key dataset characteristics, such as streaming status and identity namespaces

By understanding exactly which datasets feed your reports, you can focus validation efforts where they matter most.

## Explore dataset schemas and available fields

Learn how to inspect dataset schemas directly from Adobe Experience Platform.

Coworker retrieves schema details and surfaces:

- Commerce and transaction fields
- Product information
- Web interaction data
- Identity fields
- Campaign and marketing attributes
- Device and geographic dimensions

This provides an inventory of fields available for analysis and highlights the difference between fields that exist in a schema and fields that contain usable data.

## Validate identity quality

Identity data is essential for Customer Journey Analytics because it supports person-level reporting and cross-channel journey analysis.

In this video, you will see how Coworker:

- Validates identity fields
- Checks for null values and data completeness
- Evaluates identifier quality
- Surfaces missing or unavailable identity attributes

The example validation shows that ECID and email identities are fully populated and valid in the sample, while the Analytics ID could not be retrieved. This provides a useful signal when deciding which identifiers can support profile stitching and reporting.

## Analyze individual field quality

A field may exist in a dataset but still be unsuitable for reporting.

Watch how Coworker validates a campaign tracking field and reports:

- Population rates
- Null percentages
- Data consistency
- Invalid value detection

In the example, the tracking code values that are present are clean and consistent, but approximately 85% of rows are null. This reveals a major reporting blind spot before a CJA dimension or campaign metric is built on the field.

## Perform AI-powered dataset validation

Rather than validating individual fields one at a time, Coworker can evaluate an entire dataset.

You will learn how the Data Validation skill:

- Selects important fields for validation
- Assesses completeness and quality
- Compares data health across fields
- Highlights strengths and potential reporting risks

The validation results provide a viability map for CJA. Clean fields such as web page name and email code may be ready for reporting, while sparse fields such as purchase value, campaign name, and tracking code require investigation.

## Identify revenue and attribution risks

The video also demonstrates how data validation can uncover issues that affect reporting accuracy, including:

- Sparse campaign data
- Missing attribution information
- Incomplete transaction values
- Revenue measurement gaps

In the dataset shown, purchase counts are available, but order amounts are not reliably populated. This is an issue to investigate before trusting revenue reporting.

## Why data validation matters for Customer Journey Analytics

Customer Journey Analytics is only as reliable as the data behind it.

Validating datasets before building reports helps teams:

- Increase confidence in analytics results
- Improve data governance practices
- Reduce reporting errors
- Identify implementation issues earlier
- Troubleshoot unexpected metrics more efficiently

With Coworker, these checks can be initiated using natural language prompts, making data validation more accessible to technical and non-technical users.
 