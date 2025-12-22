---
description: >-
  This endpoint allows you to stop the current session for the specified server
  ID.
---

# Stop Session

{% hint style="warning" %}
API endpoint requires the **FREE** version of Sonoran CMS or higher.\
For more information, see our [pricing ](../../../../pricing/pricing-faq/)page.
{% endhint %}

## Start Session

<mark style="color:green;">`POST`</mark> `https://api.sonorancms.com/sessions/stop`&#x20;

Stops the current session for the specified server ID.

#### Request Body

| Name                                   | Type   | Description              |
| -------------------------------------- | ------ | ------------------------ |
| id<mark style="color:red;">\*</mark>   | string | Community ID             |
| key<mark style="color:red;">\*</mark>  | string | API Key                  |
| type<mark style="color:red;">\*</mark> | string | STOP\_SESSION            |
| data<mark style="color:red;">\*</mark> | array  | Array of request objects |

{% tabs %}
{% tab title="200: OK " %}
```javascript
{
    "id": "UUID_OF_SESSION",
    "sysStatus": true,
    "community": "YOUR_COMMUNITY_ID",
    "serverId": 1,
    "startedBy": "UUID_OF_SESSION_STARTER",
    "startedAt": "TIMESTAMPTZ_STRING",
    "endedBy": "UUID_OF_SESSION_ENDER",
    "endedAt": "TIMESTAMPTZ_STRING",
    "cancelledBy": null,
    "stats": {},
    "metadata": {},
}
```
{% endtab %}

{% tab title="400: Bad Request The following 400 errors may be sent in response:" %}
```javascript
INVALID API KEY
INVALID COMMUNITY ID
NO_SERVER_ID
INVALID_SERVER
SESSION_ERROR
```
{% endtab %}
{% endtabs %}

```json
{
    "id": "YOUR_COMMUNITY_ID",
    "key": "YOUR_API_KEY",
    "type": "STOP_SESSION",
    "data": [
        {
            "serverId": 1,
            "accId": "ACCID_OF_USER_STOPPING_SESSION",
        }
    ]
}
```
