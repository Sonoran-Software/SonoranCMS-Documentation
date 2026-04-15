---
description: Retrieve a single community account.
---

# Get Account

<mark style="color:green;">`GET`</mark> `https://api.sonorancms.com/v2/community/accounts/00000000-0000-0000-0000-000000000000`

> **Rate limit:** `27 requests per minute`  
> Authenticated v2 endpoints are rate limited per credential rather than per IP address.

Retrieve a single community account.

## Route Parameters

| Name | Type | Required | Description |
| --- | --- | --- | --- |
| `accountId` | string (uuid) | Yes | Target accountId. |

## Example Request

{% tabs %}
{% tab title="OpenAPI" %}

```yaml
openapi: "3.0.3"
info:
  title: "Sonoran CMS v2 - Get Account"
  version: "1.0.0"
  description: "Retrieve a single community account."
servers:
  -
    url: "https://api.sonorancms.com"
paths:
  /v2/community/accounts/{accountId}:
    get:
      summary: "Get Account"
      operationId: "getAccount"
      parameters:
        -
          description: "Target account UUID."
          name: "accountId"
          in: "path"
          schema:
            type: "string"
            format: "uuid"
          required: true
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
                  archived: false
                  activeApiIds:
                    - "discord:1234567890"
                  discordId: "1234567890"
                  uniqueId: 1001
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
                  profileFields:
                    data:
                      -
                        id: "discord"
                        value: "1234567890"
                  clockData:
                    data:
                      -
                        id: "55555555-5555-5555-5555-555555555555"
                        startTime: "2026-04-15T00:00:00.000Z"
                        endTime: null
                        completed: false
                        notes: []
                        type: "patrol"
                  teamspeakId: null
                meta:
                  timestamp: "2026-04-15T00:00:00.000Z"
                  path: "/v2/community/accounts/00000000-0000-0000-0000-000000000000"
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
curl --request GET \
  --url "https://api.sonorancms.com/v2/community/accounts/00000000-0000-0000-0000-000000000000" \
  --header "Authorization: Bearer YOUR_API_KEY" \
  --header "Accept: application/json"
```

{% endtab %}
{% endtabs %}

## Response

Successful requests return `application/json` and use the standard v2 envelope.
This endpoint returns the API-selected account subset plus hydrated `clockData` and `teamspeakId`.

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
    "archived": false,
    "activeApiIds": [
      "discord:1234567890"
    ],
    "discordId": "1234567890",
    "uniqueId": 1001,
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
    "profileFields": {
      "data": [
        {
          "id": "discord",
          "value": "1234567890"
        }
      ]
    },
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
    "teamspeakId": null
  },
  "meta": {
    "timestamp": "2026-04-15T00:00:00.000Z",
    "path": "/v2/community/accounts/00000000-0000-0000-0000-000000000000"
  }
}
```