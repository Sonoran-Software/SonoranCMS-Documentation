---
description: This endpoint allows you to verify the whitelist of a community account.
---

# Verify Whitelist

{% hint style="warning" %}
API endpoint requires the **Plus** version of Sonoran CMS or higher.\
For more information, see our [pricing ](../../../../pricing/pricing-faq/)page.
{% endhint %}

{% swagger method="post" path="/servers/verify_whitelist" baseUrl="https://api.sonorancms.com" summary="Verify Whitelist" %}
{% swagger-description %}
Verifies the whitelist of a community account found given the accId or API ID.
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

{% swagger-response status="200: OK" description="The following text responses may be sent in response:" %}
```javascript
{{Sonoran CMS Account Username}}
BYPASSED WHITELIST - {{Sonoran CMS Account Username}}
```
{% endswagger-response %}

{% swagger-response status="400: Bad Request" description="The following text responses may be sent in response:" %}
```javascript
INVALID REQUEST TYPE
INVALID COMMUNITY ID
```
{% endswagger-response %}

{% swagger-response status="404: Not Found" description="The following text responses may be sent in response:" %}
```javascript
NOT ALLOWED ON WHITELIST
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
            "apiId": "SOME_API_ID", // Optional - must have one (apiId or accId)
            "accId": "SOMEACCID", // Optional - must have one (apiId or accId)
            "serverId": 2 // Optional - will check specific server whitelist if specified
        }
    ]
}
```
