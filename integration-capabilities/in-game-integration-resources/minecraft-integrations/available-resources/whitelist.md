---
description: A whitelist system that utilizes Sonoran CMS's game whitelist system.
---

# Whitelist

{% hint style="info" %}
All players of your server must have their [API ID](../../../../developer-api-documentation/api-integration/getting-started/api-id-system.md) setup and must be given a rank that has whitelist permissions for the specified server.
{% endhint %}

{% hint style="success" %}
Looking for VPS, web, or dedicated hosting? Check out our official [server hosting](../../../../other-products/server-hosting.md)!
{% endhint %}

This resource is a whitelist system that utilizes Sonoran CMS's game whitelist system by checking against that whitelist upon each player connection.

{% embed url="https://www.youtube.com/watch?v=4PAtKYQokXE" %}

## Installation

### 1. Download the Resource

{% tabs %}
{% tab title="Forge" %}
You can download a copy [here](https://github.com/Sonoran-Software/Sonoran-CMS-Minecraft-Integration/releases/tag/1.0.0).

Ensure that you download the one that has `forge` in the name.
{% endtab %}

{% tab title="Fabric" %}
You can download a copy [here](https://github.com/Sonoran-Software/Sonoran-CMS-Minecraft-Integration/releases/tag/1.0.0).

Ensure that you download the one that has `fabric` in the name.
{% endtab %}

{% tab title="Bukkit/Spigot/Paper" %}
You can download a copy [here](https://github.com/Sonoran-Software/Sonoran-CMS-Minecraft-Integration/releases/tag/1.0.0).

Ensure that you download the one that has `plugin` in the name.
{% endtab %}
{% endtabs %}



### 2. Install the Resource

Follow the standard resource installation guide for the whitelist resource, available [here](../minecraft-resource-installation.md).1

### 3. Setup Whitelist Permissions

Navigate to the Department Manager within the Administrative Panel.

Administrative Panel > Customization > Department Manager

![Sonoran CMS Department Manager](https://i.imgur.com/1x7EHpI.png)

For users in your Sonoran CMS community to be accepted through the whitelist, they'll need to be granted permission for the whitelist through rank permissions. You will need to grant each rank the permission of **Allow Whitelist** that you want to be allowed through the whitelist. You will want to grant each rank with the permission of **Block Whitelist** if you want them to be blocked from passing through the whitelist.

{% hint style="warning" %}
**Block Whitelist** will ALWAYS overrule **Allow Whitelist**\
\
If a user is granted both **Block Whitelist** and **Allow Whitelist** through various ranks they will be blocked from the whitelist. Block will always overrule allow.
{% endhint %}

![Sonoran CMS - Department Manager Server Permissions](https://i.imgur.com/yBjp7ZA.png)

### 4. Add your API ID

Ensure all players have added their [API ID](../../../../developer-api-documentation/api-integration/getting-started/api-id-system.md) to the CMS!

## Configuration

{% tabs %}
{% tab title="Forge" %}
The config file is called `cmswhitelist-common.toml` in the config folder of your Minecraft server folder.

```
[SonoranCMS]
	#This is your SonoranCMS Community ID.
	"Community ID" = ""
	#This is your SonoranCMS API key.
	"Community API Key" = ""
	#Which identifier to use, either UUID or Username. UUID is preferred.
	"Identifier Type" = "UUID"
	#The server ID found in SonoranCMS that this whitelist should check against.
	"Server ID" = 1
```

| Value Name        | Description                                                                                    | Default                |
| ----------------- | ---------------------------------------------------------------------------------------------- | ---------------------- |
| Server ID         | This is the game server ID set in the CMS management panel.                                    | `1`                    |
| Community ID      | This is the community ID that is found in the API Integration section of the management panel. | `""`                   |
| Community API Key | This is the API key listed in the API Integration section of the management panel.             | `""`                   |
| Identifier Type   | This controls whether a player's UUID or username is used for identifying.                     | `"UUID"` (Recommended) |
{% endtab %}

{% tab title="Fabric" %}
The config file is called `sonorancms.json` in the config folder of your Minecraft server folder.

```
{
  "CMS_Settings": {
    "Community_ID": "",
    "Community_API_Key": "",
    "Identifier": "UUID",
    "Server_ID": 1
  }
}
```

| Value Name          | Description                                                                                    | Default                |
| ------------------- | ---------------------------------------------------------------------------------------------- | ---------------------- |
| Server\_ID          | This is the game server ID set in the CMS management panel.                                    | `1`                    |
| Community\_ID       | This is the community ID that is found in the API Integration section of the management panel. | `""`                   |
| `Community_API_Key` | This is the API key listed in the API Integration section of the management panel.             | `""`                   |
| Identifier          | This controls whether a player's UUID or username is used for identifying.                     | `"UUID"` (Recommended) |
{% endtab %}

{% tab title="Bukkit/Spigot/Paper" %}
The config file is called `config.yml` in the `plugins/SonoranCMSWhitelist` folder of your Minecraft server folder.

```
CommunityID: ''
CommunityAPIKey: ''
Identifier: UUID
ServerID: 1
```

| Value Name      | Description                                                                                    | Default              |
| --------------- | ---------------------------------------------------------------------------------------------- | -------------------- |
| ServerID        | This is the game server ID set in the CMS management panel.                                    | `1`                  |
| CommunityID     | This is the community ID that is found in the API Integration section of the management panel. | `''`                 |
| CommunityAPIKey | This is the API key listed in the API Integration section of the management panel.             | `''`                 |
| Identifier      | This controls whether a player's UUID or username is used for identifying.                     | `UUID` (Recommended) |
{% endtab %}
{% endtabs %}
