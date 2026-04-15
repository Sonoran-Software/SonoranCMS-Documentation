---
description: Retrieve the current session for a server.
---

# Get Current Session

<mark style="color:green;">`GET`</mark> `https://api.sonorancms.com/v2/community/sessions/current`

> **Rate limit:** `27 requests per minute`  
> Authenticated v2 endpoints are rate limited per credential rather than per IP address.

Retrieve the current session for a server.

## Query Parameters

| Name | Type | Required | Description |
| --- | --- | --- | --- |
| `serverId` | number | Yes | See example request for the shape. |

## Example Request

{% tabs %}
{% tab title="Sonoran.lua" %}

```lua
local response = sonoran:request({
  "method": "GET",
  "path": "/v2/community/sessions/current",
  "query": {
    "serverId": 1
  }
})
```

{% endtab %}
{% tab title="Sonoran.js" %}

```javascript
const response = await sonoran.request({
  "method": "GET",
  "path": "/v2/community/sessions/current",
  "query": {
    "serverId": 1
  }
});
```

{% endtab %}
{% tab title="Sonoran.py" %}

```python
response = sonoran.request({
  "method": "GET",
  "path": "/v2/community/sessions/current",
  "query": {
    "serverId": 1
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
      "path": "/v2/community/sessions/current",
      "query": {
        "serverId": 1
      }
    }
});
```

{% endtab %}
{% tab title="OpenAPI" %}

```yaml
get:
  summary: Get Current Session
  security:
    - v2ApiKey: []
  parameters:
    - name: serverId
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
  --url "https://api.sonorancms.com/v2/community/sessions/current?serverId=1" \
  --header "Authorization: Bearer YOUR_API_KEY" \
  --header "Accept: application/json"
```

{% endtab %}
{% endtabs %}

## Response

The `data` object is the session row. `GET`, `POST`, and `PATCH` all return the `CommunityServerSession` entity shape on success.

```json
{
  "success": true,
  "data": {
    "id": "55555555-5555-5555-5555-555555555555",
    "sysStatus": true,
    "community": "00000000-0000-0000-0000-000000000000",
    "serverId": 1,
    "startedBy": "00000000-0000-0000-0000-000000000000",
    "startedAt": "2026-04-15T00:00:00.000Z",
    "endedBy": null,
    "endedAt": null,
    "cancelledBy": null,
    "stats": {},
    "metadata": {}
  },
  "meta": {
    "timestamp": "2026-04-15T00:00:00.000Z",
    "path": "/v2/community/sessions/current"
  }
}
```
