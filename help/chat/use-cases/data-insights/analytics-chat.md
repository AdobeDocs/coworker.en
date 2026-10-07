---
title: Get Started Analyzing Data with Coworker Chat
description: Learn how to use Adobe CX Enterprise Coworker Chat to analyze Customer Journey Analytics data, build funnels, and find where customers drop off in the journey.
product_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: CX Enterprise Coworker
feature_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: CX Enterprise Coworker
---
# Get started analyzing data with Coworker Chat

Set up Adobe CX Enterprise Coworker Chat to analyze your Customer Journey Analytics data views or Adobe Analytics report suites, then follow a working example. For an overview of what you can do with Coworker Chat, including use cases, skills, and best practices, see [Analyze data with Coworker Chat](/help/chat/use-cases/data-insights/analytics-overview-v2.md).

Before you begin, learn the Coworker Chat interface and configuration options, then ensure Coworker is connected to Customer Journey Analytics or Adobe Analytics and the relevant data views or report suites.

## Before you begin

### Data access and permissions

Coworker Chat inherits permissions from Customer Journey Analytics or Adobe Analytics. You can access only those data views, report suites, dimensions, metrics, and segments available to you in Analysis Workspace. 

### Interface and configuration options

Before you use Coworker Chat with your Customer Journey Analytics or Adobe Analytics data, learn how to sign in and manage configuration options for the following features:

* Chat inputs
* Conversations
* Marketplaces
* MCP servers
* Memory
* Plugins
* Skills
* And more

For more information, see the [Coworker Chat UI guide](/help/chat/ui-guide.md).

## Verify that Coworker Chat is connected to Customer Journey Analytics

In Coworker Chat, verify that Coworker is connected to Customer Journey Analytics:

1. Select the MCP icon in the left rail, then make sure that [!UICONTROL **cja-mcp**] is available in your list of connected MCP servers.

   ![The MCP icon highlighted in the Coworker left rail](../../assets/coworker-mcp-cja.png)

1. (Conditional) If [!UICONTROL **cja-mcp**] is not yet connected, select [!UICONTROL **Add MCP Server**], specify cja in the [!UICONTROL **Server Name**] field and select it when it appears, then select [!UICONTROL **Add Server**].

## Connect to the right data view or report suite

A data view is a container in Customer Journey Analytics that determines how data is interpreted. A report suite is a container in Adobe Analytics that holds the data collected from your sites and apps.

You might have access to various data views in Customer Journey Analytics or report suites in Adobe Analytics. Each might contain different dimensions and metrics that Coworker can use when analyzing data.

### Decide which data views or report suites you want to use

