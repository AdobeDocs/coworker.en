---
description: Learn how to launch a campaign, schedule when it goes out and how often, and permanently stop a live campaign that is actively sending.
title: Launch and manage a campaign
product_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: CX Enterprise Coworker
feature_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: CX Enterprise Coworker
---
# Launch and manage a campaign {#launch-campaign}

After your campaign is created, learn how to launch it, schedule when it goes out, and stop it if needed.

>[!AVAILABILITY]
>
>Launch campaign is currently only available to users in North American regions.

## Launch a campaign

1. In your completed campaign, click **Review and launch**.

   >[!NOTE]
   >
   >If anything is missing, a dialog appears, listing what you need to complete. Make the fixes and reselect **Review and launch**.

1. After the campaign passes the readiness check, the launch dialog opens, showing a preview of the email and audience.

1. Review the schedule shown in the dialog. To change it, use the schedule options described in [Schedule when a campaign launches](#schedule-when-a-campaign-launches), then click **Save**.

1. Click **Launch campaign** when done.

>[!NOTE]
>
>- A campaign can't launch with a sample (non-real) audience, email drafts that have not been proofed, or unconfigured sending settings.
>
>- If you schedule a campaign, you can still edit it prior to its launch. There's no need to switch to draft mode.

## Schedule when a campaign launches {#schedule-when-a-campaign-launches}

When launching a campaign, you can choose exactly when it goes out: immediately, at a specific future date and time, or on a recurring schedule. You can also come back later and change the schedule of a campaign that's already been launched or scheduled.

### Prerequisites

The campaign must be ready to launch (all required setup complete).

### Schedule a campaign at launch

1. From the campaign, click **Review and launch**.

1. In the launch dialog, choose a schedule option:
   - **Now**: the campaign starts sending immediately after launch.
   - **Schedule once**: pick a future **Start date** (date and time together).
   - **Recurring**: choose a **Frequency** (Daily, Weekly, or Monthly) and a start time, then set the recurrence pattern (see fields below).

1. If Recurring is selected, choose whether the campaign ends **Never** or **On a date**, and pick an end date if applicable.

1. Confirm to launch the campaign with the selected schedule.

### Edit an existing schedule

1. Open the campaign and go to its settings.

1. Find the schedule section and select the current schedule summary.

1. Update the schedule using the same options described above.

1. Save the change.

### Input fields

| Field | Description | Required? |
| --- | --- | --- |
| Schedule mode | Choice of Now, Schedule once, or Recurring | Yes |
| Start date | Date and time the campaign starts (Schedule once mode) | Yes, for Schedule once |
| Frequency | Daily, Weekly, or Monthly (Recurring mode) | Yes, for Recurring |
| Start time | Time of day the recurring campaign sends | Yes, for Recurring |
| Days of week | Which day(s) the campaign repeats on | Yes, for Weekly frequency |
| Day of month | Which day of the month the campaign repeats on | Yes, for Monthly frequency |
| End campaign | Never, or on a specific end date | Yes, for Recurring |

### Things to note

- Recurring campaigns can be set to run indefinitely or until a specific end date. One-time and immediate campaigns don't have an end date option, since they run once.
- Scheduling does not support custom repeat intervals, such as "every 2 weeks" or "every 3 days." It also does not support relative monthly recurrence, such as "the second Monday of the month."

## Stop a campaign {#stop-campaign}

You can stop a campaign that is actively sending (a "live" campaign) directly from the campaign detail page.

>[!CAUTION]
>
>Stopping a campaign is permanent. Recipients stop progressing through the campaign immediately, and the campaign cannot be resumed or restarted afterward. To send again, you must create a new campaign and launch that one.

<!--

### Prerequisites

- [NEEDS INPUT - to confirm with engineer: does stopping a campaign require a specific role or permission, or can any user with campaign access do this?]

-->

### How to stop a campaign

1. Open a campaign that is currently live.

1. In the campaign detail header, click **Stop Campaign**.

1. Click **Stop** to confirm.
