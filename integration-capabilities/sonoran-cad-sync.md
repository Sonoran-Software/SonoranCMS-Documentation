---
description: >-
  Easily manage Sonoran CAD permissions from Sonoran CMS ranks! Learn more
  below.
---

# Sonoran CAD Sync

Remove all the hassle of managing your community's Sonoran CAD permissions. Sonoran CMS is now your single point of management!

Sonoran CMS allows you to easily manage your community's Sonoran CAD permissions based on their Sonoran CMS rank automatically!

Sonoran CAD permissions can be managed via the CMS web panel, or with the Discord bot.

## Option A: Discord Bot

<figure><img src="../.gitbook/assets/crossrolesync-v6.png" alt=""><figcaption></figcaption></figure>

Learn more about Sonoran Bot managing both CMS and CAD roles!

{% content-ref url="discord-role-sync/" %}
[discord-role-sync](discord-role-sync/)
{% endcontent-ref %}

## Option B: Web Panel Sync

![Sonoran CMS x Sonoran CAD - Permission Sync](../.gitbook/assets/CMS-CAD-Sync.png)

{% hint style="warning" %}
This features requires the **standard** version of Sonoran CMS or higher. For more information, view our [pricing ](broken-reference)page.\
\
This feature also requires the **plus** version of Sonoran CAD or higher. For more information, view Sonoran CAD's [pricing](https://info.sonorancad.com/pricing/faq) page.
{% endhint %}

{% hint style="info" %}
Sonoran CAD Sync settings can only be seen and modified by the community owner.
{% endhint %}

### 1. Enter Credentials

Click the _Enable Sync_ check box and enter your Sonoran CAD community's ID & API Key.

![Sonoran CAD In-Game Integration Settings](https://i.imgur.com/nVFr3qR.png)

Your Community ID and API Key are located in Sonoran CAD's Admin Panel > Advanced > In-Game Integration > Web API.\
Enter these into your Sonoran CMS as shown below.

![Sonoran CMS - Sonoran CAD Integration Credential Inputs](https://i.imgur.com/62SdMok.png)

### 2. Configure Sync Settings

Check the sync options that best fit your community's needs, explanation of each sync feature can be found [below](sonoran-cad-sync.md#feature-overview).

### 3. Save Sync Settings

Click the green _Save_ button above your Sonoran CAD credentials, this will enable and save your credentials.

![Sonoran CMS - Sonoran CAD Integration Saving Credentials](https://i.imgur.com/F6IXyAm.png)

### 4. Map CAD Permissions to Ranks

To edit, click any rank on the left-hand side. This tree will contain all department and ranks that your community currently has. Enable all permissions you want to grant to the individual with this rank.

{% hint style="warning" %}
Permission syncs from Sonoran CMS will set the user's permissions explicitly to what is mapped in the CMS and will wipe any non-enabled permissions.
{% endhint %}

![Sonoran CMS - Sonoran CAD Integration Permission Mapping](https://i.imgur.com/EzjZpM3.png)

### 5. Save CAD Permission Mapping

On the Rank Selector tree on the left-hand side, on the bottom, click the _Save_ button. This will save all permission mappings and trigger a mass sync of all permissions.

![Sonoran CMS - Sonoran CAD Integration Rank Selector](https://i.imgur.com/o3Fc6NY.png)

## Feature Overview

### Kick & Ban Sync

This will trigger an action to kick the same user from your Sonoran CAD community if they're kicked from your Sonoran CMS community. This also applies to bans.

### API ID Sync

_Releasing in v0.5.24_

This will sync all member's API IDs to the same user from your Sonoran CAD community, if they have a Discord account linked to their account it will sync that ID as well.

{% hint style="info" %}
API ID Sync to CAD will overwrite any API IDs that are set by the user in Sonoran CAD upon each sync. All API IDs that are sent to the CAD from CMS will replace what is currently there.
{% endhint %}

### Auto Join CAD

_Releasing in v0.5.24_

This will have all new members that join your community automatically join your Sonoran CAD community under the same user ID.
