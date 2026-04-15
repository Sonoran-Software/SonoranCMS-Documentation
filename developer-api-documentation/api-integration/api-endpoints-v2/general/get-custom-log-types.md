---
description: Retrieve the configured custom log types.
---

# Get Custom Log Types

<mark style="color:green;">`GET`</mark> `https://api.sonorancms.com/v2/community/custom-log-types`

> **Rate limit:** `13 requests per minute`  
> Authenticated v2 endpoints are rate limited per credential rather than per IP address.

Retrieve the configured custom log types.

## Example Request

{% tabs %}
{% tab title="OpenAPI" %}

```yaml
openapi: "3.0.3"
info:
  title: "Sonoran CMS v2 - Get Custom Log Types"
  version: "1.0.0"
  description: "Retrieve the configured custom log types."
servers:
  -
    url: "https://api.sonorancms.com"
paths:
  /v2/community/custom-log-types:
    get:
      summary: "Get Custom Log Types"
      operationId: "getCustomLogTypes"
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
                    id: "33333333-3333-3333-3333-333333333333"
                    label: "Internal Warning"
                    shortCode: "warn"
                    melonlyId: "101"
                meta:
                  timestamp: "2026-04-15T00:00:00.000Z"
                  path: "/v2/community/custom-log-types"
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
  --url "https://api.sonorancms.com/v2/community/custom-log-types" \
  --header "Authorization: Bearer YOUR_API_KEY" \
  --header "Accept: application/json"
```

{% endtab %}
{% endtabs %}

## Response

The `data` array contains the configured custom log types used by ERLC and disciplinary integrations.

```json
{
  "success": true,
  "data": [
    {
      "id": "33333333-3333-3333-3333-333333333333",
      "label": "Internal Warning",
      "shortCode": "warn",
      "melonlyId": "101"
    }
  ],
  "meta": {
    "timestamp": "2026-04-15T00:00:00.000Z",
    "path": "/v2/community/custom-log-types"
  }
}
```
