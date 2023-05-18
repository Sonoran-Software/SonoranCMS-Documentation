---
description: Provides all departments and their ranks (and their associated IDs)
---

# Get Departments

{% swagger method="post" path="/general/get_departments" baseUrl="https://api.sonorancms.com" summary="Get Departments" %}
{% swagger-description %}
Get a Sonoran CMS community account's ranks by account ID, API ID, or username.
{% endswagger-description %}

{% swagger-parameter in="body" name="id" type="string" required="true" %}
Community ID
{% endswagger-parameter %}

{% swagger-parameter in="body" name="key" type="string" required="true" %}
API Key
{% endswagger-parameter %}

{% swagger-parameter in="body" required="true" name="type" type="string" %}
GET_COM_ACCOUNT
{% endswagger-parameter %}

{% swagger-parameter in="body" required="true" name="data" type="array" %}
Array of request objects
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```javascript
[
    "4298c76d-a1ee-46dc-b33c-8daf2e2280dd", // UUID of Rank
    ...
]
```
{% endswagger-response %}

{% swagger-response status="400: Bad Request" description="The following 400 errors may be sent in response:" %}
```javascript
INVALID API KEY
INVALID COMMUNITY ID
API ID NOT LINKED TO AN ACCOUNT IN THIS COMMUNITY
NO ACCOUNT FOUND UNDER GIVEN PARAMETERS IN THIS COMMUNITY
```
{% endswagger-response %}
{% endswagger %}

```
{
    "id": "YOUR_COMMUNITY_ID",
    "key": "YOUR_API_KEY",
    "type": "GET_DEPARTMENTS"
}
```
