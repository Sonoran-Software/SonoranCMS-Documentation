---
description: Retrieve the configured promotion flows.
---

# Get Promotion Flows

<mark style="color:green;">`GET`</mark> `https://api.sonorancms.com/v2/community/promotion-flows`

> **Rate limit:** `13 requests per minute`  
> Authenticated v2 endpoints are rate limited per credential rather than per IP address.

Retrieve the configured promotion flows.

## Example Request

{% tabs %}
{% tab title="OpenAPI" %}

```yaml
openapi: "3.0.3"
info:
  title: "Sonoran CMS v2 - Get Promotion Flows"
  version: "1.0.0"
  description: "Retrieve the configured promotion flows."
servers:
  -
    url: "https://api.sonorancms.com"
paths:
  /v2/community/promotion-flows:
    get:
      summary: "Get Promotion Flows"
      operationId: "getPromotionFlows"
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
                    id: "44444444-4444-4444-4444-444444444444"
                    communityUuid: "00000000-0000-0000-0000-000000000000"
                    labelFrom: "Cadet"
                    labelTo: "Officer"
                    ranksToAdd:
                      - "22222222-2222-2222-2222-222222222222"
                    ranksToRemove: []
                    actions:
                      data: []
                      promotionType: "both"
                    promotionType: "both"
                meta:
                  timestamp: "2026-04-15T00:00:00.000Z"
                  path: "/v2/community/promotion-flows"
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
  --url "https://api.sonorancms.com/v2/community/promotion-flows" \
  --header "Authorization: Bearer YOUR_API_KEY" \
  --header "Accept: application/json"
```

{% endtab %}
{% endtabs %}

## Response

The `data` array contains promotion flow entities with the derived `promotionType` field added by the v2 service.

```json
{
  "success": true,
  "data": [
    {
      "id": "44444444-4444-4444-4444-444444444444",
      "communityUuid": "00000000-0000-0000-0000-000000000000",
      "labelFrom": "Cadet",
      "labelTo": "Officer",
      "ranksToAdd": [
        "22222222-2222-2222-2222-222222222222"
      ],
      "ranksToRemove": [],
      "actions": {
        "data": [],
        "promotionType": "both"
      },
      "promotionType": "both"
    }
  ],
  "meta": {
    "timestamp": "2026-04-15T00:00:00.000Z",
    "path": "/v2/community/promotion-flows"
  }
}
```
