---
description: Retrieve the ACE configuration for a server.
---

# Get ACE Config

<mark style="color:green;">`GET`</mark> `https://api.sonorancms.com/v2/community/servers/1/ace-config`

> **Rate limit:** `27 requests per minute`  
> Authenticated v2 endpoints are rate limited per credential rather than per IP address.

Retrieve the ACE configuration for a server.

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
  title: "Sonoran CMS v2 - Get Ace Config"
  version: "1.0.0"
  description: "Retrieve the ACE configuration for a server."
servers:
  -
    url: "https://api.sonorancms.com"
paths:
  /v2/community/servers/{serverId}/ace-config:
    get:
      summary: "Get Ace Config"
      operationId: "getAceConfig"
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
                    ranks:
                      - "22222222-2222-2222-2222-222222222222"
                    principal: "group:123456"
                meta:
                  timestamp: "2026-04-15T00:00:00.000Z"
                  path: "/v2/community/servers/1/ace-config"
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
  --url "https://api.sonorancms.com/v2/community/servers/1/ace-config" \
  --header "Authorization: Bearer YOUR_API_KEY" \
  --header "Accept: application/json"
```

{% endtab %}
{% endtabs %}

## Response

The `data` array contains ACE mapping objects for the requested server. The v2 service returns the flattened `mappings` array.

```json
{
  "success": true,
  "data": [
    {
      "ranks": [
        "22222222-2222-2222-2222-222222222222"
      ],
      "principal": "group:123456"
    }
  ],
  "meta": {
    "timestamp": "2026-04-15T00:00:00.000Z",
    "path": "/v2/community/servers/1/ace-config"
  }
}
```
