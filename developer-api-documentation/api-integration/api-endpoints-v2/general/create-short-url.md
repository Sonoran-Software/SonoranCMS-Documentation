---
description: Create a short URL for the community.
---

# Create Short URL

<mark style="color:green;">`POST`</mark> `https://api.sonorancms.com/v2/community/short-urls`

> **Rate limit:** `13 requests per minute`  
> Authenticated v2 endpoints are rate limited per credential rather than per IP address.

Create a short URL for the community.

## Request Body

| Name | Type | Required | Description |
| --- | --- | --- | --- |
| `path` | string | Yes | See example request for the shape. |
| `isCustomDomain` | boolean | Yes | See example request for the shape. |

## Example Request

{% tabs %}
{% tab title="OpenAPI" %}

```yaml
openapi: "3.0.3"
info:
  title: "Sonoran CMS v2 - Create Short Url"
  version: "1.0.0"
  description: "Create a short URL for the community."
servers:
  -
    url: "https://api.sonorancms.com"
paths:
  /v2/community/short-urls:
    post:
      summary: "Create Short Url"
      operationId: "createShortUrl"
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
        "201":
          description: "Successful response"
          content:
            application/json:
              schema:
                type: "object"
              example:
                success: true
                data:
                  success: true
                  redirect: "https://sonorancms.com/dashboard"
                meta:
                  timestamp: "2026-04-15T00:00:00.000Z"
                  path: "/v2/community/short-urls"
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
  --url "https://api.sonorancms.com/v2/community/short-urls" \
  --header "Authorization: Bearer YOUR_API_KEY" \
  --header "Accept: application/json" \
  --data '{"path":"/go/example","isCustomDomain":false}'
```

{% endtab %}
{% endtabs %}

## Response

The `data` object is the nested short-url lookup result. On success it contains `success: true` and the resolved `redirect` URL.

```json
{
  "success": true,
  "data": {
    "success": true,
    "redirect": "https://sonorancms.com/dashboard"
  },
  "meta": {
    "timestamp": "2026-04-15T00:00:00.000Z",
    "path": "/v2/community/short-urls"
  }
}
```
