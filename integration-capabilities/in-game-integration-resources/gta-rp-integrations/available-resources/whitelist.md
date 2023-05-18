---
description: A whitelist system that utilizes Sonoran CMS's game whitelist system.
---

# Whitelist

{% hint style="success" %}
Looking for VPS, web, or dedicated hosting? Check out our official [server hosting](../../../../other-products/server-hosting.md)!
{% endhint %}

This whitelist resource utilizes Sonoran CMS's to enforce player connections.

![Sonoran CMS - Whitelist](../../../../.gitbook/assets/CMS-WL.png)

{% embed url="https://www.youtube.com/watch?v=4PAtKYQokXE" %}

### Installation

### 1. Download the Core Resource

This resource requires the [CMS core](core.md) for push event handling and API key configuration.

### 2. Download the Resource

Click [<mark style="color:blue;">here</mark>](https://github.com/Sonoran-Software/sonoran\_whitelist) to download the whitelist resource.

### 3. Install the Resource

Follow the [standard resource installation guide](../gta-rp-resource-installation/) for the whitelist resource.

### 4. Setup Whitelist Permissions

Navigate to the Department Manager within the Administrative Panel.

Administrative Panel > Customization > Department Manager

![Sonoran CMS Department Manager](https://i.imgur.com/1x7EHpI.png)

For users in your Sonoran CMS community to be accepted through the whitelist, they'll need to be granted permission for the whitelist through rank permissions.

Granting each rank the permission of **Allow Whitelist** allows those members through the whitelist.

Granting each rank with the permission of **Block Whitelist** blockeds users from passing through the whitelist.

{% hint style="warning" %}
**Block Whitelist** will ALWAYS overrule **Allow Whitelist**\
\
If a user is granted both **Block Whitelist** and **Allow Whitelist** through various ranks they will be blocked from the whitelist. Block will always overrule allow.
{% endhint %}

![Sonoran CMS - Department Manger Server Permissions](https://i.imgur.com/yBjp7ZA.png)

### 5. Add your API ID

Ensure all players have added their [API ID](../../../../developer-api-documentation/api-integration/getting-started/api-id-system.md) to the CMS!

Configuration

## Reliability Notice

In the event that the CMS API is temporarily unavailable, this resource utilizes a local backup cache. The resource will automatically fall back to the latest saved version of the whitelist, allowing members to join as normal.
