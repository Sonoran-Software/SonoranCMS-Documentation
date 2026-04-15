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
{% tab title="Sonoran.lua" %}

```lua
local response = sonoran:request({
  "method": "POST",
  "path": "/v2/community/short-urls",
  "body": {
    "path": "/go/example",
    "isCustomDomain": false
  }
})
```

{% endtab %}
{% tab title="Sonoran.js" %}

```javascript
const response = await sonoran.request({
  "method": "POST",
  "path": "/v2/community/short-urls",
  "body": {
    "path": "/go/example",
    "isCustomDomain": false
  }
});
```

{% endtab %}
{% tab title="Sonoran.py" %}

```python
response = sonoran.request({
  "method": "POST",
  "path": "/v2/community/short-urls",
  "body": {
    "path": "/go/example",
    "isCustomDomain": false
  }
})
```

{% endtab %}
{% tab title="Sonoran.Net" %}

```csharp
var response = await sonoran.RequestAsync(new SonoranRequest
{
    {
      "method": "POST",
      "path": "/v2/community/short-urls",
      "body": {
        "path": "/go/example",
        "isCustomDomain": false
      }
    }
});
```

{% endtab %}
{% tab title="OpenAPI" %}

```yaml
post:
  summary: Create Short URL
  security:
    - v2ApiKey: []
  requestBody:
    required: true
    content:
      application/json:
        schema:
          type: object
  responses:
    '201':
      description: Created
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

Successful requests return `application/json` and use the standard v2 envelope.

```json
{
  "success": true,
  "data": {
    "path": "/go/example",
    "shortUrl": "https://api.sonorancms.com/go/example",
    "isCustomDomain": false
  },
  "meta": {
    "timestamp": "2026-04-14T00:00:00.000Z",
    "path": "/v2/community/short-urls"
  }
}
```
