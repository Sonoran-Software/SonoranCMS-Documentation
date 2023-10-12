---
description: The CMS core maintains common utility functions and push event handling.
---

# Core

{% hint style="success" %}
Looking for VPS, web, or dedicated hosting? Check out our official [server hosting](../../../../../other-products/server-hosting.md)!
{% endhint %}

This resource does nothing on its own and is simply a dependency for other resources.

## Installation

### 1. Download the Resource

Click [<mark style="color:blue;">here</mark>](https://github.com/Sonoran-Software/sonorancms\_core/releases) to download the core resource.

### 2. Install the Resource

Follow the [standard resource installation guide](../../gta-rp-resource-installation/) for the core resource.

Extracting the folder \[sonorancms] into the resources folder.

### 3. Configure and Rename

Open `sonorancms\config.CHANGEME.lua`, update the values, then save it as `config.lua`.

Default configuration is below:

#### Configuration Details

| Config Option      | Description                                                                                                                                                                       |
| ------------------ | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| APIKey             | API Key found in the API Integration section of the Administrative Panel                                                                                                          |
| CommID             | Community ID found in the API Integration section of the Administrative Panel                                                                                                     |
| allowAutoUpdate    | When enabled, the resource will update itself. When disabled, it will simply show an update notification every 2 hours.                                                           |
| debug\_mode        | <p>When set to <code>true</code>, useful debugging information it outputted to the console.<br>Keep disabled in production due to console spam.</p>                               |
| apiUrl             | Default: `https://api.sonorancms.com/`                                                                                                                                            |
| apiIdType          | Type of api ID the core script should be searching for: `discord`, `steam`, `license`, etc.                                                                                       |
| serverId           | Default: `1` - ID of the Sonoran CMS server that this core resource should be tied to.                                                                                            |
| framework          | `none`, `qb-core`, or `esx`                                                                                                                                                       |
| MaxInventorySlots  | If using framework: `qb-core` you can specify the max inventory slots your inventory resource supports, this is for inventory management via the Game Panel's within Sonoran CMS. |
| restartWithPlayers | When set to `true`, it will auto-update the resource and restart it even if players are present on the server.                                                                    |

### 4. Server Config

Add the following to your `server.cfg`

{% hint style="danger" %}
It is very important that the sonorancms\_updatehelper resource is not started manually. Doing so may cause a server crash if updates are available due to a race condition. DO NOT start the whole \[sonorancms] folder as that will also start the sonorancms\_updatehelper which might cause crashing if it is started manually. Example of not what to do ensure \[sonorancms]
{% endhint %}

```javascript
ensure sonorancms

# permissions for SonoranCMS auto-updater (REQUIRED)
add_ace resource.sonorancms command allow
add_ace resource.sonorancms_updatehelper command allow
```

## Updates

Sonoran CMS's core will automatically update with the latest features, fixes, and changes!

## Troubleshooting

### Server Crashes

1\. Check to make sure `sonorancms_updatehelper` is not being started in your server.cfg.

{% hint style="danger" %}
It is very important that the `sonorancms_updatehelper` resource is not started manually. Doing so may cause a server crash if updates are available due to a race condition.
{% endhint %}
