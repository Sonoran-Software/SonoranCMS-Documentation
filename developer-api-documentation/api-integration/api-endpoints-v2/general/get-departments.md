---
description: Retrieve the community departments.
---

# Get Departments

<mark style="color:green;">`GET`</mark> `https://api.sonorancms.com/v2/community/departments`

> **Rate limit:** `13 requests per minute`  
> Authenticated v2 endpoints are rate limited per credential rather than per IP address.

Retrieve the community departments.

## Example Request

{% tabs %}
{% tab title="OpenAPI" %}

```yaml
openapi: "3.0.3"
info:
  title: "Sonoran CMS v2 - Get Departments"
  version: "1.0.0"
  description: "Retrieve the community departments."
servers:
  -
    url: "https://api.sonorancms.com"
paths:
  /v2/community/departments:
    get:
      summary: "Get Departments"
      operationId: "getDepartments"
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
                    uuid: "11111111-1111-1111-1111-111111111111"
                    label: "Police Department"
                    labelTwo: "Police"
                    ranks:
                      -
                        id: "22222222-2222-2222-2222-222222222222"
                        label: "Cadet"
                        primaryOnly: true
                        secondaryOnly: false
                        power: 10
                meta:
                  timestamp: "2026-04-15T00:00:00.000Z"
                  path: "/v2/community/departments"
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
  --url "https://api.sonorancms.com/v2/community/departments" \
  --header "Authorization: Bearer YOUR_API_KEY" \
  --header "Accept: application/json"
```

{% endtab %}
{% endtabs %}

## Response

The `data` array is the community department list. Each department includes its label pair and the ranks nested beneath it.

```json
{
  "success": true,
  "data": [
    {
      "uuid": "11111111-1111-1111-1111-111111111111",
      "label": "Police Department",
      "labelTwo": "Police",
      "ranks": [
        {
          "id": "22222222-2222-2222-2222-222222222222",
          "label": "Cadet",
          "primaryOnly": true,
          "secondaryOnly": false,
          "power": 10
        }
      ]
    }
  ],
  "meta": {
    "timestamp": "2026-04-15T00:00:00.000Z",
    "path": "/v2/community/departments"
  }
}
```
