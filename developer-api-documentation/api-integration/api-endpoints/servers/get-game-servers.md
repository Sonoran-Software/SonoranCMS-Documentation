---
description: This endpoint allows you to retrieve your community's server configurations.
---

# Get Game Servers

{% swagger method="post" path="/servers/get_game_servers" baseUrl="https://api.sonorancms.com" summary="Get Game Servers" %}
{% swagger-description %}
Get Sonoran CMS community server configurations.
{% endswagger-description %}

{% swagger-parameter in="body" name="id" type="string" %}
Community ID
{% endswagger-parameter %}

{% swagger-parameter in="body" name="key" type="string" %}
API Key
{% endswagger-parameter %}

{% swagger-parameter in="body" name="type" type="string" %}
GET\_GAME_\__SERVERS
{% endswagger-parameter %}

{% swagger-parameter in="body" name="data" type="array" %}

{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
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
{% endswagger-response %}

{% swagger-response status="400: Bad Request" description="" %}
```javascript
INVALID REQUEST TYPE
INVALID COMMUNITY ID
```
{% endswagger-response %}
{% endswagger %}

```
{
    "id": "YOUR_COMMUNITY_ID",
    "key": "YOUR_API_KEY",
    "type": "GET_GAME_SERVERS",
    "data": []
}
```
