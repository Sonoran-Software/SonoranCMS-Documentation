---
description: Start activity tracking for a server.
---

# Activity Tracker Server Start

<mark style="color:green;">`POST`</mark> `https://api.sonorancms.com/v2/community/servers/1/activity/start`

> **Rate limit:** `27 requests per minute`  
> Authenticated v2 endpoints are rate limited per credential rather than per IP address.

Start activity tracking for a server.

## Route Parameters

| Name | Type | Required | Description |
| --- | --- | --- | --- |
| `serverId` | number | Yes | Target serverId. |

## Example Request

{% tabs %}
{% tab title="OpenAPI" %}

```yaml
openapi: "3.0.3"
info:
  title: "Sonoran CMS v2 - Activity Tracker Server Start"
  version: "1.0.0"
  description: "Start activity tracking for a server."
servers:
  -
    url: "https://api.sonorancms.com"
paths:
  /v2/community/servers/{serverId}/activity/start:
    post:
      summary: "Activity Tracker Server Start"
      operationId: "activityTrackerServerStart"
      parameters:
        -
          description: "Target server id."
          name: "serverId"
          in: "path"
          schema:
            type: "integer"
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
                  -
                    id: "55555555-5555-5555-5555-555555555555"
                    accId: "00000000-0000-0000-0000-000000000000"
                    serverId: 1
                    end: "2026-04-15T00:00:00.000Z"
                meta:
                  timestamp: "2026-04-15T00:00:00.000Z"
                  path: "/v2/community/servers/1/activity/start"
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
  --url "https://api.sonorancms.com/v2/community/servers/1/activity/start" \
  --header "Authorization: Bearer YOUR_API_KEY" \
  --header "Accept: application/json"
```

{% endtab %}
{% endtabs %}

## Response

The `data` array contains the rows that were force-finished when a server start reset cleared in-progress activity.

```json
{
  "success": true,
  "data": [
    {
      "id": "55555555-5555-5555-5555-555555555555",
      "accId": "00000000-0000-0000-0000-000000000000",
      "serverId": 1,
      "end": "2026-04-15T00:00:00.000Z"
    }
  ],
  "meta": {
    "timestamp": "2026-04-15T00:00:00.000Z",
    "path": "/v2/community/servers/1/activity/start"
  }
}
```
