---
description: Undo a previously recorded rank change.
---

# Undo Rank Change

<mark style="color:green;">`POST`</mark> `https://api.sonorancms.com/v2/community/rank-changes/11111111-1111-1111-1111-111111111111/undo`

> **Rate limit:** `13 requests per minute`  
> Authenticated v2 endpoints are rate limited per credential rather than per IP address.

Undo a previously recorded rank change.

## Route Parameters

| Name | Type | Required | Description |
| --- | --- | --- | --- |
| `undoId` | string (uuid) | Yes | Target undoId. |

## Request Body

| Name | Type | Required | Description |
| --- | --- | --- | --- |
| `userId` | string | Yes | See example request for the shape. |

## Example Request

{% tabs %}
{% tab title="Sonoran.lua" %}

```lua
local response = sonoran:request({
  "method": "POST",
  "path": "/v2/community/rank-changes/11111111-1111-1111-1111-111111111111/undo",
  "body": {
    "userId": "11111111-1111-1111-1111-111111111111"
  }
})
```

{% endtab %}
{% tab title="Sonoran.js" %}

```javascript
const response = await sonoran.request({
  "method": "POST",
  "path": "/v2/community/rank-changes/11111111-1111-1111-1111-111111111111/undo",
  "body": {
    "userId": "11111111-1111-1111-1111-111111111111"
  }
});
```

{% endtab %}
{% tab title="Sonoran.py" %}

```python
response = sonoran.request({
  "method": "POST",
  "path": "/v2/community/rank-changes/11111111-1111-1111-1111-111111111111/undo",
  "body": {
    "userId": "11111111-1111-1111-1111-111111111111"
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
      "path": "/v2/community/rank-changes/11111111-1111-1111-1111-111111111111/undo",
      "body": {
        "userId": "11111111-1111-1111-1111-111111111111"
      }
    }
});
```

{% endtab %}
{% tab title="OpenAPI" %}

```yaml
post:
  summary: Undo Rank Change
  security:
    - v2ApiKey: []
  parameters:
    - name: undoId
      in: path
      required: true
      schema:
        type: string
        format: uuid
  requestBody:
    required: true
    content:
      application/json:
        schema:
          type: object
  responses:
    '200':
      description: Successful response
```

{% endtab %}
{% tab title="cURL" %}

```bash
curl --request POST \
  --url "https://api.sonorancms.com/v2/community/rank-changes/11111111-1111-1111-1111-111111111111/undo" \
  --header "Authorization: Bearer YOUR_API_KEY" \
  --header "Accept: application/json" \
  --data '{"userId":"11111111-1111-1111-1111-111111111111"}'
```

{% endtab %}
{% endtabs %}

## Response

Successful requests return `application/json` and use the standard v2 envelope.

```json
{
  "success": true,
  "data": {
    "undoId": "11111111-1111-1111-1111-111111111111",
    "userId": "11111111-1111-1111-1111-111111111111",
    "undone": true
  },
  "meta": {
    "timestamp": "2026-04-14T00:00:00.000Z",
    "path": "/v2/community/rank-changes/11111111-1111-1111-1111-111111111111/undo"
  }
}
```
