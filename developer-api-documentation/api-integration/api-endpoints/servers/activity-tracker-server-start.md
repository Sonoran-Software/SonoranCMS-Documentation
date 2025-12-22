---
description: >-
  This endpoint allows you to stop all current activity trackers for the
  specified server ID.
---

# Activity Tracker Server Start

## Activity Tracker Server Start

<mark style="color:green;">`POST`</mark> `https://api.sonorancms.com/servers/activity_tracker_server_start`

Stop all current activity trackers for the specified server ID.

#### Request Body

| Name | Type   | Description                      |
| ---- | ------ | -------------------------------- |
| id   | string | Community ID                     |
| key  | string | API Key                          |
| type | string | ACTIVITY\_TRACKER\_SERVER\_START |
| data | object | DATA OBJECT                      |

{% tabs %}
{% tab title="200: OK " %}
```json
{
    "success": true,
    "data": [
       {
           "id": "UUID_OF_TRACKER",
           "status": true,
           "accId": "UUID_OF_USER",
           "serverId": 1,
           "start": "TIMESTAMPTZ_STRING", 
           "end": "TIMESTAMPTZ_STRING",
           "clearReason": "All server activity stopped that were in progress",
           "metadata": {},
        },
        ...
    ]
}
```
{% endtab %}

{% tab title="400: Bad Request " %}
```javascript
INVALID REQUEST TYPE
INVALID COMMUNITY ID
```
{% endtab %}
{% endtabs %}

```json
{
    "id": "YOUR_COMMUNITY_ID",
    "key": "YOUR_API_KEY",
    "type": "ACTIVITY_TRACKER_START_STOP",
    "data": {
        "serverId": 1,
    }
}
```
