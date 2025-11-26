---
description: Easily set the weather and time in your server, directly from CMS!
---

# Environment

<figure><img src="/broken/files/EGthOA3Z2ZzQPyjupM75" alt=""><figcaption><p>Sonoran CMS - VMenu Game Panel Promotional Image</p></figcaption></figure>

## Manage Weather

Here you can set the current weather on your server. Open the dropdown menu and choose from 15 different weather options! You can also toggle `Freeze` and `Blackout` on the side.

`Freeze` forces the weather to stay as what you set it to, if toggled, it will not change on its own.

`Blackout` simulates a power outage, and all buildings will show as if they don't have electricity.

<figure><img src="../../../.gitbook/assets/CMS_VMenuEnvWeather.png" alt="" width="375"><figcaption><p>Sonoran CMS - VMenu Game Panel - Weather</p></figcaption></figure>

<figure><img src="../../../.gitbook/assets/CMS_VMenuEnvWeatherOptions.png" alt="" width="275"><figcaption><p>Sonoran CMS - VMenu Game Panel - Weather Options</p></figcaption></figure>

## Manage Time

You can also set the time to any time of day using the time selector. You can also toggle `Freeze` which locks the time to whatever you've set it to.

<figure><img src="../../../.gitbook/assets/CMS_VMenuEnvTime.png" alt="" width="375"><figcaption><p>Sonoran CMS - VMenu Game Panel - Time</p></figcaption></figure>

## Weather Flickering Issue

Sometimes, having CMS installed can cause an issue where the weather and time in the server seem to rapidly "flicker". This occurs when another resource is also trying to manage weather.

If you are encountering this issue and would like to disable CMS's weather management, then please set `Config.EnableWeatherSync` to `false` in the resource's `config.lua`.
