---
description: Update the lock status for a form template.
---

# Set Form Lock Status

<mark style="color:green;">`PATCH`</mark> `https://api.sonorancms.com/v2/community/forms/1/lock`

> **Rate limit:** `18 requests per minute`  
> Authenticated v2 endpoints are rate limited per credential rather than per IP address.

Update the lock status for a form template.

## Route Parameters

| Name | Type | Required | Description |
| --- | --- | --- | --- |
| `templateId` | number | Yes | Target templateId. |

## Request Body

| Name | Type | Required | Description |
| --- | --- | --- | --- |
| `state` | boolean | Yes | See example request for the shape. |

## Example Request

{% tabs %}
{% tab title="OpenAPI" %}

```yaml
openapi: "3.0.3"
info:
  title: "Sonoran CMS v2 - Set Lock Status"
  version: "1.0.0"
  description: "Update the lock status for a form template."
servers:
  -
    url: "https://api.sonorancms.com"
paths:
  /v2/community/forms/{templateId}/lock:
    patch:
      summary: "Set Lock Status"
      operationId: "setFormLockStatus"
      parameters:
        -
          description: "Target form template id."
          name: "templateId"
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
                data: "Successfully set the lock state for Example Form to: LOCKED"
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
curl --request PATCH \
  --url "https://api.sonorancms.com/v2/community/forms/1/lock" \
  --header "Authorization: Bearer YOUR_API_KEY" \
  --header "Accept: application/json" \
  --data '{"state":true}'
```

{% endtab %}
{% endtabs %}

## Response

The `data` value is a confirmation string returned by the community service after the lock state is updated.

```json
{
  "success": true,
  "data": "Successfully set the lock state for Example Form to: LOCKED",
  "meta": {
    "timestamp": "2026-04-15T00:00:00.000Z",
    "path": "/v2/community/forms/1/lock"
  }
}
```
