---
description: Cancel an active session.
---

# Cancel Session

<mark style="color:green;">`DELETE`</mark> `https://api.sonorancms.com/v2/community/sessions`

> **Rate limit:** `9 requests per minute`  
> Authenticated v2 endpoints are rate limited per credential rather than per IP address.

Cancel an active session.

## Request Body

| Name | Type | Required | Description |
| --- | --- | --- | --- |
| `serverId` | number | Yes | See example request for the shape. |
| `accId` | string | Yes | See example request for the shape. |

## Example Request

{% tabs %}
{% tab title="OpenAPI" %}

```yaml
openapi: "3.0.3"
info:
  title: "Sonoran CMS v2 - Cancel Session"
  version: "1.0.0"
  description: "Cancel an active session."
servers:
  -
    url: "https://api.sonorancms.com"
paths:
  /v2/community/sessions:
    delete:
      summary: "Cancel Session"
      operationId: "cancelSession"
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
        "204":
          description: "No Content"
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
curl --request DELETE \
  --url "https://api.sonorancms.com/v2/community/sessions" \
  --header "Authorization: Bearer YOUR_API_KEY" \
  --header "Accept: application/json" \
  --data '{"serverId":1,"accId":"00000000-0000-0000-0000-000000000000"}'
```

{% endtab %}
{% endtabs %}

## Response

The cancel endpoint intentionally returns no JSON body when it succeeds.

This endpoint returns `204 No Content` on success, so there is no response body.
