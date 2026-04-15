---
description: Record a server activity event.
---

# Activity Tracker

<mark style="color:green;">`POST`</mark> `https://api.sonorancms.com/v2/community/servers/1/activity`

> **Rate limit:** `27 requests per minute`  
> Authenticated v2 endpoints are rate limited per credential rather than per IP address.

Record a server activity event.

## Route Parameters

| Name | Type | Required | Description |
| --- | --- | --- | --- |
| `serverId` | number | Yes | Target serverId. |

## Request Body

| Name | Type | Required | Description |
| --- | --- | --- | --- |
| `accId` | string | Yes | See example request for the shape. |
| `forceStart` | boolean | Yes | See example request for the shape. |

## Example Request

{% tabs %}
{% tab title="OpenAPI" %}

```yaml
openapi: "3.0.3"
info:
  title: "Sonoran CMS v2 - Activity Tracker"
  version: "1.0.0"
  description: "Record a server activity event."
servers:
  -
    url: "https://api.sonorancms.com"
paths:
  /v2/community/servers/{serverId}/activity:
    post:
      summary: "Activity Tracker"
      operationId: "activityTracker"
      parameters:
        -
          description: "Target server id."
          name: "serverId"
          in: "path"
          schema:
            type: "integer"
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
                  id: "55555555-5555-5555-5555-555555555555"
                  status: true
                  accId: "00000000-0000-0000-0000-000000000000"
                  serverId: 1
                  start: "2026-04-15T00:00:00.000Z"
                  end: null
                  clearReason: null
                  metadata: {}
                meta:
                  timestamp: "2026-04-15T00:00:00.000Z"
                  path: "/v2/community/servers/1/activity"
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
  --url "https://api.sonorancms.com/v2/community/servers/1/activity" \
  --header "Authorization: Bearer YOUR_API_KEY" \
  --header "Accept: application/json" \
  --data '{"accId":"00000000-0000-0000-0000-000000000000","forceStart":true}'
```

{% endtab %}
{% endtabs %}

## Response

The `data` object is the activity row that was created or updated. Stop/clear branches can return partial row objects with the updated timestamps or clear reason.

```json
{
  "success": true,
  "data": {
    "id": "55555555-5555-5555-5555-555555555555",
    "status": true,
    "accId": "00000000-0000-0000-0000-000000000000",
    "serverId": 1,
    "start": "2026-04-15T00:00:00.000Z",
    "end": null,
    "clearReason": null,
    "metadata": {}
  },
  "meta": {
    "timestamp": "2026-04-15T00:00:00.000Z",
    "path": "/v2/community/servers/1/activity"
  }
}
```
