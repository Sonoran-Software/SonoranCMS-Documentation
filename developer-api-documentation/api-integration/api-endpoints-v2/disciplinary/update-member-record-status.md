---
description: Update the status of a disciplinary record.
---

# Update Member Record Status

<mark style="color:green;">`PATCH`</mark> `https://api.sonorancms.com/v2/community/disciplinary/records/11111111-1111-1111-1111-111111111111/status`

> **Rate limit:** `18 requests per minute`  
> Authenticated v2 endpoints are rate limited per credential rather than per IP address.

Update the status of a disciplinary record.

## Route Parameters

| Name | Type | Required | Description |
| --- | --- | --- | --- |
| `recordId` | string (uuid) | Yes | Target recordId. |

## Request Body

| Name | Type | Required | Description |
| --- | --- | --- | --- |
| `status` | boolean | Yes | See example request for the shape. |

## Example Request

{% tabs %}
{% tab title="OpenAPI" %}

```yaml
openapi: "3.0.3"
info:
  title: "Sonoran CMS v2 - Update Member Record Status"
  version: "1.0.0"
  description: "Update the status of a disciplinary record."
servers:
  -
    url: "https://api.sonorancms.com"
paths:
  /v2/community/disciplinary/records/{recordId}/status:
    patch:
      summary: "Update Member Record Status"
      operationId: "updateMemberRecordStatus"
      parameters:
        -
          description: "Target disciplinary record id."
          name: "recordId"
          in: "path"
          schema:
            type: "string"
            format: "uuid"
          required: true
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
                  -
                    id: "55555555-5555-5555-5555-555555555555"
                    status: true
                    accId: "00000000-0000-0000-0000-000000000000"
                    source: "api"
                    sourceId: "api-request"
                    points: 5
                    reason: "Example disciplinary action"
                    metadata:
                      executionSource: "discord"
                    history:
                      2026-04-15T00:00:00.000Z:
                        action: "init"
                        points: 5
                        reason: "Example disciplinary action"
                        metadata:
                          executionSource: "discord"
                        timestamp: "2026-04-15T00:00:00.000Z"
                        source: "api"
                        sourceId: "api-request"
                    createdAt: "2026-04-15T00:00:00.000Z"
                    updatedAt: null
                    expired: false
                meta:
                  timestamp: "2026-04-15T00:00:00.000Z"
                  path: "/v2/community/disciplinary/records/11111111-1111-1111-1111-111111111111/status"
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
curl --request PATCH \
  --url "https://api.sonorancms.com/v2/community/disciplinary/records/11111111-1111-1111-1111-111111111111/status" \
  --header "Authorization: Bearer YOUR_API_KEY" \
  --header "Accept: application/json" \
  --data '{"status":true}'
```

{% endtab %}
{% endtabs %}

## Response

The `data` array contains the updated disciplinary record row(s) returned by the update query. The endpoint is reused for points, reason, and status updates.

```json
{
  "success": true,
  "data": [
    {
      "id": "55555555-5555-5555-5555-555555555555",
      "status": true,
      "accId": "00000000-0000-0000-0000-000000000000",
      "source": "api",
      "sourceId": "api-request",
      "points": 5,
      "reason": "Example disciplinary action",
      "metadata": {
        "executionSource": "discord"
      },
      "history": {
        "2026-04-15T00:00:00.000Z": {
          "action": "init",
          "points": 5,
          "reason": "Example disciplinary action",
          "metadata": {
            "executionSource": "discord"
          },
          "timestamp": "2026-04-15T00:00:00.000Z",
          "source": "api",
          "sourceId": "api-request"
        }
      },
      "createdAt": "2026-04-15T00:00:00.000Z",
      "updatedAt": null,
      "expired": false
    }
  ],
  "meta": {
    "timestamp": "2026-04-15T00:00:00.000Z",
    "path": "/v2/community/disciplinary/records/11111111-1111-1111-1111-111111111111/status"
  }
}
```
