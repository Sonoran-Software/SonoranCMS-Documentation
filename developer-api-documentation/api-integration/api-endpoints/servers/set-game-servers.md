---
description: This endpoint allows you to set your community's server configurations.
---

# Set Game Servers

## Set Game Servers

<mark style="color:green;">`POST`</mark> `https://api.sonorancms.com/servers/set_game_servers`

Set Sonoran CMS community server configurations.

#### Request Body

| Name | Type   | Description                    |
| ---- | ------ | ------------------------------ |
| id   | string | Community ID                   |
| key  | string | API Key                        |
| type | string | GET\_GAM&#x45;_\__&#x53;ERVERS |
| data | array  |                                |

{% tabs %}
{% tab title="200: OK " %}
```json
{
    "success": true,
    "data": [
        {
            "id": 1,
            "name": "Server 1",
            "description": "Default server description",
            "ip": "0.0.0.0"
            "port": "00000"
        }
    ]
}
```
{% endtab %}

{% tab title="400: Bad Request " %}
```javascript
INVALID REQUEST TYPE
INVALID COMMUNITY ID
```
{% endtab %}
{% endtabs %}

```json
{
    "id": "YOUR_COMMUNITY_ID",
    "key": "YOUR_API_KEY",
    "type": "SET_GAME_SERVERS",
    "data": [
        {
            "id": 1, // Optional - only supply if needing to update a server
            "name": "Server 1",
            "description": "This is server 1",
            "ip": "",
            "port": ""
        }
    ]
}
```
