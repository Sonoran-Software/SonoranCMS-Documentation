---
description: Sync your Discord roles with SonoranCMS permissions!
---

# Permissions Synchronization

{% embed url="https://www.youtube.com/watch?v=mlH4TlybT_4" %}

## Getting Started

{% hint style="warning" %}
By default, **only Administrators of the Discord guild can access the commands** below. These can be changed in the Settings menu of the server.
{% endhint %}

### 1. Discord SSO Linking

Users must link their Discord to their Sonoran account. This will also automatically add their Discord [API ID](../../../developer-api-documentation/api-integration/getting-started/api-id-system.md).

#### Enable Discord Sync

* In the Administration panel select `Advanced` -> `API Integration`
* Toggle the `Discord Bot Integration` box

<figure><img src="../../../.gitbook/assets/Screen Shot 2023-01-08 at 12.10.12 PM.png" alt=""><figcaption><p>Sonoran CMS - Enable Discord Bot</p></figcaption></figure>

#### Link your Discord Account

Once enabled in the CMS, users who do not yet have their Discord account linked with their Sonoran account will see the following banner:

<figure><img src="../../../.gitbook/assets/Screen Shot 2023-01-08 at 12.04.00 PM.png" alt=""><figcaption><p>Sonoran CMS - Link Your Discord Account</p></figcaption></figure>



### 2. Role Mapping

The command `/rolemap` can now be used.

The following image is when a CMS mode is selected.

<figure><img src="../../../.gitbook/assets/Screenshot_5.png" alt=""><figcaption><p>Options when set to To CMS or Bi Directional CMS</p></figcaption></figure>

Select a department, rank you wish to modify, and the role you wish to apply to the rank.

<figure><img src="../../../.gitbook/assets/Screenshot_6.png" alt=""><figcaption></figcaption></figure>

The "Set Department-wide Role" button will automatically assign the Department (in this example, Community Leadership) to anyone with the role you select.

<figure><img src="../../../.gitbook/assets/Screenshot_7.png" alt=""><figcaption><p>Click "Select Roles"</p></figcaption></figure>

<figure><img src="../../../.gitbook/assets/Screenshot_12.png" alt=""><figcaption><p>Use the left and right arrows to page if you have more than 25 roles.</p></figcaption></figure>

<figure><img src="../../../.gitbook/assets/Screenshot_8.png" alt=""><figcaption></figcaption></figure>

The "Staff Role" will get the rank "Director" in the CMS.

This is only an example! At any time, you can change the dropdowns to select another Department or Rank.

## Role Syncing

{% hint style="info" %}
Unlike the CAD sync mode, users will not use the `/linkme` command - this is handled within the Sonoran Account SSO.
{% endhint %}

After setting up the above, the command `/syncroles` will set up everyone's permissions.
