---
description: This endpoint allows you to toggle RSVP with an event from a community.
---

# RSVP

{% swagger method="post" path="/events/rsvp" baseUrl="https://api.sonorancms.com" summary="RSVP" %}
{% swagger-description %}
RSVP a community account found by API ID or account ID for an event.
{% endswagger-description %}

{% swagger-parameter in="body" name="id" type="string" required="true" %}
Community ID
{% endswagger-parameter %}

{% swagger-parameter in="body" name="key" type="string" required="true" %}
API Key
{% endswagger-parameter %}

{% swagger-parameter in="body" required="true" name="type" type="string" %}
RSVP
{% endswagger-parameter %}

{% swagger-parameter in="body" required="true" name="data" type="array" %}
Array of request objects
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="The following 200 response texts may be sent in response:" %}
```javascript
RSVP_SUCCESS // This string will return whenever the account is added to the RSVP
UNRSVP_SUCCESS // This string will return whenever the acocunt is removed from the RSVP list
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

```json
{
    "id": "YOUR_COMMUNITY_ID",
    "key": "YOUR_API_KEY",
    "type": "RSVP",
    "data": [
        {
            "eventId": "", // UUID of Event
            "apiId": "SOME_API_ID", // Optional - must have one (apiId or accId)
            "accId": "SOMEACCID", // Optional - must have one (apiId or accId)
        }
    ]
}
```
