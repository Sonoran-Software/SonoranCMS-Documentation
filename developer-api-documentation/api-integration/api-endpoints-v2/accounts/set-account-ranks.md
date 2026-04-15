---
description: Update the ranks assigned to an account.
---

# Set Account Ranks

<mark style="color:green;">`PATCH`</mark> `https://api.sonorancms.com/v2/community/accounts/00000000-0000-0000-0000-000000000000/ranks`

> **Rate limit:** `22 requests per minute`  
> Authenticated v2 endpoints are rate limited per credential rather than per IP address.

Update the ranks assigned to an account.

## Route Parameters

| Name | Type | Required | Description |
| --- | --- | --- | --- |
| `accountId` | string (uuid) | Yes | Target accountId. |

## Request Body

| Name | Type | Required | Description |
| --- | --- | --- | --- |
| `accId` | string | Yes | See example request for the shape. |
| `add` | array | Yes | See example request for the shape. |
| `active` | boolean | Yes | See example request for the shape. |

## Example Request

{% tabs %}
{% tab title="OpenAPI" %}

```yaml
openapi: "3.0.3"
info:
  title: "Sonoran CMS v2 - Set Account Ranks"
  version: "1.0.0"
  description: "Update the ranks assigned to an account."
servers:
  -
    url: "https://api.sonorancms.com"
paths:
  /v2/community/accounts/{accountId}/ranks:
    patch:
      summary: "Set Account Ranks"
      operationId: "setAccountRanks"
      parameters:
        -
          description: "Target account UUID."
          name: "accountId"
          in: "path"
          schema:
            type: "string"
            format: "uuid"
          required: true
      requestBody:
        required: true
        content:
          application/json:
            schema:
              type: "object"
      security:
        -
          bearerAuth: []
      responses:
        "200":
          description: "Successful response"
          content:
            application/json:
              schema:
                type: "object"
              example:
                success: true
                data:
                  accId: "00000000-0000-0000-0000-000000000000"
                  sysStatus: true
                  comStatus: true
                  accName: "ExampleAccount"
                  comName: "Example Community"
                  joinDate: "2026-04-15T00:00:00.000Z"
                  lastLogin: "2026-04-15T00:00:00.000Z"
                  owner: false
                  banned: false
                  banInfo: null
                  banExpiration: null
                  apiIdPreference: 0
                  apiIds:
                    ids: []
                  activeApiIds:
                    - "discord:1234567890"
                  identifiers:
                    idents:
                      -
                        id: "55555555-5555-5555-5555-555555555555"
                        accId: "00000000-0000-0000-0000-000000000000"
                        type: "discord"
                        value: "1234567890"
                        refCount: 1
                        verified: true
                        metadata: {}
                        flagId: null
                        createdAt: "2026-04-15T00:00:00.000Z"
                        updatedAt: null
                  ranks:
                    - "22222222-2222-2222-2222-222222222222"
                  clockData:
                    data:
                      -
                        id: "55555555-5555-5555-5555-555555555555"
                        startTime: "2026-04-15T00:00:00.000Z"
                        endTime: null
                        completed: false
                        notes: []
                        type: "patrol"
                  profileFields:
                    data:
                      -
                        id: "discord"
                        value: "1234567890"
                  bio: null
                  archived: false
                  discordId: "1234567890"
                  robloxId: "987654321"
                  uniqueId: 1001
                  customUniqueId: false
                  notificationPreferences:
                    forms:
                      statusChange:
                        inbox: true
                        desktop: true
                        mobile: true
                        email: true
                        discord: true
                  teamspeakId: null
                meta:
                  timestamp: "2026-04-15T00:00:00.000Z"
                  path: "/v2/community/accounts/00000000-0000-0000-0000-000000000000/ranks"
components:
  securitySchemes:
    bearerAuth:
      type: "http"
      scheme: "bearer"
      bearerFormat: "JWT"
```

{% endtab %}
{% tab title="cURL" %}

```bash
curl --request PATCH \
  --url "https://api.sonorancms.com/v2/community/accounts/00000000-0000-0000-0000-000000000000/ranks" \
  --header "Authorization: Bearer YOUR_API_KEY" \
  --header "Accept: application/json" \
  --data '{"accId":"00000000-0000-0000-0000-000000000000","add":["rank-1"],"active":true}'
```

{% endtab %}
{% endtabs %}

## Response

The `data` object is the updated account row returned by the rank update service. It reflects the new `ranks` and community status after the update.

```json
{
  "success": true,
  "data": {
    "accId": "00000000-0000-0000-0000-000000000000",
    "sysStatus": true,
    "comStatus": true,
    "accName": "ExampleAccount",
    "comName": "Example Community",
    "joinDate": "2026-04-15T00:00:00.000Z",
    "lastLogin": "2026-04-15T00:00:00.000Z",
    "owner": false,
    "banned": false,
    "banInfo": null,
    "banExpiration": null,
    "apiIdPreference": 0,
    "apiIds": {
      "ids": []
    },
    "activeApiIds": [
      "discord:1234567890"
    ],
    "identifiers": {
      "idents": [
        {
          "id": "55555555-5555-5555-5555-555555555555",
          "accId": "00000000-0000-0000-0000-000000000000",
          "type": "discord",
          "value": "1234567890",
          "refCount": 1,
          "verified": true,
          "metadata": {},
          "flagId": null,
          "createdAt": "2026-04-15T00:00:00.000Z",
          "updatedAt": null
        }
      ]
    },
    "ranks": [
      "22222222-2222-2222-2222-222222222222"
    ],
    "clockData": {
      "data": [
        {
          "id": "55555555-5555-5555-5555-555555555555",
          "startTime": "2026-04-15T00:00:00.000Z",
          "endTime": null,
          "completed": false,
          "notes": [],
          "type": "patrol"
        }
      ]
    },
    "profileFields": {
      "data": [
        {
          "id": "discord",
          "value": "1234567890"
        }
      ]
    },
    "bio": null,
    "archived": false,
    "discordId": "1234567890",
    "robloxId": "987654321",
    "uniqueId": 1001,
    "customUniqueId": false,
    "notificationPreferences": {
      "forms": {
        "statusChange": {
          "inbox": true,
          "desktop": true,
          "mobile": true,
          "email": true,
          "discord": true
        }
      }
    },
    "teamspeakId": null
  },
  "meta": {
    "timestamp": "2026-04-15T00:00:00.000Z",
    "path": "/v2/community/accounts/00000000-0000-0000-0000-000000000000/ranks"
  }
}
```
