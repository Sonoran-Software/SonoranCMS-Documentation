---
description: Retrieve the configured profile fields.
---

# Get Profile Fields

<mark style="color:green;">`GET`</mark> `https://api.sonorancms.com/v2/community/profile-fields`

> **Rate limit:** `13 requests per minute`  
> Authenticated v2 endpoints are rate limited per credential rather than per IP address.

Retrieve the configured profile fields.

## Example Request

{% tabs %}
{% tab title="OpenAPI" %}

```yaml
openapi: "3.0.3"
info:
  title: "Sonoran CMS v2 - Get Profile Fields"
  version: "1.0.0"
  description: "Retrieve the configured profile fields."
servers:
  -
    url: "https://api.sonorancms.com"
paths:
  /v2/community/profile-fields:
    get:
      summary: "Get Profile Fields"
      operationId: "getProfileFields"
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
                    id: "discord"
                    label: "Discord"
                    type: "discord"
                    options: null
                    metadata:
                      placeholder: "username#0000"
                meta:
                  timestamp: "2026-04-15T00:00:00.000Z"
                  path: "/v2/community/profile-fields"
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
  --url "https://api.sonorancms.com/v2/community/profile-fields" \
  --header "Authorization: Bearer YOUR_API_KEY" \
  --header "Accept: application/json"
```

{% endtab %}
{% endtabs %}

## Response

The `data` array contains the community profile field definitions with their ids, labels, types, options, and metadata.

```json
{
  "success": true,
  "data": [
    {
      "id": "discord",
      "label": "Discord",
      "type": "discord",
      "options": null,
      "metadata": {
        "placeholder": "username#0000"
      }
    }
  ],
  "meta": {
    "timestamp": "2026-04-15T00:00:00.000Z",
    "path": "/v2/community/profile-fields"
  }
}
```
