---
description: Register one or more identifiers for an account.
---

# Register Identifiers

<mark style="color:green;">`POST`</mark> `https://api.sonorancms.com/v2/community/accounts/00000000-0000-0000-0000-000000000000/identifiers`

> **Rate limit:** `22 requests per minute`  
> Authenticated v2 endpoints are rate limited per credential rather than per IP address.

Register one or more identifiers for an account.

## Route Parameters

| Name | Type | Required | Description |
| --- | --- | --- | --- |
| `accountId` | string (uuid) | Yes | Target accountId. |

## Request Body

| Name | Type | Required | Description |
| --- | --- | --- | --- |
| `identifiers` | array | Yes | See example request for the shape. |

## Example Request

{% tabs %}
{% tab title="OpenAPI" %}

```yaml
openapi: "3.0.3"
info:
  title: "Sonoran CMS v2 - Register Identifiers"
  version: "1.0.0"
  description: "Register one or more identifiers for an account."
servers:
  -
    url: "https://api.sonorancms.com"
paths:
  /v2/community/accounts/{accountId}/identifiers:
    post:
      summary: "Register Identifiers"
      operationId: "registerIdentifiers"
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
        "201":
          description: "Successful response"
          content:
            application/json:
              schema:
                type: "object"
              example:
                success: true
                data:
                  -
                    type: "discord"
                    value: "1234567890"
                  -
                    type: "roblox"
                    value: "987654321"
                meta:
                  timestamp: "2026-04-15T00:00:00.000Z"
                  path: "/v2/community/accounts/00000000-0000-0000-0000-000000000000/identifiers"
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
curl --request POST \
  --url "https://api.sonorancms.com/v2/community/accounts/00000000-0000-0000-0000-000000000000/identifiers" \
  --header "Authorization: Bearer YOUR_API_KEY" \
  --header "Accept: application/json" \
  --data '{"identifiers":[{"type":"discord","value":"1234567890"}]}'
```

{% endtab %}
{% endtabs %}

## Response

The `data` array contains only the identifier type/value pairs that were registered successfully for the account.

```json
{
  "success": true,
  "data": [
    {
      "type": "discord",
      "value": "1234567890"
    },
    {
      "type": "roblox",
      "value": "987654321"
    }
  ],
  "meta": {
    "timestamp": "2026-04-15T00:00:00.000Z",
    "path": "/v2/community/accounts/00000000-0000-0000-0000-000000000000/identifiers"
  }
}
```
