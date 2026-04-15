---
description: Update the display name for an account.
---

# Set Account Name

<mark style="color:green;">`PATCH`</mark> `https://api.sonorancms.com/v2/community/accounts/00000000-0000-0000-0000-000000000000/name`

> **Rate limit:** `22 requests per minute`  
> Authenticated v2 endpoints are rate limited per credential rather than per IP address.

Update the display name for an account.

## Route Parameters

| Name | Type | Required | Description |
| --- | --- | --- | --- |
| `accountId` | string (uuid) | Yes | Target accountId. |

## Request Body

| Name | Type | Required | Description |
| --- | --- | --- | --- |
| `newName` | string | Yes | See example request for the shape. |

## Example Request

{% tabs %}
{% tab title="OpenAPI" %}

```yaml
openapi: "3.0.3"
info:
  title: "Sonoran CMS v2 - Set Account Name"
  version: "1.0.0"
  description: "Update the display name for an account."
servers:
  -
    url: "https://api.sonorancms.com"
paths:
  /v2/community/accounts/{accountId}/name:
    patch:
      summary: "Set Account Name"
      operationId: "setAccountName"
      parameters:
        -
          description: "Target account UUID."
          name: "accountId"
          in: "path"
          schema:
            type: "string"
            format: "uuid"
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
                data: "New Community Name (00000000-0000-0000-0000-000000000000): Example Account"
                meta:
                  timestamp: "2026-04-15T00:00:00.000Z"
                  path: "/v2/community/accounts/00000000-0000-0000-0000-000000000000/name"
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
  --url "https://api.sonorancms.com/v2/community/accounts/00000000-0000-0000-0000-000000000000/name" \
  --header "Authorization: Bearer YOUR_API_KEY" \
  --header "Accept: application/json" \
  --data '{"newName":"Example Account"}'
```

{% endtab %}
{% endtabs %}

## Response

The `data` value is a confirmation string, not an account object. The account update still happens in the background through the service layer.

```json
{
  "success": true,
  "data": "New Community Name (00000000-0000-0000-0000-000000000000): Example Account",
  "meta": {
    "timestamp": "2026-04-15T00:00:00.000Z",
    "path": "/v2/community/accounts/00000000-0000-0000-0000-000000000000/name"
  }
}
```
