---
description: >-
  Easily manage Sonoran CAD permissions from Sonoran CMS ranks! Learn more
  below.
---

# Sonoran CAD Sync

Remove all the hassle of managing your community's Sonoran CAD permissions. Sonoran CMS is now your single point of management!

Sonoran CMS allows you to easily manage your community's Sonoran CAD permissions based on their Sonoran CMS rank automatically!

## Web Panel Sync

![Sonoran CMS x Sonoran CAD - Permission Sync](../.gitbook/assets/CMS-CAD-Sync.png)

{% hint style="warning" %}
This features requires the **standard** version of Sonoran CMS or higher. For more information, view our [pricing ](broken-reference)page.\
\
This feature also requires the **plus** version of Sonoran CAD or higher. For more information, view Sonoran CAD's [pricing](https://info.sonorancad.com/pricing/faq) page.
{% endhint %}

{% hint style="info" %}
Sonoran CAD Sync settings can only be seen and modified by the community owner.
{% endhint %}

### 1. Add New CAD Integration

Click the _Add CAD_ button or expand an existing setup

<figure><img src="https://i.imgur.com/gvmu3xB.png" alt=""><figcaption><p>Sonoran CMS - CAD Integration Setup List Area</p></figcaption></figure>

### 1. Enter Credentials

Click the _Enable Sync_ check box and enter your Sonoran CAD community's ID & API Key.

![Sonoran CAD In-Game Integration Settings](https://i.imgur.com/nVFr3qR.png)

Your Community ID and API Key are located in Sonoran CAD's Admin Panel > Advanced > In-Game Integration > Web API.\
Enter these into your Sonoran CMS as shown below.

![Sonoran CMS - Sonoran CAD Integration Credential Inputs](https://i.imgur.com/HHP3Eq0.png)

### 2. Configure Sync Settings

Check the sync options that best fit your community's needs, explanation of each sync feature can be found [below](sonoran-cad-sync.md#feature-overview).

### 3. Save Sync Settings

Click the green _Save_ button above your Sonoran CAD credentials, this will enable and save your credentials.

![Sonoran CMS - Sonoran CAD Integration Saving Credentials](https://i.imgur.com/AdZptnh.png)

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

### Multi-Setup Sync

Sync multiple Sonoran CAD communities with your single Sonoran CMS community. This will sync all of the below features with each community you have setup.

{% hint style="info" %}
Multiple CAD Sync setups requires a **PLUS** subscription or higher, **PRO** or higher allows unlimited community setups.
{% endhint %}

### Kick & Ban Sync

This will trigger an action to kick the same user from your Sonoran CAD community if they're kicked from your Sonoran CMS community. This also applies to bans.

### API ID Sync

This will sync all member's API IDs to the same user from your Sonoran CAD community, if they have a Discord account linked to their account it will sync that ID as well.

{% hint style="info" %}
API ID Sync to CAD will overwrite any API IDs that are set by the user in Sonoran CAD upon each sync. All API IDs that are sent to the CAD from CMS will replace what is currently there.
{% endhint %}

### Auto Join CAD

This will have all new members that join your community automatically join your Sonoran CAD community under the same user ID.

## Manual Syncing

### Full Community

Community Owner's can trigger a full community sync of CAD permissions through the **FULL SYNC** button located at the bottom of the CAD Rank Permission Selector.

<figure><img src="https://i.imgur.com/JRICaLa.png" alt=""><figcaption><p>Sonoran CMS - CAD Permission Configuration Full Sync</p></figcaption></figure>

### Individual Account

Individual member's can trigger a sync of their account with the community linked CAD in their _Account Settings_ dialog.

<figure><img src="https://i.imgur.com/mSf5VqT.png" alt=""><figcaption></figcaption></figure>
