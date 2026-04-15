---
description: Retrieve the lock status for a form template.
---

# Get Form Lock Status

<mark style="color:green;">`GET`</mark> `https://api.sonorancms.com/v2/community/forms/1/lock`

> **Rate limit:** `27 requests per minute`  
> Authenticated v2 endpoints are rate limited per credential rather than per IP address.

Retrieve the lock status for a form template.

## Route Parameters

| Name | Type | Required | Description |
| --- | --- | --- | --- |
| `templateId` | number | Yes | Target templateId. |

## Example Request

{% tabs %}
{% tab title="OpenAPI" %}

```yaml
openapi: "3.0.3"
info:
  title: "Sonoran CMS v2 - Get Lock Status"
  version: "1.0.0"
  description: "Retrieve the lock status for a form template."
servers:
  -
    url: "https://api.sonorancms.com"
paths:
  /v2/community/forms/{templateId}/lock:
    get:
      summary: "Get Lock Status"
      operationId: "getFormLockStatus"
      parameters:
        -
          description: "Target form template id."
          name: "templateId"
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
                data: true
                meta:
                  timestamp: "2026-04-15T00:00:00.000Z"
                  path: "/v2/community/forms/1/lock"
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
  --url "https://api.sonorancms.com/v2/community/forms/1/lock" \
  --header "Authorization: Bearer YOUR_API_KEY" \
  --header "Accept: application/json"
```

{% endtab %}
{% endtabs %}

## Response

The `data` value is a boolean. `true` means the form template is locked; `false` means it is open.

```json
{
  "success": true,
  "data": true,
  "meta": {
    "timestamp": "2026-04-15T00:00:00.000Z",
    "path": "/v2/community/forms/1/lock"
  }
}
```
