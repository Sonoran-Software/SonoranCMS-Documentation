---
description: Execute an ER:LC command.
---

# Execute Command

<mark style="color:green;">`POST`</mark> `https://api.sonorancms.com/v2/community/erlc/commands`

> **Rate limit:** `18 requests per minute`  
> Authenticated v2 endpoints are rate limited per credential rather than per IP address.

Execute an ER:LC command.

## Request Body

| Name | Type | Required | Description |
| --- | --- | --- | --- |
| `robloxJoinCode` | string | Yes | See example request for the shape. |
| `discordId` | string | Yes | See example request for the shape. |
| `type` | string | Yes | See example request for the shape. |
| `args` | string | Yes | See example request for the shape. |
| `includesPlayerNameOrId` | boolean | Yes | See example request for the shape. |

## Example Request

{% tabs %}
{% tab title="OpenAPI" %}

```yaml
openapi: "3.0.3"
info:
  title: "Sonoran CMS v2 - Execute Command"
  version: "1.0.0"
  description: "Execute an ER:LC command."
servers:
  -
    url: "https://api.sonorancms.com"
paths:
  /v2/community/erlc/commands:
    post:
      summary: "Execute Command"
      operationId: "executeErlcCommand"
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
                data: "Successfully added command to queue"
                meta:
                  timestamp: "2026-04-15T00:00:00.000Z"
                  path: "/v2/community/erlc/commands"
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
  --url "https://api.sonorancms.com/v2/community/erlc/commands" \
  --header "Authorization: Bearer YOUR_API_KEY" \
  --header "Accept: application/json" \
  --data '{"robloxJoinCode":"ABC123","discordId":"1234567890","type":"announce","args":"Server restart in 10 minutes","includesPlayerNameOrId":false}'
```

{% endtab %}
{% endtabs %}

## Response

The `data` value is a confirmation string once the command has been queued for ERLC execution.

```json
{
  "success": true,
  "data": "Successfully added command to queue",
  "meta": {
    "timestamp": "2026-04-15T00:00:00.000Z",
    "path": "/v2/community/erlc/commands"
  }
}
```
