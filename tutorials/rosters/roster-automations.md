---
description: Create powerful automations with your custom community rosters!
---

# Roster Automations

## Roster Trigger Actions

Communities can use the [**Actions**](../administrative/actions.md) panel to send webhooks, in-game messages, and other automated tasks. These actions can run on a schedule or be triggered when roster cells change.

**Example:**\
A community roster includes a **Status** column that automatically switches members between **Active** and **Inactive** based on their recent in-game activity. When a member’s playtime drops below the required threshold and their status updates to _Inactive_, a Discord webhook should be sent automatically.

_**Note:** Activity time columns update automatically when new logs (join/leave game) are created. If a member hasn’t logged in recently, no logs exist to trigger a recalculation, so a 12-hour scheduled task re-processes them._

<figure><img src="../../.gitbook/assets/image (1) (1).png" alt=""><figcaption></figcaption></figure>

## Edit Roster on Form Stage

When a form is moved to a new stage a roster cell can be automatically updated.

{% hint style="warning" %}
Coming soon!
{% endhint %}

