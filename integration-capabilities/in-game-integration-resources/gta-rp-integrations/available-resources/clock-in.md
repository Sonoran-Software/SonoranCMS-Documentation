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

### 1. Download the Resource

Click [<mark style="color:blue;">here</mark>](https://github.com/Sonoran-Software/sonoran\_clockin) to download the clock in resource.

### 2. Install the Resource

Follow the [standard resource installation guide](../gta-rp-resource-installation/) for the clock in resource.

### 3. Add your API ID

Ensure all players have added their [API ID](../../../../developer-api-documentation/api-integration/getting-started/api-id-system.md) to the CMS!

## Configuration

| Config Option          | Description                                                                                                                                                               |
| ---------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| apiKey                 | API Key found in the API Integration section of the Administrative Panel                                                                                                  |
| communityId            | Community ID found in the API Integration section of the Administrative Panel                                                                                             |
| serverId               | Server ID for specific server for this configuration according to the servers in the API Integration section of the Administrative Panel                                  |
| apiIdType              | <p>The identifier type your community uses in the CMS to enter their API IDs.<br>Valid values are: <code>license</code>, <code>steam</code>, or <code>discord.</code></p> |
| apiUrl                 | Default: `https://api.sonorancms.com` Change to `https://cmsapi.dev.sonoransoftware.com` if using development environment of Sonoran CMS                                  |
| enableCommand          | Registers the specified `command` that allows you to toggle clock in/out.                                                                                                 |
| command                | If `enableCommand` is `true`, this will be the registered command to toggle clock in/out.                                                                                 |
| useAcePermissions      | If `enableCommand` is `true`, this will enable ace permissions for the specific command, must give `command.whateverTheCommandIs`                                         |
| qbcore.use             | Enables qbcore integration                                                                                                                                                |
| qbcore.autoClockInJobs | Will automatically clock in/out the player's Sonoran CMS account with they clock in/out of a job with the name in the array of `autoClockInJobs`                          |

