---
description: >-
  This endpoint allows you to start, stop or clear an activity tracker for a CMS
  user.
---

# Activity Tracker Start / Stop

## Activity Tracker Start Stop

<mark style="color:green;">`POST`</mark> `https://api.sonorancms.com/servers/activity_tracker_start_stop`

Start, stop or cancel an activity tracker for a CMS user.

#### Request Body

| Name | Type   | Description                    |
| ---- | ------ | ------------------------------ |
| id   | string | Community ID                   |
| key  | string | API Key                        |
| type | string | ACTIVITY\_TRACKER\_START\_STOP |
| data | object | DATA OBJECT                    |

{% tabs %}
{% tab title="200: OK " %}
```json
{
    "success": true,
    "data": {
        "id": "UUID_OF_TRACKER",
        "status": true,
        "accId": "UUID_OF_USER",
        "serverId": 1,
        "start": "TIMESTAMPTZ_STRING", 
        "end": null, // If ended this will be a TIMESTAMPTZ string
        "clearReason": null, // If cancelled this will be a string
        "metadata": {},
    }
}
```
{% endtab %}

{% tab title="400: Bad Request " %}
```javascript
INVALID REQUEST TYPE
INVALID COMMUNITY ID
ACCOUNT_NOT_FOUND
ACTIVITY_TRACKER_START_STOP_LOG_ERROR
```
{% endtab %}
{% endtabs %}

```json
{
    "id": "YOUR_COMMUNITY_ID",
    "key": "YOUR_API_KEY",
    "type": "ACTIVITY_TRACKER_SERVER_START",
    "data": {
        "serverId": 1,
        
        "discord": "", // Optional - One is Required
        "apiId": "", // Optional - One is Required
        "username": "", // Optional - One is Required
        "accId": "", // Optional - One is Required
        "uniqueId": "", // Optional - One is Required
        
        "forceClear": false, // Optional - Will clear out current activity tracker to start a new one
        "forceStart": false, // Optional - Will 
    }
}
```
