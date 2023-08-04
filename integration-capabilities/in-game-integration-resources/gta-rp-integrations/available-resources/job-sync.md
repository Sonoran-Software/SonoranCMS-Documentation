---
description: >-
  A in-game way to utilize Sonoran CMS's roster & rank system to sync your
  in-game jobs and ranks.
---

# Job Sync

{% hint style="success" %}
Looking for VPS, web, or dedicated hosting? Check out our official [server hosting](../../../../other-products/server-hosting.md)!
{% endhint %}

This resource is a in-game way of automatically syncing jobs and ranks to match roster information in the Sonoran CMS system/community.

## Installation

### 1. Download the Core Resource

This resource requires the [CMS core](core.md) for push event handling and API key configuration.

### 2. Download the Resource

Click [<mark style="color:blue;">here</mark>](https://github.com/Sonoran-Software/sonorancms\_jobsync) to download the clock in resource.

### 3. Install the Resource

Follow the [standard resource installation guide](../gta-rp-resource-installation/) which uses the whitelist resource as an example.

Placing it inside the \[sonorancms] alongside sonorancms & sonorancms\_updatehelper.

### 4. Add your API ID

Ensure all players have added their [API ID](../../../../developer-api-documentation/api-integration/getting-started/api-id-system.md) to the CMS!

## Configuration

| Config Option  | Description                                                                                                                                                                                                  |
| -------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| rank\_mapping  | \["9dd1fea1-2360-4be2-923b-71b0c87944d0"] = {job = 'police', rank = 2}                                                                                                                                       |
| offline\_cache | true -- If set to true jobs will be cached on the server in-case CMS goes down, the cache will be updated every time the player rejoins, the rank refresh command is run, or has a rank change in CMS Footer |

## Getting Rank UUIDs

### 1. Open Department Configuration Page

![](<../../../../.gitbook/assets/image (4) (1) (1).png>)

### 2. Select the Rank

![](<../../../../.gitbook/assets/image (18).png>)

### 3. Copy Rank ID

![](<../../../../.gitbook/assets/image (10).png>)
