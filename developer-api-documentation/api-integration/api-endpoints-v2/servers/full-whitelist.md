---
description: Retrieve the full whitelist for a server.
---

# Full Whitelist

<mark style="color:green;">`GET`</mark> `https://api.sonorancms.com/v2/community/servers/1/whitelist`

> **Rate limit:** `13 requests per minute`  
> Authenticated v2 endpoints are rate limited per credential rather than per IP address.

Retrieve the full whitelist for a server.

## Route Parameters

| Name | Type | Required | Description |
| --- | --- | --- | --- |
| `serverId` | number | Yes | Target serverId. |

## Example Request

{% tabs %}
{% tab title="OpenAPI" %}

```yaml
openapi: "3.0.3"
info:
  title: "Sonoran CMS v2 - Full Whitelist"
  version: "1.0.0"
  description: "Retrieve the full whitelist for a server."
servers:
  -
    url: "https://api.sonorancms.com"
paths:
  /v2/community/servers/{serverId}/whitelist:
    get:
      summary: "Full Whitelist"
      operationId: "getFullWhitelist"
      parameters:
        -
          description: "Target server id."
          name: "serverId"
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
                data:
                  -
                    name: "ExampleAccount"
                    apiIds:
                      - "discord:1234567890"
                      - "roblox:987654321"
                meta:
                  timestamp: "2026-04-15T00:00:00.000Z"
                  path: "/v2/community/servers/1/whitelist"
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
  --url "https://api.sonorancms.com/v2/community/servers/1/whitelist" \
  --header "Authorization: Bearer YOUR_API_KEY" \
  --header "Accept: application/json"
```

{% endtab %}
{% endtabs %}

## Response

The `data` array contains the full whitelist entries, each with the community account name and the API identifiers that should be allowed into the server.

```json
{
  "success": true,
  "data": [
    {
      "name": "ExampleAccount",
      "apiIds": [
        "discord:1234567890",
        "roblox:987654321"
      ]
    }
  ],
  "meta": {
    "timestamp": "2026-04-15T00:00:00.000Z",
    "path": "/v2/community/servers/1/whitelist"
  }
}
```
