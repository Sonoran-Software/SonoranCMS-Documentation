---
description: Retrieve the current community summary.
---

# Get Community

<mark style="color:green;">`GET`</mark> `https://api.sonorancms.com/v2/community`

> **Rate limit:** `13 requests per minute`  
> Authenticated v2 endpoints are rate limited per credential rather than per IP address.

Retrieve the current community summary.

## Example Request

{% tabs %}
{% tab title="Sonoran.lua" %}

```lua
local response = sonoran:request({
  "method": "GET",
  "path": "/v2/community"
})
```

{% endtab %}
{% tab title="Sonoran.js" %}

```javascript
const response = await sonoran.request({
  "method": "GET",
  "path": "/v2/community"
});
```

{% endtab %}
{% tab title="Sonoran.py" %}

```python
response = sonoran.request({
  "method": "GET",
  "path": "/v2/community"
})
```

{% endtab %}
{% tab title="Sonoran.Net" %}

```csharp
var response = await sonoran.RequestAsync(new SonoranRequest
{
    {
      "method": "GET",
      "path": "/v2/community"
    }
});
```

{% endtab %}
{% tab title="OpenAPI" %}

```yaml
get:
  summary: Get Community
  security:
    - v2ApiKey: []
  responses:
    '200':
      description: Successful response
```

{% endtab %}
{% tab title="cURL" %}

```bash
curl --request GET \
  --url "https://api.sonorancms.com/v2/community" \
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
    "communityId": "YOUR_COMMUNITY_ID",
    "communityName": "Example Community",
    "subVersion": "pro",
    "departments": [],
    "profileFields": [],
    "clockinTypes": [],
    "customLogTypes": [],
    "promotionFlows": []
  },
  "meta": {
    "timestamp": "2026-04-14T00:00:00.000Z",
    "path": "/v2/community"
  }
}
```
