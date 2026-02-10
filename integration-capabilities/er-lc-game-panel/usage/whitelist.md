---
description: >-
  The ER:LC whitelist panel enables social, server, team, vehicle, and livery
  restrictions.
---

# Whitelist

## Social Requirements

The `Social Requirements` section allows you to require that CMS accounts be linked to both Discord and Roblox accounts. When users have both social accounts connected, the ER:LC panel and Discord integrations can operate with full functionality.

### Enabling Social Requirements

<details>

<summary>Enabling Social Requirements</summary>

Toggle the `Roblox` and/or `Discord` requirement(s). Then, define custom actions to trigger when a user joins your ER:LC panel without having a linked Roblox or Discord account in the CMS.

Available actions include public or private in-game messages, Discord webhooks, push notifications, and more.

<div><figure><img src="../../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" width="375"><figcaption></figcaption></figure> <figure><img src="../../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1).png" alt="" width="243"><figcaption></figcaption></figure></div>

</details>

## Allow and Deny Players Whitelist

<details>

<summary>Allow and Deny List</summary>

The allow and deny lists let you control game access based on CMS ranks. These lists are activated once one or more ranks are configured.

When enabled, only users with a Roblox account linked to a CMS account that holds an **allowed rank** can join the server. Users without an allowed rank will be kicked automatically.

If a user’s CMS rank appears on the **deny list**, that restriction overrides the allow list — those users will be kicked upon joining.

<figure><img src="../../../.gitbook/assets/image (3) (1) (1) (1) (1) (1) (1).png" alt="" width="375"><figcaption></figcaption></figure>

</details>

## Team Locks and Restrictions

### Team Locks

Each ER:LC team can be locked down to a maximum amount of players. Teams can be locked via the CMS **Lock** icon, or via Discord bot command.

#### Lock via CMS

<details>

<summary>Lock via CMS</summary>

Next to the team, select the **Lock** icon to enable or disable the lock, then enter a number into the **Max**&#x20;

Use the **Shield** icon to add CMS ranks that bypass and ignore this lock.

<figure><img src="../../../.gitbook/assets/image (9).png" alt="" width="375"><figcaption></figcaption></figure>

</details>

#### Lock via Discord

<details>

<summary>Lock via Discord</summary>

Team locks can also be configured via [Discord bot](../../discord-bot-integration.md) by using the `/erlc lock` and `/erlc unlock` commands.

<figure><img src="../../../.gitbook/assets/image (10).png" alt=""><figcaption></figcaption></figure>

</details>

#### Lock Actions

<details>

<summary>Lock Actions</summary>

When a player joins a team that has already reached its maximum amount of players, custom actions can be used to kick the user off of the team, send a message, Discord webhook, and more!

Select **Actions** next to the team > Add a new action > And toggle the mode to **Lock** to apply this action whenever a team lock is reached.

<figure><img src="../../../.gitbook/assets/image (11).png" alt="" width="375"><figcaption></figcaption></figure>

<div><figure><img src="../../../.gitbook/assets/image (12).png" alt="" width="286"><figcaption></figcaption></figure> <figure><img src="../../../.gitbook/assets/image (13).png" alt="" width="286"><figcaption></figcaption></figure></div>

</details>

### Team Restrictions

<details>

<summary>Team Restrictions</summary>

Each team can also be locked to users with specific CMS ranks.

Select the **Shield** icon to configure which ranks are allowed to join the team.

Select the **Actions** panel to create actions that apply when a user joins a team without the proper CMS rank.

<div><figure><img src="../../../.gitbook/assets/image (14).png" alt=""><figcaption></figcaption></figure> <figure><img src="../../../.gitbook/assets/image (15).png" alt=""><figcaption></figcaption></figure></div>

</details>

## Vehicle & Livery Restrictions

<details>

<summary>Vehicle &#x26; Livery Restrictions</summary>

Vehicles and vehicle liveries can also be restricted to users with specific CMS ranks.

Just like teams, select the **Shield** icon to which ranks are allowed to use the vehicle and vehicle liveries.

Select the **Actions** panel to create actions that apply when a user uses a vehicle or livery without the proper CMS rank.

<div><figure><img src="../../../.gitbook/assets/image (16).png" alt="" width="375"><figcaption></figcaption></figure> <figure><img src="../../../.gitbook/assets/image (4) (1) (1) (1) (1).png" alt="" width="246"><figcaption></figcaption></figure></div>

</details>
