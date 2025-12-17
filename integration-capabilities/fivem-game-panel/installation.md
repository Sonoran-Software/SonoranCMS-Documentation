---
description: Sonoran CMS manages your QB Core server for free!
---

# Installation

## Video Tutorial

{% embed url="https://youtu.be/pkdC-qgM64E" %}



<figure><img src="../../.gitbook/assets/Screenshot (480).png" alt=""><figcaption><p>Sonoran CMS - Integrations</p></figcaption></figure>

## 1. Install the CMS Core Framework

The QB Core management panel will help walk you through each step.

<figure><img src="../../.gitbook/assets/Screenshot (481).png" alt=""><figcaption></figcaption></figure>

Download the CMS Core. This download will already have the config filled with your Community ID (or UUID) and API Key.

## 2. Configure the Core

<figure><img src="../../.gitbook/assets/Screenshot (482).png" alt=""><figcaption></figcaption></figure>

Once installed, the `config.lua` will configure your Community ID (or UUID) and your API key. It is recommended to keep all remaining config options with their default values.

## 3. Configure your Server

In your `server.cfg` file, add the following lines to run the CMS core resource and grant permissions to the auto-updater.

```
# file system permissions (if using QB-Core)
add_filesystem_permission sonorancms write qb-core

# file system permissions (if using QBox)
add_filesystem_permission sonorancms write qbx_core
add_filesystem_permission sonorancms write ox_inventory

exec @sonorancms/sonorancms.cfg
```

<div align="center" data-full-width="false"><figure><img src="../../.gitbook/assets/Screenshot (483).png" alt=""><figcaption></figcaption></figure></div>

## 4. Configure your Server (Required for QB-Core and QBox)

Due to recent changes to FiveM there is now security limitations to the file system which the game panel uses to update Items, Jobs, Gangs, etc. This requires the `add_filesystem_permission` line(s) to be added to the `server.cfg` shown above, as well as the author of the resources to be updated. You can find out more information on why this is required [here](https://docs.fivem.net/docs/developers/sandbox/#file-system-permissions).

**QB-Core Specific**

* Update `qb-core/fxmanifest.lua` author line to the following:
  * `author ''`

**QBox Specific**

* Update `ox_inventory/fxmanifest.lua` author line to the following:
  * `author ''`

_Note: We're working on making this not a requirement in the future but need to work with the respective resource developers to get it updated._

## 5. Configure the Panel

Select `Edit Servers` to include the IP address and port used to direct connect to your server.

<figure><img src="../../.gitbook/assets/Screenshot (487).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/Screenshot (485).png" alt=""><figcaption></figcaption></figure>



## 6. Grant Permissions

By default, only community owners will have access to the QB Core management panel.

In the [Rank Manager](../teamspeak-3-role-sync/adding-ranks.md), you will need to add the associated permissions under the `Server` tab.

<figure><img src="../../.gitbook/assets/Screenshot (488).png" alt=""><figcaption></figcaption></figure>

## 7. Using the Game Panel

View the next guide below to start using the QB Core game panel.

{% content-ref url="qbcore-and-qbox-panel/" %}
[qbcore-and-qbox-panel](qbcore-and-qbox-panel/)
{% endcontent-ref %}
