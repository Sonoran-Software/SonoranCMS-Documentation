---
description: Retrieve the lock status for a form template.
---

# Get Form Lock Status

<mark style="color:green;">`GET`</mark> `https://api.sonorancms.com/v2/community/forms/1/lock`

> **Rate limit:** `27 requests per minute`  
> Authenticated v2 endpoints are rate limited per credential rather than per IP address.

Retrieve the lock status for a form template.

## Route Parameters

| Name | Type | Required | Description |
| --- | --- | --- | --- |
| `templateId` | number | Yes | Target templateId. |

## Example Request

{% tabs %}
{% tab title="Sonoran.lua" %}

```lua
local response = sonoran:request({
  "method": "GET",
  "path": "/v2/community/forms/1/lock"
})
```

{% endtab %}
{% tab title="Sonoran.js" %}

```javascript
const response = await sonoran.request({
  "method": "GET",
  "path": "/v2/community/forms/1/lock"
});
```

{% endtab %}
{% tab title="Sonoran.py" %}

```python
response = sonoran.request({
  "method": "GET",
  "path": "/v2/community/forms/1/lock"
})
```

{% endtab %}
{% tab title="Sonoran.Net" %}

```csharp
var response = await sonoran.RequestAsync(new SonoranRequest
{
    {
      "method": "GET",
      "path": "/v2/community/forms/1/lock"
    }
});
```

{% endtab %}
{% tab title="OpenAPI" %}

```yaml
get:
  summary: Get Form Lock Status
  security:
    - v2ApiKey: []
  parameters:
    - name: templateId
      in: path
      required: true
      schema:
        type: integer
  responses:
    '200':
      description: Successful response
```

{% endtab %}
{% tab title="cURL" %}

```bash
curl --request GET \
  --url "https://api.sonorancms.com/v2/community/forms/1/lock" \
  --header "Authorization: Bearer YOUR_API_KEY" \
  --header "Accept: application/json"
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
