---
description: Retrieve the current community summary.
---

# Get Community

<mark style="color:green;">`GET`</mark> `https://api.sonorancms.com/v2/community`

> **Rate limit:** `13 requests per minute`  
> Authenticated v2 endpoints are rate limited per credential rather than per IP address.

Retrieve the current community summary.

## Example Request

{% tabs %}
{% tab title="OpenAPI" %}

```yaml
openapi: "3.0.3"
info:
  title: "Sonoran CMS v2 - Get Community"
  version: "1.0.0"
  description: "Retrieve the current community summary."
servers:
  -
    url: "https://api.sonorancms.com"
paths:
  /v2/community:
    get:
      summary: "Get Community"
      operationId: "getCommunity"
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
                  id: "CMS-1000"
                  uuid: "00000000-0000-0000-0000-000000000000"
                  name: "Example Community"
                  subVersion: 5
                  tier: "SonoranOne"
                  servers: 3
                meta:
                  timestamp: "2026-04-15T00:00:00.000Z"
                  path: "/v2/community"
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
  --url "https://api.sonorancms.com/v2/community" \
  --header "Authorization: Bearer YOUR_API_KEY" \
  --header "Accept: application/json"
```

{% endtab %}
{% endtabs %}

## Response

The `data` object is the community summary returned by `V2Service.summary()`. It includes the community identifier, UUID, name, sub-version, resolved tier, and server count.

```json
{
  "success": true,
  "data": {
    "id": "CMS-1000",
    "uuid": "00000000-0000-0000-0000-000000000000",
    "name": "Example Community",
    "subVersion": 5,
    "tier": "SonoranOne",
    "servers": 3
  },
  "meta": {
    "timestamp": "2026-04-15T00:00:00.000Z",
    "path": "/v2/community"
  }
}
```
