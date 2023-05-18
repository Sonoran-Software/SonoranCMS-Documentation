---
description: This endpoint allows you to check a community API ID.
---

# Check Com API ID

{% swagger method="post" path="/general/check_com_apiid" baseUrl="https://api.sonorancms.com" summary="Check Com APIID" %}
{% swagger-description %}
Check if a API ID is attached to any community account
{% endswagger-description %}

{% swagger-parameter in="body" name="id" type="string" required="true" %}
Community ID
{% endswagger-parameter %}

{% swagger-parameter in="body" name="key" type="string" required="true" %}
API Key
{% endswagger-parameter %}

{% swagger-parameter in="body" required="true" name="type" type="string" %}
CHECK_COM

___

APIID
{% endswagger-parameter %}

{% swagger-parameter in="body" required="true" name="data" type="array" %}
Array of request objects
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```javascript
{{Sonoran CMS Account Username}}
```
{% endswagger-response %}

{% swagger-response status="400: Bad Request" description="The following 400 errors may be sent in response:" %}
```javascript
INVALID API KEY
INVALID COMMUNITY ID
API ID NOT LINKED TO AN ACCOUNT IN THIS COMMUNITY
```
{% endswagger-response %}
{% endswagger %}

```
{
    "id": "YOUR_COMMUNITY_ID",
    "key": "YOUR_API_KEY",
    "type": "CHECK_COM_APIID",
    "data": [
        {
            "apiId": "SOME_API_ID"
        }
    ]
}
```

