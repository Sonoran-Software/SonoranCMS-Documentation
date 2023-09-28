---
description: This endpoint allows you to check your Sonoran CMS subscription version.
---

# Get Sub Version

{% hint style="warning" %}
API endpoint requires the **FREE** version of Sonoran CMS or higher.\
For more information, see our [pricing ](../../../../pricing/pricing-faq/)page.
{% endhint %}

{% swagger method="post" path="/general/get_sub_version" baseUrl="https://api.sonorancms.com" summary="Get Sub Version" %}
{% swagger-description %}
Get Sonoran CMS subscription version of a community.
{% endswagger-description %}

{% swagger-parameter in="body" name="id" type="string" required="true" %}
Community ID
{% endswagger-parameter %}

{% swagger-parameter in="body" name="key" type="string" required="true" %}
API Key
{% endswagger-parameter %}

{% swagger-parameter in="body" required="true" name="type" type="string" %}
GET\_SUB_\__VERSION
{% endswagger-parameter %}

{% swagger-parameter in="body" required="true" name="data" type="array" %}
Array of request objects
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```javascript
0 - FREE
1 - STARTER
2 - STANDARD
3 - PLUS
4 - PRO
5 - SONORANONE
```
{% endswagger-response %}

{% swagger-response status="400: Bad Request" description="The following 400 errors may be sent in response:" %}
```javascript
INVALID API KEY
INVALID COMMUNITY ID
```
{% endswagger-response %}
{% endswagger %}

```
{
    "id": "YOUR_COMMUNITY_ID",
    "key": "YOUR_API_KEY",
    "type": "GET_SUB_VERSION",
    "data": []
}
```
