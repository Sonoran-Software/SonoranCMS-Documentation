---
description: Get started with Sonoran's CMS, CAD, and Discord role sync!
---

# Getting Started

<figure><img src="../../.gitbook/assets/crossrolesync-v6.png" alt=""><figcaption><p>Sonoran CMS - Discord Sync</p></figcaption></figure>

## Setup

{% hint style="warning" %}
This system utilizes API endpoints that require the **Standard** version of Sonoran CMS or higher. For more information, view our [pricing ](../../pricing/pricing-faq/)page.
{% endhint %}

{% hint style="warning" %}
Setting up the bot requires you to have the "Manage Server" permissions on the Discord server for security reasons. You must also have access to your server's [API Key information](../../developer-api-documentation/api-integration/getting-started/retrieving-your-credentials.md).
{% endhint %}

### 1. Invite the Bot to Your Server

[Invite the bot to your Discord server](https://discord.com/api/oauth2/authorize?client\_id=1060274480930361424\&permissions=805306368\&scope=bot%20applications.commands).

You must have the "Manage Server" permission to add bots; plus any permissions the bot requires to function.

### 2. Run the Setup command

* After inviting the bot, run the `/setup` command.
* Enter your [Sonoran CMS ID and API key](../../developer-api-documentation/api-integration/getting-started/#gather-your-credentials).
* (OPTIONAL) Enter your [Sonoran CAD ID and API key](https://info.sonorancad.com/sonoran-cad/api-integration/getting-started/retrieving-your-credentials).

<figure><img src="../../.gitbook/assets/Screenshot_11.png" alt=""><figcaption></figcaption></figure>

You will then be presented with the results of the setup.

<figure><img src="../../.gitbook/assets/Screenshot_1.png" alt=""><figcaption></figcaption></figure>

### **3. Invite to Additional Servers**

Multi-server support is currently unavailable in the closed beta.

## Command Reference

Learn more about the available slash commands with Sonoran Bot:

{% content-ref url="commands-reference.md" %}
[commands-reference.md](commands-reference.md)
{% endcontent-ref %}