Tell Coworker the types of questions you want answered, and ask it which data views or report suites you have access to that provide that information. You can also [set your data view or report suite as a preference in memory](#add-a-data-view-or-report-suite-preference-in-memory).

**You:**

>[!BEGINSHADEBOX]

I'm interested in learning where customers drop off in the customer journey. Which data views in Customer Journey Analytics do I have access to that would be able to answer this question for me?

>[!ENDSHADEBOX]

**Coworker Chat response:**

>[!BEGINSHADEBOX]

You have access to three data views. The `Customer lifecycle` data view contains the following dimensions and metrics, which would be best for answering your question.

>[!ENDSHADEBOX]

**You:**

>[!BEGINSHADEBOX]

Great, let's use that data view.

>[!ENDSHADEBOX]

**Coworker Chat response:**

>[!BEGINSHADEBOX]

Okay, I'll use the `Customer lifecycle` data view to answer future questions in this chat session.

>[!ENDSHADEBOX]

### Add a data view or report suite preference in Memory

Coworker Chat contains a memory feature that allows you to provide it with access to information that spans across all chats. It's a good practice to add your preferred data views or report suites as preferences in Coworker's memory.

1. In Coworker Chat, in the left nav, select the Memory icon.

1. On the Memory page, in the [!UICONTROL **Stored preferences**] section, specify one or more data views or report suites that you want Coworker Chat to use in your chats.

   ![Memory section in the left rail](../../assets/coworker-memory.png)

## Example: Find where customers drop off

You can ask Coworker Chat to use your data to analyze any business question.

For example, as a marketing manager, merchandiser, or growth lead, you might want to understand where customers abandon the path to purchase, why they did, and what can be done to drive higher conversion rates.

>[!NOTE]
>
>The figures below are illustrative sample data for a fictional retailer, [!DNL TechPulse Electronics], used to show the shape of the conversation.

### The types of questions you can ask

You don't need to know what a "fallout visualization" is, or which metric goes in which slot. Instead, describe the outcome you care about in plain language:

* "Where are we losing people on the way to purchase?"
* "What's my full conversion funnel, from product view to checkout?"
* "Which marketing channels leak the most between cart and purchase?"
* "Is cart abandonment worse on mobile or desktop?"
* "Do people from paid social convert differently than people from email?"

### The conversation

#### 1. Start with the business question

**You:**

>[!BEGINSHADEBOX]

Where are we losing people on the way to purchase?

>[!ENDSHADEBOX]

**Coworker Chat response:**

Notice that Coworker Chat chooses the right visualization, sequences the touchpoints, and even adds recommended next steps.

>[!BEGINSHADEBOX]

![Funnel table showing session counts, conversion rates, and drop-off at each step from sessions to purchase](../../assets/coworker-funnel-response.png)

This is a funnel question — let me run the conversion funnel to see where drop-off happens on the path to purchase.

Here's where you're losing people:

| Funnel step | Count | Conversion to next | Drop-off |
| --- | --- | --- | --- |
| Sessions | 137,476 | 45.0% view a product | 55% leave without browsing products |
| Product views | 61,845 | 55.0% add to cart | 45% browse but don't add |
| Cart adds | 34,045 | 16.4% purchase | 83.6% abandon cart |
| Purchases | 5,582 | — | — |

**The big finding: cart to purchase is your biggest leak**

28,463 people add items to their cart but never complete the purchase. That's an 83.6% cart-to-purchase drop-off rate — by far the largest single point of failure.

**What this tells you about priorities:**

| Priority | Problem | Scale of opportunity |
| --- | --- | --- |
| #1 | Cart to purchase abandonment (83.6% drop) | 28,463 lost buyers |
| #2 | Session to product view (55% never browse) | 75,631 sessions without product engagement |
| #3 | Product view to cart (45% don't add) | 27,800 interested but uncommitted |

**Recommended next steps:**

1. Break down cart abandonment by marketing channel — are certain channels bringing low-intent traffic that adds to cart but never buys?
1. Look at cart abandonment by device type — is mobile checkout friction killing conversions?
1. Identify which products get abandoned most — pricing issue? Shipping surprise?

**Which of these would you like me to dig into next?** The channel breakdown would tell you directly which marketing actions are bringing you "almost-buyers" versus actual buyers.

>[!ENDSHADEBOX]

#### 2. Drill into the leak

**You:**

>[!BEGINSHADEBOX]

Okay, let's break down by marketing channel

>[!ENDSHADEBOX]

**Coworker Chat response:**

>[!BEGINSHADEBOX]

![Funnel table showing conversion rates and drop-off broken down by marketing channel](../../assets/coworker-funnel-response2.png)

There's a custom **Marketing Channel** dimension. Let me pull the funnel by that, then calculate the per-channel conversion rates and identify where each channel leaks.

**The verdict: the leak is not channel-specific**

This is a really revealing finding. Here's the per-channel funnel breakdown:

| Channel | Sessions | To product view | To cart add | To purchase | Overall conversion | Revenue/session |
| --- | --- | --- | --- | --- | --- | --- |
| Paid search | 43,958 | 45.1% | 54.6% | 16.6% | 4.09% | $499.58 |
| Organic search | 31,492 | 44.9% | 54.9% | 16.9% | 4.17% | $494.76 |
| Direct | 25,245 | 43.6% | 55.4% | 15.8% | 3.82% | $497.29 |
| Email | 17,586 | 45.3% | 55.4% | 16.2% | 4.07% | $501.13 |
| Paid social | 12,684 | 45.4% | 55.7% | 16.0% | 4.03% | $512.17 |
| Display | 6,511 | 45.3% | 55.7% | 16.2% | 4.09% | $501.45 |

**Key takeaways:**

1. The cart-to-purchase drop-off is uniformly bad across all channels (83-84%). This means the problem isn't about traffic quality — every channel is converting people into the cart at similar rates. The leak is in your checkout experience itself, not your marketing.
1. No channel is significantly better or worse at converting. Overall conversion rates cluster tightly between 3.8% and 4.2%, and revenue per session is nearly identical ($495-$512).
1. Where the volume impact matters most: paid search loses the most people in absolute terms (9,015 cart abandonments), followed by organic search (6,449 lost). These are the biggest dollar-value opportunities because they drive the most traffic.

**What this tells you strategically**

The marketing channels are doing their job — they're all getting people interested and adding to cart at similar rates. The problem is downstream of marketing: your checkout and payment flow is where the money is leaking.

**Recommended next investigations:**

1. Break down mobile cart abandonment by product category — is it worse for high-price items (suggesting mobile payment trust issues)?
1. Look at which marketing channels drive the most mobile traffic — are you spending paid media dollars to send people into a broken mobile funnel?
1. Check if there's a page or site-section signal — can we see which checkout pages mobile users hit last before abandoning?

**Which angle would you like to explore next?**

>[!ENDSHADEBOX]

#### 3. Keep investigating

**You:**

>[!BEGINSHADEBOX]

Interesting. Let's try breaking down by device type.

>[!ENDSHADEBOX]

**Coworker Chat response:**

>[!BEGINSHADEBOX]

![Funnel table showing conversion rates and drop-off broken down by device type](../../assets/coworker-funnel-response3.png)

**Found it: mobile checkout is broken**

The funnel is identical across devices until checkout — then mobile falls off a cliff:

| Device | Sessions | To product view | To cart add | To purchase | Overall conversion |
| --- | --- | --- | --- | --- | --- |
| Desktop | 70,172 | 44.9% | 54.8% | 23.2% | 5.70% |
| Tablet | 13,855 | 44.7% | 55.6% | 14.3% | 3.56% |
| Mobile | 53,449 | 44.9% | 55.3% | 8.1% | 2.02% |

**The smoking gun**

| Metric | Desktop | Mobile | Gap |
| --- | --- | --- | --- |
| Cart to purchase rate | 23.2% | 8.1% | 15 percentage points |
| Mobile is | — | 2.8x worse | — |
| Abandoned carts | 13,274 | 12,178 | Nearly the same absolute volume |

The browsing and add-to-cart experience is fine on mobile (identical ~45% browse rate, ~55% add-to-cart rate). People are equally interested and engaged. But something in the mobile checkout flow is killing conversions.

**The revenue opportunity**

If mobile checkout converted at the same rate as desktop, you'd gain ~1,991 additional purchases — a 35% increase in total purchase volume from fixing one experience.

**What's likely happening**

The data pattern (equal engagement, catastrophic checkout drop) is a classic signal for:

* Payment form friction on small screens (autofill issues, form layout)
* Unexpected costs revealed at checkout (shipping, tax) causing sticker shock
* Guest checkout not available or a login wall on mobile
* Page load or timeout issues during payment processing on mobile

**Recommended next steps:**

1. Break down mobile cart abandonment by product category — is it worse for high-price items (suggesting mobile payment trust issues)?
1. Look at which marketing channels drive the most mobile traffic — are you spending paid media dollars to send people into a broken mobile funnel?
1. Check if the "holiday_flash_sale" campaign had better checkout conversion — urgency-driven campaigns might overcome checkout friction

**Which would you like to explore, or is this enough evidence to take to your UX and checkout team?**

>[!ENDSHADEBOX]

#### 4. Turn it into a decision

**You:**

>[!BEGINSHADEBOX]

So what should I do?

>[!ENDSHADEBOX]

**Coworker Chat response:**

>[!BEGINSHADEBOX]

Based on what the data shows, here's where I'd focus:

* **Fix the mobile checkout — it's not a channel problem.** Every channel is converting people into the cart at a similar, healthy rate, so the ad spend is working across the board. The revenue is being lost specifically in the mobile checkout flow, which is where the fix belongs.
* **Start with payment and form friction.** These are the most common reasons high-intent mobile shoppers abandon a cart. Offering mobile wallet options and shortening the form are usually the fastest wins.
* **Re-check after the fix.** Once checkout changes ship, watch whether mobile's cart-to-purchase rate moves toward the desktop rate of 23.2%.

Want me to save this as a project so you can track it, or set an alert if mobile cart-to-purchase drops below a threshold?

>[!ENDSHADEBOX]

### What happened

In four plain-language questions, Coworker helped us:

* Build a multi-step conversion funnel and flag cart-to-purchase as the biggest leak
* Rule out marketing channel as the cause — every channel leaked at nearly the same rate
* Isolate the real problem to mobile checkout, and quantify the fix at a 35% lift in purchases
* Walk away with a specific fix to prioritize: mobile payment and form friction. This is benchmarked against desktop's 23.2% conversion rate

## Analyze in Customer Journey Analytics

After Coworker creates a visualization, you can open it in Analysis Workspace for deeper analysis and granular control. The visualization opens in a new Analysis Workspace project in Customer Journey Analytics.

To open a visualization in a new Analysis Workspace project:

1. Select [!UICONTROL **Analyze in CJA**] next to any visualization that is created in Coworker.

1. With the visualization open in Customer Journey Analytics, you can use the Analysis Workspace drag-and-drop browser interface to make modifications, further craft your analysis, create an audience, and much more. You can even share your Workspace project with anyone you choose.

   For more information about Analysis Workspace, see [Analysis Workspace overview](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/home).

## Next steps

For more use cases, the skills that Coworker Chat uses to analyze your data, and best practices for writing prompts, see [Analyze data with Coworker Chat](/help/chat/use-cases/data-insights/analytics-overview-v2.md).
