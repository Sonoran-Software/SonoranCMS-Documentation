---
description: Retrieve the configured clock-in types.
---

# Get Clock In Types

<mark style="color:green;">`GET`</mark> `https://api.sonorancms.com/v2/community/clockin-types`

> **Rate limit:** `13 requests per minute`  
> Authenticated v2 endpoints are rate limited per credential rather than per IP address.

Retrieve the configured clock-in types.

## Example Request

{% tabs %}
{% tab title="OpenAPI" %}

```yaml
openapi: "3.0.3"
info:
  title: "Sonoran CMS v2 - Get Clockin Types"
  version: "1.0.0"
  description: "Retrieve the configured clock-in types."
servers:
  -
    url: "https://api.sonorancms.com"
paths:
  /v2/community/clockin-types:
    get:
      summary: "Get Clockin Types"
      operationId: "getClockInTypes"
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
                    id: "patrol"
                    label: "Patrol"
                meta:
                  timestamp: "2026-04-15T00:00:00.000Z"
                  path: "/v2/community/clockin-types"
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
  --url "https://api.sonorancms.com/v2/community/clockin-types" \
  --header "Authorization: Bearer YOUR_API_KEY" \
  --header "Accept: application/json"
```

{% endtab %}
{% endtabs %}

## Response

The `data` array contains the community clock-in types exactly as configured in the community settings.

```json
{
  "success": true,
  "data": [
    {
      "id": "patrol",
      "label": "Patrol"
    }
  ],
  "meta": {
    "timestamp": "2026-04-15T00:00:00.000Z",
    "path": "/v2/community/clockin-types"
  }
}
```
