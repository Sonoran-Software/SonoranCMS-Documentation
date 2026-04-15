---
description: Retrieve the ER:LC queue.
---

# Get Player Queue

<mark style="color:green;">`GET`</mark> `https://api.sonorancms.com/v2/community/erlc/players/queue`

> **Rate limit:** `27 requests per minute`  
> Authenticated v2 endpoints are rate limited per credential rather than per IP address.

Retrieve the ER:LC queue.

## Query Parameters

| Name | Type | Required | Description |
| --- | --- | --- | --- |
| `robloxJoinCode` | string | Yes | See example request for the shape. |

## Example Request

{% tabs %}
{% tab title="OpenAPI" %}

```yaml
openapi: "3.0.3"
info:
  title: "Sonoran CMS v2 - Get Player Queue"
  version: "1.0.0"
  description: "Retrieve the ER:LC queue."
servers:
  -
    url: "https://api.sonorancms.com"
paths:
  /v2/community/erlc/players/queue:
    get:
      summary: "Get Player Queue"
      operationId: "getPlayerQueue"
      parameters:
        -
          description: "Target Roblox join code."
          name: "robloxJoinCode"
          in: "query"
          schema:
            type: "string"
          required: false
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
                data: 3
                meta:
                  timestamp: "2026-04-15T00:00:00.000Z"
                  path: "/v2/community/erlc/players/queue"
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
  --url "https://api.sonorancms.com/v2/community/erlc/players/queue?robloxJoinCode=ABC123" \
  --header "Authorization: Bearer YOUR_API_KEY" \
  --header "Accept: application/json"
```

{% endtab %}
{% endtabs %}

## Response

The `data` value is the current queue length for the target server, not the queue entries themselves.

```json
{
  "success": true,
  "data": 3,
  "meta": {
    "timestamp": "2026-04-15T00:00:00.000Z",
    "path": "/v2/community/erlc/players/queue"
  }
}
```
