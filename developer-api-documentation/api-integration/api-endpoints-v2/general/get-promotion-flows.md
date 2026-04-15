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
{% tab title="Sonoran.lua" %}

```lua
local response = sonoran:request({
  "method": "GET",
  "path": "/v2/community/promotion-flows"
})
```

{% endtab %}
{% tab title="Sonoran.js" %}

```javascript
const response = await sonoran.request({
  "method": "GET",
  "path": "/v2/community/promotion-flows"
});
```

{% endtab %}
{% tab title="Sonoran.py" %}

```python
response = sonoran.request({
  "method": "GET",
  "path": "/v2/community/promotion-flows"
})
```

{% endtab %}
{% tab title="Sonoran.Net" %}

```csharp
var response = await sonoran.RequestAsync(new SonoranRequest
{
    {
      "method": "GET",
      "path": "/v2/community/promotion-flows"
    }
});
```

{% endtab %}
{% tab title="OpenAPI" %}

```yaml
get:
  summary: Get Promotion Flows
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
