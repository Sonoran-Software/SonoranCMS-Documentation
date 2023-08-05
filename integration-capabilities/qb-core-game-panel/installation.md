---
description: Sonoran CMS manages your QB Core server for free!
---

# Installation

## Video Tutorial

{% embed url="https://youtu.be/pkdC-qgM64E" %}

## 1. Install the CMS Core Framework

The QB Core management panel will help walk you through each step.

<figure><img src="../../.gitbook/assets/image (2) (1).png" alt="" width="375"><figcaption></figcaption></figure>

Download the CMS Core. This download will already have the config filled with your Community ID (or UUID) and API Key.

## 2. Configure the Core

<figure><img src="../../.gitbook/assets/image (3) (1).png" alt="" width="375"><figcaption></figcaption></figure>

Once installed, the `config.lua` will configure your Community ID (or UUID) and your API key. It is recommended to keep all remaining config options with their default values.

## 3. Configure your Server

In your `server.cfg` file, add the following lines to run the CMS core resource and grant permissions to the auto-updater.

```
ensure sonorancms
# permissions for SonoranCMS auto-updater (REQUIRED)
add_ace resource.sonorancms command allow
add_ace resource.sonorancms_updatehelper command allow
```

<figure><img src="../../.gitbook/assets/image (4) (1).png" alt="" width="375"><figcaption></figcaption></figure>

## 4. Configure the Panel

Select `Edit Servers` to include the IP address and port used to direct connect to your server.

<figure><img src="../../.gitbook/assets/image (5) (1).png" alt="" width="347"><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (6) (1).png" alt="" width="276"><figcaption></figcaption></figure>

## 5. Grant Permissions

By default, only community owners will have access to the QB Core management panel.

In the [Rank Manager](../teamspeak-3-role-sync/adding-ranks.md), you will need to add the associated permissions under the `Server` tab.

<figure><img src="../../.gitbook/assets/image (11) (1) (1).png" alt="" width="278"><figcaption></figcaption></figure>

## 6. Using the Game Panel

View the next guide below to start using the QB Core game panel.

{% content-ref url="using-the-game-panel/" %}
[using-the-game-panel](using-the-game-panel/)
{% endcontent-ref %}
