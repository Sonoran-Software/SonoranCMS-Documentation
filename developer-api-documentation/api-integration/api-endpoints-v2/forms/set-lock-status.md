---
description: Update the lock status for a form template.
---

# Set Form Lock Status

<mark style="color:green;">`PATCH`</mark> `https://api.sonorancms.com/v2/community/forms/1/lock`

> **Rate limit:** `18 requests per minute`  
> Authenticated v2 endpoints are rate limited per credential rather than per IP address.

Update the lock status for a form template.

## Route Parameters

| Name | Type | Required | Description |
| --- | --- | --- | --- |
| `templateId` | number | Yes | Target templateId. |

## Request Body

| Name | Type | Required | Description |
| --- | --- | --- | --- |
| `state` | boolean | Yes | See example request for the shape. |

## Example Request

{% tabs %}
{% tab title="Sonoran.lua" %}

```lua
local response = sonoran:request({
  "method": "PATCH",
  "path": "/v2/community/forms/1/lock",
  "body": {
    "state": true
  }
})
```

{% endtab %}
{% tab title="Sonoran.js" %}

```javascript
const response = await sonoran.request({
  "method": "PATCH",
  "path": "/v2/community/forms/1/lock",
  "body": {
    "state": true
  }
});
```

{% endtab %}
{% tab title="Sonoran.py" %}

```python
response = sonoran.request({
  "method": "PATCH",
  "path": "/v2/community/forms/1/lock",
  "body": {
    "state": true
  }
})
```

{% endtab %}
{% tab title="Sonoran.Net" %}

```csharp
var response = await sonoran.RequestAsync(new SonoranRequest
{
    {
      "method": "PATCH",
      "path": "/v2/community/forms/1/lock",
      "body": {
        "state": true
      }
    }
});
```

{% endtab %}
{% tab title="OpenAPI" %}

```yaml
patch:
  summary: Set Form Lock Status
  security:
    - v2ApiKey: []
  parameters:
    - name: templateId
      in: path
      required: true
      schema:
        type: integer
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
curl --request PATCH \
  --url "https://api.sonorancms.com/v2/community/forms/1/lock" \
  --header "Authorization: Bearer YOUR_API_KEY" \
  --header "Accept: application/json" \
  --data '{"state":true}'
```

{% endtab %}
{% endtabs %}

## Response

Successful requests return `application/json` and use the standard v2 envelope.

```json
{
  "success": true,
  "data": {
    "templateId": 1,
    "state": true
  },
  "meta": {
    "timestamp": "2026-04-14T00:00:00.000Z",
    "path": "/v2/community/forms/1/lock"
  }
}
```
