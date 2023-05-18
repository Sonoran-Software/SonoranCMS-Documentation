---
description: This endpoint allows you to clock in/out a community account.
---

# Clock In Out

{% swagger method="post" path="/general/clock_in_out" baseUrl="https://api.sonorancms.com" summary="Clock In Out" %}
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
CLOCK_IN

___

OUT
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
    "type": "CLOCK_IN_OUT",
    "data": [
        {
            "apiId": "SOME_API_ID", // Optional - must have one (apiId or accId)
            "accId": "SOMEACCID", // Optional - must have one (apiId or accId)
            "forceClockIn": true // Optional - will start a new clock in replacing any current one
        }
    ]
}
```
