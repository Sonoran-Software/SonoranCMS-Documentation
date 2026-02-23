---
description: Create powerful automations with your custom community rosters!
---

# Roster Automations

{% embed url="https://app.guidde.com/share/playbooks/ox4JpYzJkH8RACzRs43FUF?origin=G25dDmjNZ2b8ccFUz9X7G7W8T1k1" %}

## Roster Trigger Actions

Communities can use the [**Actions**](../administrative/actions.md) panel to send webhooks, in-game messages, and other automated tasks. These actions can run on a schedule or be triggered when roster cells change.

**Example:**\
A community roster includes a **Status** column that automatically switches members between **Active** and **Inactive** based on their recent in-game activity. When a member’s playtime drops below the required threshold and their status updates to _Inactive_, a Discord webhook should be sent automatically.

_**Note:** Activity time columns update automatically when new logs (join/leave game) are created. If a member hasn’t logged in recently, no logs exist to trigger a recalculation, so a 12-hour scheduled task re-processes them._

<figure><img src="../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

## Edit Roster on Form Stage

[Custom form stages](../forms/creating-custom-forms.md#form-stages) can also update rosters. For example, when a leave-of-absence (LOA) submission moves to the **Accepted** stage, the submitter’s **Status** field can automatically be set to **LOA**.

<figure><img src="../../.gitbook/assets/Screenshot 2026-02-13 at 11.02.53 AM.png" alt="" width="375"><figcaption></figcaption></figure>
