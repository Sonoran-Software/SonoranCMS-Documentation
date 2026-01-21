---
description: Log player records for warnings, punishments, notes, and more!
---

# Player Records

## Creating Player Records

### Via CMS Panel

<details>

<summary>Via CMS Panel</summary>

New player records can be created directly from the ER:LC server dashboard.

* **Kick** and **Ban** records automatically execute the corresponding in-game commands.
* **Disciplinary Point** records add a specified number of points to a user and can be used for warnings or punishments.
* **Note** records allow staff to store important information or observations about a player.

<figure><img src="../../../.gitbook/assets/image (23).png" alt="" width="375"><figcaption></figcaption></figure>

</details>

### Via Discord Bot

<details>

<summary>Via Discord Bot</summary>

<figure><img src="../../../.gitbook/assets/image (36).png" alt=""><figcaption></figcaption></figure>

Player records can be added via [Discord bot](../../discord-bot-integration.md) by using the `/erlc record` command.

* **ServerID** specifies the ER:LC server you wish to add this player record to.
* **Player** is a selected Discord user or Roblox user ID.
  * Players must [have their Discord linked](../installation.md#id-3.-link-roblox-and-discord-to-cms) for this to work!
* **Type** is the type of player record (kick, ban, disciplinary, note, etc.)
* Additional inputs may be needed for reasoning, points, etc.

</details>

### Via In-Game Command

<details>

<summary>Via In-Game Command</summary>

Players in-game can use the `:log` command to create records.

Syntax: `:log record [type] [player name] [points - optional] [reason]`

Example: `:log record note John This is an example note!`

Record Types:

* `points` (uses extra `[points]` parameter)
* `note`
* `kick`
* `ban`
* [Custom Log Type](moderation.md#custom-record-types)

Players can also manage their timeclock in-game using the `:log` command.

[Learn more about in-game timeclock commands here.](shifts-and-activity.md#timeclock)

</details>

## Adding Custom Record Types

Communities can [configure additional custom record types in the Moderation panel](moderation.md#custom-record-types).

## Searching Player Records

### Search Filters

<details>

<summary>Search Filters</summary>

Find a specific record by expanding the filter menu on the Latest Activity section to specify a record's type, staff member, user, and date range.

<figure><img src="../../../.gitbook/assets/image (20).png" alt="" width="375"><figcaption></figcaption></figure>

</details>

### In Latest Activity

<details>

<summary>In Latest Activity</summary>

Click the orange icon to toggle the latest activity from viewing all activity logs and records to viewing only recently added records.

<figure><img src="../../../.gitbook/assets/image (21).png" alt="" width="375"><figcaption></figcaption></figure>

</details>

### In Player Activity

<details>

<summary>In Player Activity</summary>

Click any player to open their account modal. You can view all recent activity and records in the `Activity` expansion area. Additionally, click the orange icon to toggle from viewing all activity logs and records to viewing only recently added records.

</details>

## Editing Player Records

<details>

<summary>Editing Player Records</summary>

Click any player record to open it in the editor. Here, you can modify the record and view the record's edit history.

<figure><img src="../../../.gitbook/assets/image (22).png" alt="" width="375"><figcaption></figcaption></figure>

</details>
