---
description: This guide covers the installation process for a general integration resource.
---

# GTA RP Resource Installation

## Installing a Resource

This uses the whitelist resource as an example.

### 1. Download

Download the resource from its repository. These are found under its resource page, like here for the whitelist resource.

![](../../../../.gitbook/assets/opera\_M5S4BnTZL9.png)

### 2. Extract

{% hint style="warning" %}
All plugins for FiveM require the [Core](../available-resources/core.md) to start.
{% endhint %}

Extract the resource to your server resources folder in the folder named [sonorancms] that comes with the download of Core so it sits alongside sonorancms & sonorancms_updatehelper.

![](../../../../.gitbook/assets/%5Bsonorancms%5D%20folder.png)

### 3. Add resource to server.cfg

Add `ensure sonorancms` to your server.cfg and restart your server!

{% hint style="danger" %}
It is very important that the sonorancms_updatehelper resource is not started manually. Doing so may cause a server crash if updates are available due to a race condition.
DO NOT start the whole [sonorancms] folder as that will also start the sonorancms_updatehelper which might cause crashing if it is started manually. Example of not what to do ensure [sonorancms]
{% endhint %}
