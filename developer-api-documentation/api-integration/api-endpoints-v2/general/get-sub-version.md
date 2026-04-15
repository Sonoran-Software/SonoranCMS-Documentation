---
description: Retrieve the community subscription tier.
---

# Get Sub Version

<mark style="color:green;">`GET`</mark> `https://api.sonorancms.com/v2/community/sub-version`

> **Rate limit:** `13 requests per minute`  
> Authenticated v2 endpoints are rate limited per credential rather than per IP address.

Retrieve the community subscription tier.

## Example Request

{% tabs %}
{% tab title="OpenAPI" %}

```yaml
openapi: "3.0.3"
info:
  title: "Sonoran CMS v2 - Get Sub Version"
  version: "1.0.0"
  description: "Retrieve the community subscription tier."
servers:
  -
    url: "https://api.sonorancms.com"
paths:
  /v2/community/sub-version:
    get:
      summary: "Get Sub Version"
      operationId: "getSubVersion"
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
                  subVersion: 5
                  tier: "SonoranOne"
                meta:
                  timestamp: "2026-04-15T00:00:00.000Z"
                  path: "/v2/community/sub-version"
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
  --url "https://api.sonorancms.com/v2/community/sub-version" \
  --header "Authorization: Bearer YOUR_API_KEY" \
  --header "Accept: application/json"
```

{% endtab %}
{% endtabs %}

## Response

The `data` object is the current community sub-version and the resolved tier name from `SubNumLevelToName()`.

```json
{
  "success": true,
  "data": {
    "subVersion": 5,
    "tier": "SonoranOne"
  },
  "meta": {
    "timestamp": "2026-04-15T00:00:00.000Z",
    "path": "/v2/community/sub-version"
  }
}
```
