---
description: This endpoint allows you to set your community's server configurations.
---

# Set Game Servers

{% hint style="warning" %}
API endpoint requires the **Plus** version of Sonoran CMS or higher.\
For more information, see our [pricing ](../../../../pricing/pricing-faq/)page.
{% endhint %}

{% swagger method="post" path="general/set_game_servers" baseUrl="https://api.sonorancms.com" summary="Set Game Servers" %}
{% swagger-description %}
Set Sonoran CMS community server configurations.
{% endswagger-description %}

{% swagger-parameter in="body" name="id" type="string" %}
Community ID
{% endswagger-parameter %}

{% swagger-parameter in="body" name="key" type="string" %}
API Key
{% endswagger-parameter %}

{% swagger-parameter in="body" name="type" type="string" %}
GET_GAME

___

SERVERS
{% endswagger-parameter %}

{% swagger-parameter in="body" name="data" type="array" %}

{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
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
{% endswagger-response %}

{% swagger-response status="400: Bad Request" description="" %}
```javascript
INVALID REQUEST TYPE
INVALID COMMUNITY ID
```
{% endswagger-response %}
{% endswagger %}

```json
{
    "id": "YOUR_COMMUNITY_ID",
    "key": "YOUR_API_KEY",
    "type": "SET_GAME_SERVERS",
    "data": [
        {
            "name": "Server 1",
            "description": "This is server 1",
            "ip": "",
            "port": ""
        }
    ]
}
```
