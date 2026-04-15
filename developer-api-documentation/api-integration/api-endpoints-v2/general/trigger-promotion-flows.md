---
description: Trigger one or more promotion flow actions.
---

# Trigger Promotion Flows

<mark style="color:green;">`POST`</mark> `https://api.sonorancms.com/v2/community/promotion-flows/trigger`

> **Rate limit:** `13 requests per minute`  
> Authenticated v2 endpoints are rate limited per credential rather than per IP address.

Trigger one or more promotion flow actions.

## Request Body

| Name | Type | Required | Description |
| --- | --- | --- | --- |
| `data` | array | Yes | See example request for the shape. |

## Example Request

{% tabs %}
{% tab title="OpenAPI" %}

```yaml
openapi: "3.0.3"
info:
  title: "Sonoran CMS v2 - Trigger Promotion Flows"
  version: "1.0.0"
  description: "Trigger one or more promotion flow actions."
servers:
  -
    url: "https://api.sonorancms.com"
paths:
  /v2/community/promotion-flows/trigger:
    post:
      summary: "Trigger Promotion Flows"
      operationId: "triggerPromotionFlows"
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
                    users:
                      - "00000000-0000-0000-0000-000000000000"
                    flow: "44444444-4444-4444-4444-444444444444"
                    promote: true
                    succeeded: true
                    message: "Promotion executed successfully"
                    config:
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
                  path: "/v2/community/promotion-flows/trigger"
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
  --url "https://api.sonorancms.com/v2/community/promotion-flows/trigger" \
  --header "Authorization: Bearer YOUR_API_KEY" \
  --header "Accept: application/json" \
  --data '{"data":[{"flowId":"flow-1","users":["ExampleUser"],"promote":true}]}'
```

{% endtab %}
{% endtabs %}

## Response

The `data` array contains one result object per flow/user combination. Each entry includes the users involved, the flow id, whether it was a promotion or demotion, the execution result, and the resolved flow config.

```json
{
  "success": true,
  "data": [
    {
      "users": [
        "00000000-0000-0000-0000-000000000000"
      ],
      "flow": "44444444-4444-4444-4444-444444444444",
      "promote": true,
      "succeeded": true,
      "message": "Promotion executed successfully",
      "config": {
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
    }
  ],
  "meta": {
    "timestamp": "2026-04-15T00:00:00.000Z",
    "path": "/v2/community/promotion-flows/trigger"
  }
}
```
