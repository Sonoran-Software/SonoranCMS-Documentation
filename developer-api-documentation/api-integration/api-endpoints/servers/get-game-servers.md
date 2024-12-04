---
description: This endpoint allows you to retrieve your community's server configurations.
---

# Get Game Servers

## Get Game Servers

<mark style="color:green;">`POST`</mark> `https://api.sonorancms.com/servers/get_game_servers`

Get Sonoran CMS community server configurations.

#### Request Body

| Name | Type   | Description                    |
| ---- | ------ | ------------------------------ |
| id   | string | Community ID                   |
| key  | string | API Key                        |
| type | string | GET\_GAM&#x45;_\__&#x53;ERVERS |
| data | array  |                                |

{% tabs %}
{% tab title="200: OK " %}
```javascript
{
    "servers": [
        {
            "id": 1,
            "name": "Server 1",
            "description": "Default server description"
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

```
{
    "id": "YOUR_COMMUNITY_ID",
    "key": "YOUR_API_KEY",
    "type": "GET_GAME_SERVERS",
    "data": []
}
```
