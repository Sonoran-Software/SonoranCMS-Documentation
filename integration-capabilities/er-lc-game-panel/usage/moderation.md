---
description: Configure moderation standards in the ER:LC panel.
---

# Moderation

## Priority Player List

<details>

<summary>Priority Player List</summary>

The Priority Player List highlights in-game users with specific CMS ranks by moving them to the top of the player list. This is useful for quickly identifying which staff members (or other ranks) are currently online.

Players with one of the configured CMS ranks will display a rank badge on their player card and appear at the top of the dashboard list.

<div><figure><img src="../../../.gitbook/assets/image (16) (1).png" alt="" width="375"><figcaption></figcaption></figure> <figure><img src="../../../.gitbook/assets/image (9) (1).png" alt="" width="207"><figcaption></figcaption></figure></div>

</details>

## Custom Record Types

<details>

<summary>Custom Record Types</summary>

These custom log types can be created via [CMS](player-records.md#via-cms-panel), [Discord](player-records.md#via-discord-bot), or [in-game](player-records.md#via-in-game-command)!

<figure><img src="../../../.gitbook/assets/image (6).png" alt=""><figcaption></figcaption></figure>

Create additional, custom player record types for things like RDM, Combat, and more!

</details>

## Request Form Types

<details>

<summary>Custom Request Forms</summary>

Request form types are CMS form submissions that are displayed [right in the ER:LC panel](dashboard.md#latest-activity) for quick processing.

**Example: Priority Requests**

Many communities require approval for a "priority" scene (a roleplay scene with multiple users, weapons, etc.)

In the **Request Form Types** we've selected a custom CMS form for **Priority Requests**. When a user submits this form and it's in the **Awaiting Review** stage, it will be [displayed on the ER:LC panel](dashboard.md#latest-activity).

Additionally, players can submit this form (as long as their Roblox account is linked) from in-game using a custom `:log` comman&#x64;**.** All additional text after the command will be inserted into the selected form field.

Ex: `:log prio this is an example` > would create a new **Priority Request** form submission with "this is an example" inserted into the form field "What is the priority for?"

**Stage Actions**

When a form stage is changed [automated actions, including ER:LC commands](cms-integrations.md#stage-actions) can be ran.

<figure><img src="../../../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (2) (1).png" alt=""><figcaption></figcaption></figure>

</details>

## Username Moderation

<details>

<summary>Username Moderation</summary>

Even with Roblox’s built-in username moderation, some inappropriate names can still bypass filters. The Username Moderation panel allows you to automatically kick users with “All” or “Others” in their username — preventing commands targeting them from affecting the entire server.

You can also configure AI-based moderation standards to automatically detect and handle inappropriate usernames.

<figure><img src="../../../.gitbook/assets/image (17).png" alt="" width="375"><figcaption></figcaption></figure>

</details>
