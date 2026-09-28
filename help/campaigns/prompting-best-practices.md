---
description: Learn Coworker Campaigns prompting best practices - the CO-STAR framework, do's and don'ts, unsupported content, and a quality checklist for prompts.
title: Prompting Best Practices
product_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: CX Enterprise Coworker
feature_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: CX Enterprise Coworker
---
# Prompting best practices {#best-practices}

Getting the most out of Coworker Campaigns starts with how you prompt. Learn the practices that produce the best results: the CO-STAR framework for structuring your prompts, what to include and what to avoid, and scenario-based examples that give the AI the context it needs to generate relevant, on-target content.

>[!NOTE]
>
>Currently, you can only connect to Coworker Campaigns-supported integrations. If you have any existing Adobe Enterprise applications, where you store audiences or build journeys, we encourage you to use [CX Enterprise Coworker](/help/chat/use-cases/overview.md) instead.

## Use the CO-STAR framework

For best results, organize your prompts using the CO-STAR framework. This structured approach ensures the AI understands exactly what you need.

| Component | What it means | Why it matters |
|-|-|-|
| **C - Context** | Background about your campaign, product, or situation | Helps the AI understand the bigger picture |
| **O - Objective** | Your specific marketing goal | Drives what the content should achieve |
| **S - Style** | How you want to communicate | Sets the approach |
| **T - Tone** | Emotional style and voice | Shapes how your message feels |
| **A - Audience** | Audience you are targeting | Ensures the message resonates with the right people |
| **R - Requirements** | Specific constraints or must-haves | Defines boundaries and critical elements |

## AI prompt essentials

### Do's and don'ts

<table style="table-layout: fixed; width: 100%; border: 0;">
<thead style="border: 0; background-color: #FFFFFF;">
<tr>
<th>Do</th>
<th>Don't</th>
</tr>
</thead>
<tbody>
<tr style="border: 0;">
<td>
<p>Use the CO-STAR framework for structure</p>
<p>Focus marketing briefs with specific extraction guidance</p>
<p>Draft your prompts to produce the desired intent</p>
</td>
<td>
<p>Ask for structural changes, styling, or image editing in prompts</p>
<p>Use vague instructions like "promote our product"</p>
<p>Expect layout modifications through prompts</p>
</td>
</tr>
</tbody>
</table>

### Content supported in prompts

Use the **email editor** or **Adobe Express** for visual/image modifications. The following request types are supported.

- **Specify the frequency and the cadence of your campaign**: "Create an email campaign that is sent weekly..."

- **Target a specific audience from a larger list**: "Create a campaign only for attendees with dogs for the _Bark in the Park_ event from 'all-attendees.csv'"

- **Upload an HTML file**: "Use my attached HTML file as a basis to create an email campaign."

- **Make changes mid-conversation**: "Change the number of days before this campaign goes out from two to three."

### Content not supported in prompts

These requests are **not** supported and should be handled through other tools:

<table style="table-layout: fixed; border: 0;">
<thead style="border: 0; background-color: #FFFFFF">
<tr>
<th>✗ Email structure modifications</th>
<th>✗ Visual styling changes</th>
<th>✗ In-editor operations</th>
</tr>
</thead>
<tbody>
<tr style="border: 0;">
<td>
<ul>
<li>Selecting specific sections to change</li>
<li>Deleting or cloning elements</li>
<li>Conditional selections</li>
<li>Adding or removing layout sections</li>
</ul>
</td>
<td>
<ul>
<li>Custom fonts</li>
<li>Color modifications</li>
<li>Layout styling (borders, padding, margins)</li>
<li>Visual effects (shadows)</li>
</ul>
</td>
<td>
<ul>
<li>Background changes</li>
<li>Adding text overlays or logos</li>
<li>Image cropping or resizing</li>
<li>Color adjustments</li>
</ul>
</td>
</tr>
</tbody>
</table>

### Quality checklist

Before generating content, ensure the following:

✓ **Clear objective**: Clearly states the action, product/service, value, and context.

✓ **Defined target audience**: Specifies the demographic, role, or segment.

✓ **Correct brand assigned as default**: Appropriate brand guidelines are selected.

✓ **Realistic scope**: Avoid requests for layout changes, styling, or structural edits.

## Scenario-based prompt examples

Always provide context and the value proposition so the AI can generate relevant content.

>[!NOTE]
>
>While you can currently only generate and launch email campaigns, you can always ask Coworker to generate copy for social media, WhatsApp, or SMS.

<table style="table-layout: fixed; border-collapse: collapse; border: 0;">
<thead>
<tr style="border: 0;background-color: #FFFFFF;">
<th>Industry</th>
<th>Example prompt</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>B2B Technology</strong></td>
<td>"Generate a four-touch email campaign to demonstrate ROI and technical specifications while addressing security concerns for IT decision-makers evaluating our cloud infrastructure solution, emphasizing 99.9% uptime SLA, SOC 2 compliance, and 40% cost savings."</td>
</tr>
<tr>
<td><strong>E-commerce Retail</strong></td>
<td>"Generate a single-touch campaign to create urgency around limited-stock holiday items while highlighting free shipping and easy returns for last-minute shoppers, emphasizing limited quantities (less than 50 remaining), and 24-hour shipping cutoff."</td>
</tr>
<tr>
<td><strong>Education & Training</strong></td>
<td>"Generate a two-touch campaign that emphasizes career advancement outcomes and industry certifications while showcasing instructor expertise, highlighting 92% job placement rate, and project-based curriculum."</td>
</tr>
<tr>
<td><strong>Consulting</strong></td>
<td>"Generate a three-touch campaign to nurture enterprise prospects by showcasing three customer success stories with detailed ROI metrics (IBM: 45% cost reduction, Accenture: 200% lead increase, Microsoft: 60% time savings), targeting IT directors at companies with 1000+ employees."</td>
</tr>
</tbody>
</table>

## General marketing prompt ideas

### Content marketing

- "Generate 20 blog topics that answer common questions from first-time homebuyers."
- "Brainstorm LinkedIn post ideas for a B2B cybersecurity startup."
- "Create a three-month content calendar focused on educating new customers."
- "Suggest content themes that can be repurposed into blogs, videos, newsletters, and social posts."

### Email marketing

- "Generate a welcome email sequence for new subscribers interested in sustainable fashion."
- "Brainstorm subject lines that create curiosity without sounding like clickbait."
- "Suggest re-engagement campaign ideas for inactive customers."
- "Create lifecycle email ideas for users who have completed onboarding."

>[!MORELIKETHIS]
>
>Browse more [prompt patterns](use-cases.md) for Coworker Campaigns.
