---
description: A in-game way to utilize Sonoran CMS's clock in/out system.
---

# Clock In

{% hint style="success" %}
Looking for VPS, web, or dedicated hosting? Check out our official [server hosting](../../../../../other-products/server-hosting.md)!
{% endhint %}

This module is a in-game way of automatically\* clocking in/out of Sonoran CMS's system.

## Installation / Configuration

{% hint style="info" %}
With core version `v1.4.0` the Clock In resource was converted to a core module and no longer requires manual installation just configuration.
{% endhint %}

### 1. Configure Clock In Module

Locate the clockin module within your `[sonorancms]/sonorancms/server/modules` and open the `clockin_config.json` file



<figure><img src="https://i.imgur.com/sR9g6J3.png" alt=""><figcaption></figcaption></figure>

## Configuration

| Config Option          | Description                                                                                                                                      |
| ---------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------ |
| enableCommand          | Registers the specified `command` that allows you to toggle clock in/out.                                                                        |
| command                | If `enableCommand` is `true`, this will be the registered command to toggle clock in/out.                                                        |
| useAcePermissions      | If `enableCommand` is `true`, this will enable ace permissions for the specific command, must give `command.whateverTheCommandIs`                |
| qbcore.use             | Enables qbcore integration                                                                                                                       |
| qbcore.autoClockInJobs | Will automatically clock in/out the player's Sonoran CMS account with they clock in/out of a job with the name in the array of `autoClockInJobs` |

### 2. Add your API ID

Ensure all players have added their [API ID](../../../../../developer-api-documentation/api-integration/getting-started/api-id-system.md) to the CMS!
