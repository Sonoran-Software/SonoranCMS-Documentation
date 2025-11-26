---
description: Easily grant ACE Permissions to users directly from CMS.
---

# Aces & Principals

<figure><img src="/broken/files/jILuwFyjFX0VdFnCOqGw" alt=""><figcaption><p>Sonoran CMS - VMenu Game Panel Promotional Image</p></figcaption></figure>

## Setup

Ensure you have the following in your `server.cfg` (if you don't permissions won't be able to be granted)

```
add_ace resource.sonorancms command allow
```

## Mapping Ranks to ACE Principal Identifiers

You can select the ranks you would like and input the principal identifier you would like to grant them. This makes it easy to grant users in-game permissions en masse.

<figure><img src="https://i.imgur.com/j5XTpYT.png" alt=""><figcaption><p>Sonoran CMS -VMenu Game Panel - Aces &#x26; Principals</p></figcaption></figure>

You can further customize the permissions each Principal group receives in your `server.cfg`, make sure to follow the conventions outlined in [this guide](https://forum.cfx.re/t/basic-aces-principals-overview-guide/90917).

Additionally, ensure all players have added their [API ID](../../../developer-api-documentation/api-integration/getting-started/api-id-system.md) to the CMS.

For more details, read our documentation on the "Ace Permission Sync" module for CMS Core [here](../../in-game-integration-resources/core/core-submodules/ace-permission-sync.md).
