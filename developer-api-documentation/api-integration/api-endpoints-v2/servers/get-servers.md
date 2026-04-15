---
description: Retrieve the configured servers.
---

# Get Servers

<mark style="color:green;">`GET`</mark> `https://api.sonorancms.com/v2/community/servers`

> **Rate limit:** `13 requests per minute`  
> Authenticated v2 endpoints are rate limited per credential rather than per IP address.

Retrieve the configured servers.

## Example Request

{% tabs %}
{% tab title="OpenAPI" %}

```yaml
openapi: "3.0.3"
info:
  title: "Sonoran CMS v2 - Get Servers"
  version: "1.0.0"
  description: "Retrieve the configured servers."
servers:
  -
    url: "https://api.sonorancms.com"
paths:
  /v2/community/servers:
    get:
      summary: "Get Servers"
      operationId: "getServers"
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
                  servers:
                    -
                      id: 1
                      name: "Main Server"
                      description: "Primary gameplay server"
                      ip: "127.0.0.1"
                      port: "30120"
                      typeLastUpdated: "2026-04-15T00:00:00.000Z"
                      type: "erlc"
                      robloxJoinCode: "ABCD-1234"
                      aceConfig:
                        mappings:
                          -
                            ranks:
                              - "22222222-2222-2222-2222-222222222222"
                            principal: "group:123456"
                meta:
                  timestamp: "2026-04-15T00:00:00.000Z"
                  path: "/v2/community/servers"
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
  --url "https://api.sonorancms.com/v2/community/servers" \
  --header "Authorization: Bearer YOUR_API_KEY" \
  --header "Accept: application/json"
```

{% endtab %}
{% endtabs %}

## Response

The `data` object is the community `servers` container. It exposes the server list the backend stores for the community.

```json
{
  "success": true,
  "data": {
    "servers": [
      {
        "id": 1,
        "name": "Main Server",
        "description": "Primary gameplay server",
        "ip": "127.0.0.1",
        "port": "30120",
        "typeLastUpdated": "2026-04-15T00:00:00.000Z",
        "type": "erlc",
        "robloxJoinCode": "ABCD-1234",
        "aceConfig": {
          "mappings": [
            {
              "ranks": [
                "22222222-2222-2222-2222-222222222222"
              ],
              "principal": "group:123456"
            }
          ]
        }
      }
    ]
  },
  "meta": {
    "timestamp": "2026-04-15T00:00:00.000Z",
    "path": "/v2/community/servers"
  }
}
```
