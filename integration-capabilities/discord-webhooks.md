---
description: >-
  Receive instant notifications in your Discord channel when new forms are
  submitted, community customization changes, and much more!
---

# Discord Webhooks

{% embed url="https://www.youtube.com/watch?v=Y6CFMpj1LT8" %}

{% hint style="warning" %}
Currently, Discord webhooks can only be created using the Desktop version of Discord.
{% endhint %}

### 1. Open your Server Settings

Open the "Server Settings" panel in the top right of your Discord server.

![Discord Server Settings](<../.gitbook/assets/Screen Shot 2020-08-20 at 10.56.54 PM.png>)

### 2. Open your Discord Integrations

In the server settings panel, select the “Integrations” tab.

![Discord Server Settings - Integrations](<../.gitbook/assets/Screen Shot 2020-08-20 at 10.54.04 PM.png>)

### 3. View your Webhooks

On the right, click to view all of your current Discord webhooks.

![Discord View Webhooks](<../.gitbook/assets/Screen Shot 2020-08-20 at 10.54.37 PM.png>)

### 4. Create a New Webhook URL

Select the "New Webhook" button.

![Discord New Webhook](<../.gitbook/assets/Screen Shot 2020-08-20 at 10.54.59 PM.png>)

### 5. Customize the New Webhook

Here, you can set the Webhook name, channel and icon.

Press the "Copy Webhook URL" button to copy the webhook's URL.\
Press the "Save Changes" button to save your new webhook in Discord.

![Discord Webhook Creation & Settings](<../.gitbook/assets/Screen Shot 2020-08-20 at 10.55.39 PM.png>)

### 6. Configure the Sonoran CMS Webhook

In the Sonoran CMS Administrator Panel, under Advanced select `Integrations`> `Discord`\
Paste your Webhook URL in the desired webhook configuration box.\
When you are done editing, click anywhere outside and it will automatically save any changes.

![Sonoran CMS - Discord Webhook Setup](../.gitbook/assets/CMS\_DiscordIntegrationWebhooks.png)

### 7. Role Mention

{% hint style="info" %}
Copying IDs in Discord requires Developer mode to be enabled.

\
Go to `User Settings` > `Advanced` > `enable Developer Mode`
{% endhint %}

To tag and mention a role in the webhook edit the `Webhook Content` box and format the mention as `<@&ID>` with `ID` being the Discord Role ID.

You can copy a Discord Role ID in your Discord server's `Settings` > `Roles` > Right-Click on the role > `Copy ID`

Example: `<@&1234567890>`

<figure><img src="../.gitbook/assets/Screen Shot 2023-01-29 at 3.08.10 PM.png" alt=""><figcaption><p>Discord Role ID Copy</p></figcaption></figure>

### 8. User Mention

{% hint style="info" %}
Copying IDs in Discord requires Developer mode to be enabled.

\
Go to `User Settings` > `Advanced` > `enable Developer Mode`
{% endhint %}

To tag and mention a user in the webhook edit the `Webhook Content` box and format the mention as `<@ID>` with `ID` being the Discord User ID.

You can copy a Discord User ID in your Discord. Right-Click on the user > `Copy ID`

Example: `<@1234567890>`
