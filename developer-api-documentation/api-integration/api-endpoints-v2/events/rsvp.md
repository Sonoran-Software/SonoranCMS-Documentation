---
description: Create an RSVP for an event.
---

# RSVP

<mark style="color:green;">`POST`</mark> `https://api.sonorancms.com/v2/community/events/11111111-1111-1111-1111-111111111111/rsvps`

> **Rate limit:** `27 requests per minute`  
> Authenticated v2 endpoints are rate limited per credential rather than per IP address.

Create an RSVP for an event.

## Route Parameters

| Name | Type | Required | Description |
| --- | --- | --- | --- |
| `eventId` | string (uuid) | Yes | Target eventId. |

## Request Body

| Name | Type | Required | Description |
| --- | --- | --- | --- |
| `accId` | string | Yes | See example request for the shape. |

## Example Request

{% tabs %}
{% tab title="OpenAPI" %}

```yaml
openapi: "3.0.3"
info:
  title: "Sonoran CMS v2 - Rsvp"
  version: "1.0.0"
  description: "Create an RSVP for an event."
servers:
  -
    url: "https://api.sonorancms.com"
paths:
  /v2/community/events/{eventId}/rsvps:
    post:
      summary: "Rsvp"
      operationId: "createRsvp"
      parameters:
        -
          description: "Target event id."
          name: "eventId"
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
                data: "RSVP_SUCCESS"
                meta:
                  timestamp: "2026-04-15T00:00:00.000Z"
                  path: "/v2/community/events/11111111-1111-1111-1111-111111111111/rsvps"
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
  --url "https://api.sonorancms.com/v2/community/events/11111111-1111-1111-1111-111111111111/rsvps" \
  --header "Authorization: Bearer YOUR_API_KEY" \
  --header "Accept: application/json" \
  --data '{"accId":"00000000-0000-0000-0000-000000000000"}'
```

{% endtab %}
{% endtabs %}

## Response

The `data` value is a toggle code. The service returns `RSVP_SUCCESS` when the account is added and `UNRSVP_SUCCESS` when the existing RSVP is removed.

```json
{
  "success": true,
  "data": "RSVP_SUCCESS",
  "meta": {
    "timestamp": "2026-04-15T00:00:00.000Z",
    "path": "/v2/community/events/11111111-1111-1111-1111-111111111111/rsvps"
  }
}
```
