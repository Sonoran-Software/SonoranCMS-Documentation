---
description: Retrieve the ER:LC queue.
---

# Get Player Queue

<mark style="color:green;">`GET`</mark> `https://api.sonorancms.com/v2/community/erlc/players/queue`

> **Rate limit:** `27 requests per minute`  
> Authenticated v2 endpoints are rate limited per credential rather than per IP address.

Retrieve the ER:LC queue.

## Query Parameters

| Name | Type | Required | Description |
| --- | --- | --- | --- |
| `robloxJoinCode` | string | Yes | See example request for the shape. |

## Example Request

{% tabs %}
{% tab title="Sonoran.lua" %}

```lua
local response = sonoran:request({
  "method": "GET",
  "path": "/v2/community/erlc/players/queue",
  "query": {
    "robloxJoinCode": "ABC123"
  }
})
```

{% endtab %}
{% tab title="Sonoran.js" %}

```javascript
const response = await sonoran.request({
  "method": "GET",
  "path": "/v2/community/erlc/players/queue",
  "query": {
    "robloxJoinCode": "ABC123"
  }
});
```

{% endtab %}
{% tab title="Sonoran.py" %}

```python
response = sonoran.request({
  "method": "GET",
  "path": "/v2/community/erlc/players/queue",
  "query": {
    "robloxJoinCode": "ABC123"
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
      "path": "/v2/community/erlc/players/queue",
      "query": {
        "robloxJoinCode": "ABC123"
      }
    }
});
```

{% endtab %}
{% tab title="OpenAPI" %}

```yaml
get:
  summary: Get Player Queue
  security:
    - v2ApiKey: []
  parameters:
    - name: robloxJoinCode
      in: query
      required: false
      schema:
        type: string
  responses:
    '200':
      description: Successful response
```

{% endtab %}
{% tab title="cURL" %}

```bash
curl --request GET \
  --url "https://api.sonorancms.com/v2/community/erlc/players/queue?robloxJoinCode=ABC123" \
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
  "data": [
    {
      "playerName": "ExamplePlayer",
      "userId": "1234567890",
      "joinCode": "ABC123"
    }
  ],
  "meta": {
    "timestamp": "2026-04-14T00:00:00.000Z",
    "path": "/v2/community/erlc/players/queue"
  }
}
```
