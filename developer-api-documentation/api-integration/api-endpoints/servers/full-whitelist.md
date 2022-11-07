---
description: >-
  This endpoint allows you to get the full whitelist list for the specified
  server.
---

# Full Whitelist

{% hint style="warning" %}
API endpoint requires the **Plus** version of Sonoran CMS or higher.\
For more information, see our [pricing ](../../../../pricing/pricing-faq/)page.
{% endhint %}

{% swagger method="post" path="/servers/full_whitelist" baseUrl="https://api.sonorancms.com" summary="Full Whitelist" %}
{% swagger-description %}
Gets the full list for everyone whitelisted for the specified server.
{% endswagger-description %}

{% swagger-parameter in="body" name="id" type="string" %}
Community ID
{% endswagger-parameter %}

{% swagger-parameter in="body" name="key" type="string" %}
API Key
{% endswagger-parameter %}

{% swagger-parameter in="body" name="type" type="string" %}
FULL_WHITELIST
{% endswagger-parameter %}

{% swagger-parameter in="body" name="data" type="array" %}

{% endswagger-parameter %}

{% swagger-response status="200: OK" description="The following text responses may be sent in response:" %}
```json
[
    {
        "name": "John Doe",
        "apiIds: [...],
    }
]
```
{% endswagger-response %}

{% swagger-response status="400: Bad Request" description="The following text responses may be sent in response:" %}
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
    "type": "VERIFY_WHITELIST",
    "data": [
        {
            "serverId": 1,
        }
    ]
}
```
