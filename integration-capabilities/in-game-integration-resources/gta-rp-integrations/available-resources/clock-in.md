---
description: A in-game way to utilize Sonoran CMS's clock in/out system.
---

# Clock In

{% hint style="warning" %}
This resource utilizes API endpoints that require the **plus** version of Sonoran CMS or higher. For more information, view our [pricing ](broken-reference)page.
{% endhint %}

{% hint style="success" %}
Looking for VPS, web, or dedicated hosting? Check out our official [server hosting](../../../../other-products/server-hosting.md)!
{% endhint %}

This resource is a in-game way of automatically\* clocking in/out of Sonoran CMS's system.

## Installation

### 1. Download the Core Resource

This resource requires the [CMS core](core.md) for push event handling and API key configuration.

### 2.Download the Resource

Click [<mark style="color:blue;">here</mark>](https://github.com/Sonoran-Software/sonoran\_clockin) to download the clock in resource.

### 3. Install the Resource

Follow the [standard resource installation guide](../gta-rp-resource-installation/) for the clock in resource.

### 4. Add your API ID

Ensure all players have added their [API ID](../../../../developer-api-documentation/api-integration/getting-started/api-id-system.md) to the CMS!

## Configuration

| Config Option          | Description                                                                                                                                      |
| ---------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------ |
| enableCommand          | Registers the specified `command` that allows you to toggle clock in/out.                                                                        |
| command                | If `enableCommand` is `true`, this will be the registered command to toggle clock in/out.                                                        |
| useAcePermissions      | If `enableCommand` is `true`, this will enable ace permissions for the specific command, must give `command.whateverTheCommandIs`                |
| qbcore.use             | Enables qbcore integration                                                                                                                       |
| qbcore.autoClockInJobs | Will automatically clock in/out the player's Sonoran CMS account with they clock in/out of a job with the name in the array of `autoClockInJobs` |

