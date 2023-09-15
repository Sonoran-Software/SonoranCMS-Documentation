---
description: >-
  Receive instant notifications in your Discord channel when new forms are
  submitted, community customization changes, and much more!
---

# Discord Webhooks

{% embed url="https://www.youtube.com/watch?v=EsoYW-tROMs" %}

{% hint style="info" %}
**Notice:** Managing Discord Webhooks now requires Sonoran Bot as of [v0.5.56](../roadmap/changelog.md#v0.5.56-beta-pending-release)!
{% endhint %}

### 1. Invite & Configure Sonoran Bot

In the Sonoran CMS Administrator Panel, under Advanced select `Integrations`> `Discord`\
In order to configure your Sonoran CMS Webhooks you must invite and configure Sonoran Bot. Follow each step in the setup process stepper directly in the Sonoran CMS UI.

<figure><img src="https://i.imgur.com/SVnephg.png" alt=""><figcaption><p>Sonoran CMS - Discord Webhook Setup - Sonoran Bot Setup</p></figcaption></figure>

### 2. Configure the Sonoran CMS Webhook

Select the channel you want your webhook logs to send to for each log type\
When you are done editing, click anywhere outside and it will automatically save any changes.

![Sonoran CMS - Discord Webhook Setup](../.gitbook/assets/CMS\_DiscordWebhookSettings.png)

### 3. Role Mention

In the middle drop down menu you can select any roles you would like to be mentioned in the webhook. You can select as many roles as you wish and this will mention these roles at the beginning of the message.

<figure><img src="../.gitbook/assets/CMS_DiscordWebhookRoleMention.png" alt=""><figcaption><p>Sonoran CMS - Discord Webhook Mentions Menu</p></figcaption></figure>

Alternatively, if you would like to integrate the mention into the content message, you can also manually mention roles.

{% hint style="info" %}
Copying IDs in Discord requires Developer mode to be enabled.

\
Go to `User Settings` > `Advanced` > `enable Developer Mode`
{% endhint %}

To tag and mention a role in the webhook edit the `Webhook Content` box and format the mention as `<@&ID>` with `ID` being the Discord Role ID.

You can copy a Discord Role ID in your Discord server's `Settings` > `Roles` > Right-Click on the role > `Copy ID`

You can also right-click on any user's role in their profile popup and copy the Role ID from there.

Example: `<@&1234567890>`

<figure><img src="../.gitbook/assets/Screen Shot 2023-01-29 at 3.08.10 PM.png" alt=""><figcaption><p>Discord Role ID Copy</p></figcaption></figure>

### 4. User Mention

{% hint style="info" %}
Copying IDs in Discord requires Developer mode to be enabled.

\
Go to `User Settings` > `Advanced` > `enable Developer Mode`
{% endhint %}

To tag and mention a user in the webhook edit the `Webhook Content` box and format the mention as `<@ID>` with `ID` being the Discord User ID.

You can copy a Discord User ID in your Discord. Right-Click on the user > `Copy ID`

Example: `<@1234567890>`
