---
description: This endpoint allows you to ban an account from your community.
---

# Ban Account

{% swagger method="post" path="/general/ban_account" baseUrl="https://api.sonorancms.com" summary="Ban Account" %}
{% swagger-description %}
Clock in/out a community account found by API ID or account ID.
{% endswagger-description %}

{% swagger-parameter in="body" name="id" type="string" required="true" %}
Community ID
{% endswagger-parameter %}

{% swagger-parameter in="body" name="key" type="string" required="true" %}
API Key
{% endswagger-parameter %}

{% swagger-parameter in="body" required="true" name="type" type="string" %}
CLOCK\_IN_\__OUT
{% endswagger-parameter %}

{% swagger-parameter in="body" required="true" name="data" type="array" %}
Array of request objects
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="The following 200 response texts may be sent in response:" %}
```javascript
CLOCKED IN
FORCE CLOCKED IN
CLOCKED OUT
```
{% endswagger-response %}

{% swagger-response status="400: Bad Request" description="The following 400 errors may be sent in response:" %}
```javascript
INVALID API KEY
INVALID COMMUNITY ID
API ID NOT LINKED TO AN ACCOUNT IN THIS COMMUNITY
```
{% endswagger-response %}

{% swagger-response status="404: Not Found" description="The following 404 errors may be sent in response:" %}
```javascript
API ID NOT LINKED TO AN ACCOUNT IN THIS COMMUNITY
```
{% endswagger-response %}
{% endswagger %}

```
{
    "id": "YOUR_COMMUNITY_ID",
    "key": "YOUR_API_KEY",
    "type": "BAN_ACCOUNT",
    "data": [
        {
            "apiId": "SOME_API_ID", // Optional - must have one (apiId or accId)
            "accId": "SOMEACCID", // Optional - must have one (apiId or accId)
        }
    ]
}
```

