---
description: >-
  Advanced alternate account detection keeps your community safe from bad actors
  and previously banned users.
---

# Account Flags

<figure><img src="../../../.gitbook/assets/image (38).png" alt=""><figcaption><p>Sonoran CMS - Alt Detection</p></figcaption></figure>

{% hint style="danger" %}
**Alternate Account Detection & Account Flags are only enabled with a Pro Subscription!**

Learn more about our [paid plans](../../../pricing/pricing-faq/create-and-manage-a-subscription.md).
{% endhint %}

## What is Alternate Account Detection?

When bad actors are banned from your community, it's important to ensure they don't come back under a different account name, alias, etc.

Sonoran CMS offers advanced tools to detect ban evasion, easily detecting duplicate accounts on member applications, forums posts, user profiles, game session joins, etc.

## Account Flags

### What is an Account Flag?

Account flags are raised when a user has a "clash" with another account in your CMS.

Ex: "Bob123" logs in with the same IP address as "Alice456" -> this results in a `Duplicate IP` flag

### What Flag Types are There?

* Duplicate IP Address
* Duplicate Browser IDs
* Duplicate PC Hardware IDs
* Duplicate Mobile Device IDs
* Duplicate Linked Discord IDs
* Duplicate CFX License (in-game)
* Duplicate Steam ID (in-game)
* Duplicate Xbox Live ID (in-game)
* VPN Usage Detection

## Flag Management

### How Do I View Flags?

#### Via Security Center

In the `Administrator Panel` the `Security Center` tab highlights all active flags that need to be reviewed.

<figure><img src="../../../.gitbook/assets/image (32).png" alt=""><figcaption></figcaption></figure>

#### Via Account Avatar

Anywhere an account avatar is visible will also show a user's account flags.

* Forms and Applications
* Forums Posts
* User Accounts Panel
* User Profile and Bio

<figure><img src="../../../.gitbook/assets/image (36).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (34).png" alt=""><figcaption></figcaption></figure>

Select the highlighted flag on a user's account avatar to automatically redirect to the security center with their specific flags raised.

### Viewing and Dismissing Flags

Select a flag in the account flags center to view more details. This will show what type of flag it is and what accounts it has been raised on.

#### Investigating a Flag

Investigate the flag type and the users involved. If one of the users was a previously banned user, and the other is a new member - it's possible it's the same person trying to evade a community ban.

This example shows user `8` (SonoranBrian) linked a Discord account that a banned user `14` (Bob123) previously used.

<figure><img src="../../../.gitbook/assets/image (37).png" alt=""><figcaption></figcaption></figure>

#### Flag Icons

When viewing a flag, the user accounts mentioned may also display one of the following icons:

* 🚫 - This user is banned in your community
* 🕒 - This user is pending in your community (no ranks yet, new applicant)
* ❓ - This user has not yet joined your community but may be an alternate account of someone who is already in your community

#### Dismissing a Flag

Sometimes two different users may be harmlessly sharing the same physical device, IP address, etc.

Ex: Two users sharing the same WiFi network, but both are in your community.

After investigating why these two users have a shared identifier, and that it's harmless, you can "dismiss" the flag. Once dismissed, the flag with the involved accounts will no longer appear unless an additional account matches up in the future.

## Flag Permissions

In order to view and manage these account flags, users will need the `Security Center Manage Flags` permissions under the `System` tab in the [rank manager](../../user-management/creating-departments.md).
