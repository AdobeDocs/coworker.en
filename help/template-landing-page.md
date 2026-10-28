---
# TEMPLATE ONLY. Delete this line and the "hide" line below when you copy this file.
hide: true

# TITLE AND DESCRIPTION
# Title: title case, 60 characters or fewer. Use the pattern "CX Enterprise Coworker in [Application]".
# Description: one or two sentences, about 150-160 characters. Start with "Learn how Coworker..." and name two or three things the reader can do in the application.
title: CX Enterprise Coworker in [Application]
description: Learn how Coworker's conversational AI helps you [first thing], [second thing], and get more done in [Application].

# LANDING PAGE FIELDS
# A landing page is a catalog of cards. It has no video of its own, so the duration is 0.
doc-type: Catalog
duration: 0
last-substantial-update: 2026-01-01
nudge: true

# AUDIENCE FIELDS
# Keep role and role_v2 in sync, and level and level_v2 in sync. Remove the roles and levels that do not apply.
role: Leader, User, Developer, Admin
level: Beginner

# PRODUCT AND TAGGING FIELDS
# Add the product ID and label for the host application (for example, Experience Manager).
# Do not add a TQID line. The publishing system adds it.
product_v2:
  - id: [host product ID]
    internal-label: [Host product]
role_v2:
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
    internal-label: Leader
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
---
<!--
TEMPLATE GUIDANCE. Delete this comment block before you commit a new page.

PURPOSE
Use this layout for a Coworker landing page in an application's tutorial
repository. The page introduces Coworker for that application and sends
readers to videos and articles through cards. It does not contain steps.
The reader should leave the page knowing what Coworker can do in the
application and where to go next.

HOW TO USE THIS FILE
1. Copy this file into your repository. Use a descriptive, lowercase,
   hyphenated file name, for example aem-in-coworker.md.
2. Delete the two "TEMPLATE ONLY" lines in the front matter.
3. Replace everything in [brackets]. Add or remove card sections as needed,
   but keep the order: Get started, application use cases, cross-application
   workflows.
4. Write the card source (see below) in an HTML comment above each card block.
   Generate the card HTML from it using your team's card process.
5. Add a TOC entry for the page.

SECTION ORDER
1. Introduction, with no heading, below the H1.
2. Get started with Coworker: cards for readers new to Coworker.
3. [Application] in Coworker: cards for use cases in the application.
4. CX Enterprise workflows: cards for use cases that span the application and
   other CX Enterprise applications. Delete this section if you have none.

HOW CARDS WORK
Each card section has two parts, in this order:
a. The card source: an HTML comment. Its first line is the word CARDS. After
   a blank line, add one entry per card, in this form:

   * https://experienceleague.adobe.com/en/docs/path/to/target-page
     {title = Card title}
     {description = One sentence that says what the reader gets.}
     {image = https://video.tv.adobe.com/v/VIDEO_ID?format=jpeg}
     {cta = Watch}

b. The generated card HTML, which sits between the START CARDS HTML and
   END CARDS HTML comments. Never edit it by hand. To change a card, edit
   the card source and generate the HTML again. Leave the generated block
   out of a new page until the card source is final.

CARD RULES
- Use a full URL for every card target, because the target pages usually live
  in another repository. Do not use relative paths to pages.
- title: the name of the target page, in sentence case.
- description: one sentence, 160 characters or fewer. Start with a verb that
  tells the reader what they can do, for example "Ask Coworker to..." or
  "Learn how to...". Keep descriptions in a section parallel.
- cta: use Watch for a video page, and Get Started for a documentation page.
- image: leave it out when the target page has a video, because the video
  thumbnail is used. Add it when the target has no video or you want a
  different frame. Use a full URL, or a path to an image in this repository.
- Cards can sit in any number. Keep a section to six cards or fewer, and
  split a longer section by theme.
- Do not leave blank lines inside a card entry. A stray line between entries
  can break the card list.

STANDARD CARDS FOR THE GET STARTED SECTION
Use the same two cards on every Coworker landing page, so readers see
consistent starting points:
- The CX Enterprise Coworker guide home page (cta: Get Started).
- The "Get started with CX Enterprise Coworker Chat" video playlist (cta: Watch).
Copy their current URLs, titles, and descriptions from a recently published
landing page, so they stay in step with the rest of the set.

WRITING THE INTRODUCTION
- Say what Coworker does in this application, in terms of work the reader does
  today (for example, "generate assets" or "check brand compliance").
- Include one example prompt in quotation marks.
- Say that the reader stays in control by reviewing and approving results.
- Make claims you can support. Avoid superlatives and statements about how
  Coworker was trained.
- Use "Adobe CX Enterprise Coworker" at first mention on the page, and
  "Coworker" after that.
-->

# CX Enterprise Coworker in [Application] {#page-id}

Adobe CX Enterprise Coworker is Adobe's conversational AI for CX Enterprise applications. In [Application], you describe what you want in plain language, for example, "[example prompt one]" or "[example prompt two]". Coworker plans the work, runs it across your connected Adobe applications, and shows you the results for review.

[One or two sentences on what changes for the reader in this application, and how they stay in control through review and approval.]

## Get started with Coworker {#get-started}

[One sentence for readers who are new to Coworker. Say what they will understand after using these resources.]

[Card source and generated card HTML for the standard Get started cards.]

## [Application] in Coworker {#application-use-cases}

[One or two sentences that summarize the use cases in this section and the results the reader can expect.]

[Card source and generated card HTML. One card per use case page or video.]

## CX Enterprise workflows {#cx-enterprise-workflows}

[One sentence that explains how Coworker works across [Application] and other CX Enterprise applications. Delete this section if you have no cross-application cards.]

[Card source and generated card HTML. One card per cross-application workflow.]
