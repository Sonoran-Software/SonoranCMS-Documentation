---
description: Retrieve the contents of a roster.
---

# Get Roster Contents

<mark style="color:green;">`GET`</mark> `https://api.sonorancms.com/v2/community/rosters/1`

> **Rate limit:** `9 requests per minute`  
> Authenticated v2 endpoints are rate limited per credential rather than per IP address.

Retrieve the contents of a roster.

## Route Parameters

| Name | Type | Required | Description |
| --- | --- | --- | --- |
| `rosterId` | number | Yes | Target rosterId. |

## Query Parameters

| Name | Type | Required | Description |
| --- | --- | --- | --- |
| `skip` | number | Yes | See example request for the shape. |
| `limit` | number | Yes | See example request for the shape. |

## Example Request

{% tabs %}
{% tab title="Sonoran.lua" %}

```lua
local response = sonoran:request({
  "method": "GET",
  "path": "/v2/community/rosters/1",
  "query": {
    "skip": 0,
    "limit": 25
  }
})
```

{% endtab %}
{% tab title="Sonoran.js" %}

```javascript
const response = await sonoran.request({
  "method": "GET",
  "path": "/v2/community/rosters/1",
  "query": {
    "skip": 0,
    "limit": 25
  }
});
```

{% endtab %}
{% tab title="Sonoran.py" %}

```python
response = sonoran.request({
  "method": "GET",
  "path": "/v2/community/rosters/1",
  "query": {
    "skip": 0,
    "limit": 25
  }
})
```

{% endtab %}
{% tab title="Sonoran.Net" %}

```csharp
var response = await sonoran.RequestAsync(new SonoranRequest
{
    {
      "method": "GET",
      "path": "/v2/community/rosters/1",
      "query": {
        "skip": 0,
        "limit": 25
      }
    }
});
```

{% endtab %}
{% tab title="OpenAPI" %}

```yaml
get:
  summary: Get Roster Contents
  security:
    - v2ApiKey: []
  parameters:
    - name: rosterId
      in: path
      required: true
      schema:
        type: integer
  parameters:
    - name: skip
      in: query
      required: false
      schema:
        type: integer
    - name: limit
      in: query
      required: false
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
  --url "https://api.sonorancms.com/v2/community/rosters/1?skip=0&limit=25" \
  --header "Authorization: Bearer YOUR_API_KEY" \
  --header "Accept: application/json"
```

{% endtab %}
{% endtabs %}

## Response

The `data` object includes the paginated roster rows, paging metadata, and the roster column definitions that were used to shape the rows. Row keys are dynamic and follow the roster template.

```json
{
  "success": true,
  "data": {
    "rows": [
      {
        "uuid": "55555555-5555-5555-5555-555555555555",
        "sortPower": 10,
        "name": "ExampleAccount",
        "rank": "Cadet"
      }
    ],
    "total": 1,
    "skip": 0,
    "limit": 25,
    "columns": [
      {
        "field": "name",
        "type": "text",
        "mask": "",
        "reverseMask": false,
        "label": "Name",
        "options": [],
        "metadata": {},
        "cosmetic": {
          "font": null,
          "textColor": null,
          "color": null,
          "align": null
        },
        "style": {}
      }
    ]
  },
  "meta": {
    "timestamp": "2026-04-15T00:00:00.000Z",
    "path": "/v2/community/rosters/1"
  }
}
```
