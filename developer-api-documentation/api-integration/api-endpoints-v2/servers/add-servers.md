---
description: Append one or more servers to the configuration.
---

# Add Servers

<mark style="color:green;">`POST`</mark> `https://api.sonorancms.com/v2/community/servers`

> **Rate limit:** `9 requests per minute`  
> Authenticated v2 endpoints are rate limited per credential rather than per IP address.

Append one or more servers to the configuration.

## Request Body

| Name | Type | Required | Description |
| --- | --- | --- | --- |
| `servers` | array | Yes | See example request for the shape. |

## Example Request

{% tabs %}
{% tab title="OpenAPI" %}

```yaml
openapi: "3.0.3"
info:
  title: "Sonoran CMS v2 - Add Servers"
  version: "1.0.0"
  description: "Append one or more servers to the configuration."
servers:
  -
    url: "https://api.sonorancms.com"
paths:
  /v2/community/servers:
    post:
      summary: "Add Servers"
      operationId: "addServers"
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
curl --request POST \
  --url "https://api.sonorancms.com/v2/community/servers" \
  --header "Authorization: Bearer YOUR_API_KEY" \
  --header "Accept: application/json" \
  --data '{"servers":[{"id":1,"name":"Main Server","description":"Primary community server","ip":"127.0.0.1","port":"30120","type":"FiveM","erlcApiKey":"","robloxJoinCode":"ABC123","aceConfig":{},"robloxMetadata":{}}]}'
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
