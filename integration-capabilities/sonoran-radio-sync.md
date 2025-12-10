---
description: >-
  Easily manage Sonoran Radio permissions from Sonoran CMS ranks! Learn more
  below.
---

# Sonoran Radio Sync

Sonoran CMS allows you to easily manage your community's Sonoran Radio permissions based on their Sonoran CMS rank automatically!

{% hint style="warning" %}
This sync requires Sonoran Radio Standalone.

If you are using the Sonoran Radio TeamSpeak, view our [TeamSpeak integration](teamspeak-3-role-sync/).
{% endhint %}

### 1. Add New Radio Integration

Click the _Sonoran Radio_ icon or click the plus button to sync another Radio to you community

<figure><img src="../.gitbook/assets/Screenshot (463).png" alt=""><figcaption><p>Sonoran CMS - Radio Integration Setup List Area</p></figcaption></figure>

### 1. Enter Credentials

Enter your Sonoran Radio community's ID & API Key.

Your Community ID and API Key are located in Sonoran Radio's `Administration` panel.\
Enter these into your Sonoran CMS as shown below.

<figure><img src="../.gitbook/assets/Screenshot (462).png" alt=""><figcaption><p>Sonoran Radio - Administration Panel</p></figcaption></figure>

<figure><img src="../.gitbook/assets/Screenshot (464).png" alt=""><figcaption><p>Sonoran CMS - Sonoran Radio Integration Credential Inputs</p></figcaption></figure>

### 2. Configure Sync Settings

Check the sync options that best fit your community's needs, explanation of each sync feature can be found [below](sonoran-cad-sync.md#feature-overview).

<figure><img src="../.gitbook/assets/Screenshot (465).png" alt=""><figcaption></figcaption></figure>

### 3. Map CAD Permissions to Ranks

Select a CMS rank and toggle the desired Radio permissions below.

When you're done setting up Radio sync and configuring permission mappings, simply close out of the window by clicking the red X button and it will automatically save your credentials, settings, and trigger a mass sync of all permissions.

{% hint style="warning" %}
Permission syncs from Sonoran CMS will set the user's permissions explicitly to what is mapped in the CMS and will wipe any non-enabled permissions.
{% endhint %}

<figure><img src="../.gitbook/assets/Screenshot (466).png" alt=""><figcaption><p>Sonoran CMS - Sonoran CAD Integration Permission Mapping</p></figcaption></figure>

## Feature Overview

### Multi-Setup Sync

Sync multiple Sonoran Radio communities with your single Sonoran CMS community. This will sync all of the below features with each community you have setup.

### Kick Sync

This will trigger an action to kick the same user from your Sonoran Radio community if they're kicked from your Sonoran CMS community.

### Ranks that Auto Join Radio

This allows specific ranked members who join your community to be automatically added to your Sonoran Radio community under the same account.

### Name Sync

This will automatically set a user's radio display name to match their CMS display name. This is updated on:

* CMS community name change
* User account update/save
* Radio integration configuration change
