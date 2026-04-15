---
description: Undo a previously recorded rank change.
---

# Undo Rank Change

<mark style="color:green;">`POST`</mark> `https://api.sonorancms.com/v2/community/rank-changes/11111111-1111-1111-1111-111111111111/undo`

> **Rate limit:** `13 requests per minute`  
> Authenticated v2 endpoints are rate limited per credential rather than per IP address.

Undo a previously recorded rank change.

## Route Parameters

| Name | Type | Required | Description |
| --- | --- | --- | --- |
| `undoId` | string (uuid) | Yes | Target undoId. |

## Request Body

| Name | Type | Required | Description |
| --- | --- | --- | --- |
| `userId` | string | Yes | See example request for the shape. |

## Example Request

{% tabs %}
{% tab title="OpenAPI" %}

```yaml
openapi: "3.0.3"
info:
  title: "Sonoran CMS v2 - Undo Rank Change"
  version: "1.0.0"
  description: "Undo a previously recorded rank change."
servers:
  -
    url: "https://api.sonorancms.com"
paths:
  /v2/community/rank-changes/{undoId}/undo:
    post:
      summary: "Undo Rank Change"
      operationId: "undoRankChange"
      parameters:
        -
          description: "Target rank change undo id."
          name: "undoId"
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
                  undoId: "55555555-5555-5555-5555-555555555555"
                  account:
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
                  previousRanks:
                    - "11111111-1111-1111-1111-111111111111"
                  currentRanks:
                    - "22222222-2222-2222-2222-222222222222"
                  originalLogId: "44444444-4444-4444-4444-444444444444"
                  reversalUndoId: "33333333-3333-3333-3333-333333333333"
                meta:
                  timestamp: "2026-04-15T00:00:00.000Z"
                  path: "/v2/community/rank-changes/11111111-1111-1111-1111-111111111111/undo"
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
curl --request POST \
  --url "https://api.sonorancms.com/v2/community/rank-changes/11111111-1111-1111-1111-111111111111/undo" \
  --header "Authorization: Bearer YOUR_API_KEY" \
  --header "Accept: application/json" \
  --data '{"userId":"11111111-1111-1111-1111-111111111111"}'
```

{% endtab %}
{% endtabs %}

## Response

The `data` object contains the undo summary, the updated account, the previous and current ranks, and the original/reversal log ids.

```json
{
  "success": true,
  "data": {
    "undoId": "55555555-5555-5555-5555-555555555555",
    "account": {
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
    "previousRanks": [
      "11111111-1111-1111-1111-111111111111"
    ],
    "currentRanks": [
      "22222222-2222-2222-2222-222222222222"
    ],
    "originalLogId": "44444444-4444-4444-4444-444444444444",
    "reversalUndoId": "33333333-3333-3333-3333-333333333333"
  },
  "meta": {
    "timestamp": "2026-04-15T00:00:00.000Z",
    "path": "/v2/community/rank-changes/11111111-1111-1111-1111-111111111111/undo"
  }
}
```
