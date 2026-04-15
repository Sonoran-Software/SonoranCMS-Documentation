---
description: Retrieve the current clock-in state for an account.
---

# Get Current Clock In

<mark style="color:green;">`GET`</mark> `https://api.sonorancms.com/v2/community/accounts/00000000-0000-0000-0000-000000000000/clock/current`

> **Rate limit:** `27 requests per minute`  
> Authenticated v2 endpoints are rate limited per credential rather than per IP address.

Retrieve the current clock-in state for an account.

## Route Parameters

| Name | Type | Required | Description |
| --- | --- | --- | --- |
| `accountId` | string (uuid) | Yes | Target accountId. |

## Query Parameters

| Name | Type | Required | Description |
| --- | --- | --- | --- |
| `accId` | string | Yes | See example request for the shape. |

## Example Request

{% tabs %}
{% tab title="OpenAPI" %}

```yaml
openapi: "3.0.3"
info:
  title: "Sonoran CMS v2 - Get Current Clock In"
  version: "1.0.0"
  description: "Retrieve the current clock-in state for an account."
servers:
  -
    url: "https://api.sonorancms.com"
paths:
  /v2/community/accounts/{accountId}/clock/current:
    get:
      summary: "Get Current Clock In"
      operationId: "getCurrentClockIn"
      parameters:
        -
          description: "Target account UUID."
          name: "accountId"
          in: "path"
          schema:
            type: "string"
            format: "uuid"
          required: true
        -
          description: "Target API identifier. Provide exactly one identifier."
          name: "apiId"
          in: "query"
          schema:
            type: "string"
          required: false
        -
          description: "Target username. Provide exactly one identifier."
          name: "username"
          in: "query"
          schema:
            type: "string"
          required: false
        -
          description: "Target Discord id. Provide exactly one identifier."
          name: "discordId"
          in: "query"
          schema:
            type: "string"
          required: false
        -
          description: "Target community unique id. Provide exactly one identifier."
          name: "uniqueId"
          in: "query"
          schema:
            type: "integer"
          required: false
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
                  id: "55555555-5555-5555-5555-555555555555"
                  startTime: "2026-04-15T00:00:00.000Z"
                  endTime: null
                  completed: false
                  notes: []
                  type: "patrol"
                meta:
                  timestamp: "2026-04-15T00:00:00.000Z"
                  path: "/v2/community/accounts/00000000-0000-0000-0000-000000000000/clock/current"
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
  --url "https://api.sonorancms.com/v2/community/accounts/00000000-0000-0000-0000-000000000000/clock/current?accId=00000000-0000-0000-0000-000000000000" \
  --header "Authorization: Bearer YOUR_API_KEY" \
  --header "Accept: application/json"
```

{% endtab %}
{% endtabs %}

## Response

The `data` value is either the active clock row or the string `"Not Clocked In"` when the account has no open clock.

```json
{
  "success": true,
  "data": {
    "id": "55555555-5555-5555-5555-555555555555",
    "startTime": "2026-04-15T00:00:00.000Z",
    "endTime": null,
    "completed": false,
    "notes": [],
    "type": "patrol"
  },
  "meta": {
    "timestamp": "2026-04-15T00:00:00.000Z",
    "path": "/v2/community/accounts/00000000-0000-0000-0000-000000000000/clock/current"
  }
}
```
