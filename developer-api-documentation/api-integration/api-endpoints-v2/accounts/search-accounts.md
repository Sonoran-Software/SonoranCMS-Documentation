---
description: Search for community accounts.
---

# Search Accounts

<mark style="color:green;">`GET`</mark> `https://api.sonorancms.com/v2/community/accounts/search`

> **Rate limit:** `27 requests per minute`  
> Authenticated v2 endpoints are rate limited per credential rather than per IP address.

Search for community accounts.

## Query Parameters

| Name | Type | Required | Description |
| --- | --- | --- | --- |
| `username` | string | Yes | See example request for the shape. |

## Example Request

{% tabs %}
{% tab title="OpenAPI" %}

```yaml
openapi: "3.0.3"
info:
  title: "Sonoran CMS v2 - Search Accounts"
  version: "1.0.0"
  description: "Search for community accounts."
servers:
  -
    url: "https://api.sonorancms.com"
paths:
  /v2/community/accounts/search:
    get:
      summary: "Search Accounts"
      operationId: "searchAccounts"
      parameters:
        -
          description: "Target account UUID. Provide exactly one identifier."
          name: "accountId"
          in: "query"
          schema:
            type: "string"
            format: "uuid"
          required: false
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
          description: "Target community account id. Provide exactly one identifier."
          name: "accId"
          in: "query"
          schema:
            type: "string"
            format: "uuid"
          required: false
        -
          description: "Target Discord id. Provide exactly one identifier."
          name: "discord"
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
                  items:
                    -
                      accId: "00000000-0000-0000-0000-000000000000"
                      uniqueId: 1001
                      accName: "ExampleAccount"
                      comName: "Example Community"
                      activeApiIds:
                        - "discord:1234567890"
                      discordId: "1234567890"
                      sysStatus: true
                      comStatus: true
                      archived: false
                      banned: false
                      teamspeakId: null
                  total: 1
                meta:
                  timestamp: "2026-04-15T00:00:00.000Z"
                  path: "/v2/community/accounts/search"
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
  --url "https://api.sonorancms.com/v2/community/accounts/search?username=ExampleUser" \
  --header "Authorization: Bearer YOUR_API_KEY" \
  --header "Accept: application/json"
```

{% endtab %}
{% endtabs %}

## Response

The `data` object contains the matched accounts and a `total` count. This search endpoint does not page the result set beyond the service-level filters.

```json
{
  "success": true,
  "data": {
    "items": [
      {
        "accId": "00000000-0000-0000-0000-000000000000",
        "uniqueId": 1001,
        "accName": "ExampleAccount",
        "comName": "Example Community",
        "activeApiIds": [
          "discord:1234567890"
        ],
        "discordId": "1234567890",
        "sysStatus": true,
        "comStatus": true,
        "archived": false,
        "banned": false,
        "teamspeakId": null
      }
    ],
    "total": 1
  },
  "meta": {
    "timestamp": "2026-04-15T00:00:00.000Z",
    "path": "/v2/community/accounts/search"
  }
}
```
