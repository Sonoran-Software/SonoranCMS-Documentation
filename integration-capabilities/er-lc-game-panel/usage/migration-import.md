---
description: >-
  Migrating to Sonoran CMS from another ER:LC management panel provider? Import
  your data by using the import wizard!
---

# Migration Import

## Migrate from Melonly

Easily import your Melonly player logs to convert them to CMS player records!

### 1. Create a Melonly API Key

<details>

<summary>1. Create a Melonly API Key</summary>

On the Melonly dashboard select **Settings** > **Panel** > **Server API Tokens** > **Create Token**

Create and copy the API token to be used with Sonoran CMS.

<figure><img src="../../../.gitbook/assets/image (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (3) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

</details>

### 2. Import into CMS

<details>

<summary>2. Import into CMS</summary>

Select **Import** on the side panel > **Melonly** > paste your Melonly API Token > **Initiate Import**

Once started, the CMS will begin importing your Melonly player logs, including any custom log types. After a few minutes, your Melonly logs will begin to display in the activity feed and&#x20;

<div><figure><img src="../../../.gitbook/assets/image (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure> <figure><img src="../../../.gitbook/assets/image (5) (1).png" alt=""><figcaption><p>CMS: Import Melonly Logs</p></figcaption></figure></div>

</details>

### 3. Custom Log Types

<details>

<summary>3. Custom Log Types</summary>

Both Melonly and Sonoran CMS allow for the creation of custom player log/record types. Because Melonly does not expose the record type labels in their API these logs will be imported as `Unknown Custom Log Type`.

You can [rename these custom log types from Melonly properly in the Moderation panel](moderation.md#custom-record-types).

<figure><img src="../../../.gitbook/assets/image (8).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (7).png" alt=""><figcaption></figcaption></figure>

</details>

