---
description: Retrieve the community departments.
---

# Get Departments

<mark style="color:green;">`GET`</mark> `https://api.sonorancms.com/v2/community/departments`

> **Rate limit:** `13 requests per minute`  
> Authenticated v2 endpoints are rate limited per credential rather than per IP address.

Retrieve the community departments.

## Example Request

{% tabs %}
{% tab title="Sonoran.lua" %}

```lua
local response = sonoran:request({
  "method": "GET",
  "path": "/v2/community/departments"
})
```

{% endtab %}
{% tab title="Sonoran.js" %}

```javascript
const response = await sonoran.request({
  "method": "GET",
  "path": "/v2/community/departments"
});
```

{% endtab %}
{% tab title="Sonoran.py" %}

```python
response = sonoran.request({
  "method": "GET",
  "path": "/v2/community/departments"
})
```

{% endtab %}
{% tab title="Sonoran.Net" %}

```csharp
var response = await sonoran.RequestAsync(new SonoranRequest
{
    {
      "method": "GET",
      "path": "/v2/community/departments"
    }
});
```

{% endtab %}
{% tab title="OpenAPI" %}

```yaml
get:
  summary: Get Departments
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
  --url "https://api.sonorancms.com/v2/community/departments" \
  --header "Authorization: Bearer YOUR_API_KEY" \
  --header "Accept: application/json"
```

{% endtab %}
{% endtabs %}

## Response

The `data` array is the community department list. Each department includes its label pair and the ranks nested beneath it.

```json
{
  "success": true,
  "data": [
    {
      "uuid": "11111111-1111-1111-1111-111111111111",
      "label": "Police Department",
      "labelTwo": "Police",
      "ranks": [
        {
          "id": "22222222-2222-2222-2222-222222222222",
          "label": "Cadet",
          "primaryOnly": true,
          "secondaryOnly": false,
          "power": 10
        }
      ]
    }
  ],
  "meta": {
    "timestamp": "2026-04-15T00:00:00.000Z",
    "path": "/v2/community/departments"
  }
}
```
