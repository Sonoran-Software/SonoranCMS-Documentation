---
description: Retrieve the online ER:LC players.
---

# Get Online Players

<mark style="color:green;">`GET`</mark> `https://api.sonorancms.com/v2/community/erlc/players/online`

> **Rate limit:** `27 requests per minute`  
> Authenticated v2 endpoints are rate limited per credential rather than per IP address.

Retrieve the online ER:LC players.

## Query Parameters

| Name | Type | Required | Description |
| --- | --- | --- | --- |
| `robloxJoinCode` | string | Yes | See example request for the shape. |

## Example Request

{% tabs %}
{% tab title="OpenAPI" %}

```yaml
openapi: "3.0.3"
info:
  title: "Sonoran CMS v2 - Get Online Players"
  version: "1.0.0"
  description: "Retrieve the online ER:LC players."
servers:
  -
    url: "https://api.sonorancms.com"
paths:
  /v2/community/erlc/players/online:
    get:
      summary: "Get Online Players"
      operationId: "getOnlinePlayers"
      parameters:
        -
          description: "Target Roblox join code."
          name: "robloxJoinCode"
          in: "query"
          schema:
            type: "string"
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
                  -
                    Player: "ExamplePlayer:123456789"
                    Permission: "Normal"
                    Callsign: ""
                    Team: "Civilian"
                    Actioned: null
                    Location:
                      LocationX: 0
                      LocationY: 0
                      LocationZ: 0
                meta:
                  timestamp: "2026-04-15T00:00:00.000Z"
                  path: "/v2/community/erlc/players/online"
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
  --url "https://api.sonorancms.com/v2/community/erlc/players/online?robloxJoinCode=ABC123" \
  --header "Authorization: Bearer YOUR_API_KEY" \
  --header "Accept: application/json"
```

{% endtab %}
{% endtabs %}

## Response

The `data` array contains the ERLC player projection rows returned by the hub cache. Each item follows the panel player shape.

```json
{
  "success": true,
  "data": [
    {
      "Player": "ExamplePlayer:123456789",
      "Permission": "Normal",
      "Callsign": "",
      "Team": "Civilian",
      "Actioned": null,
      "Location": {
        "LocationX": 0,
        "LocationY": 0,
        "LocationZ": 0
      }
    }
  ],
  "meta": {
    "timestamp": "2026-04-15T00:00:00.000Z",
    "path": "/v2/community/erlc/players/online"
  }
}
```
