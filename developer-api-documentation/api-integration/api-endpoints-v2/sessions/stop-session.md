---
description: Stop an active session.
---

# Stop Session

<mark style="color:green;">`PATCH`</mark> `https://api.sonorancms.com/v2/community/sessions`

> **Rate limit:** `27 requests per minute`  
> Authenticated v2 endpoints are rate limited per credential rather than per IP address.

Stop an active session.

## Request Body

| Name | Type | Required | Description |
| --- | --- | --- | --- |
| `serverId` | number | Yes | See example request for the shape. |
| `accId` | string | Yes | See example request for the shape. |

## Example Request

{% tabs %}
{% tab title="Sonoran.lua" %}

```lua
local response = sonoran:request({
  "method": "PATCH",
  "path": "/v2/community/sessions",
  "body": {
    "serverId": 1,
    "accId": "00000000-0000-0000-0000-000000000000"
  }
})
```

{% endtab %}
{% tab title="Sonoran.js" %}

```javascript
const response = await sonoran.request({
  "method": "PATCH",
  "path": "/v2/community/sessions",
  "body": {
    "serverId": 1,
    "accId": "00000000-0000-0000-0000-000000000000"
  }
});
```

{% endtab %}
{% tab title="Sonoran.py" %}

```python
response = sonoran.request({
  "method": "PATCH",
  "path": "/v2/community/sessions",
  "body": {
    "serverId": 1,
    "accId": "00000000-0000-0000-0000-000000000000"
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
      "path": "/v2/community/sessions",
      "body": {
        "serverId": 1,
        "accId": "00000000-0000-0000-0000-000000000000"
      }
    }
});
```

{% endtab %}
{% tab title="OpenAPI" %}

```yaml
patch:
  summary: Stop Session
  security:
    - v2ApiKey: []
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
  --url "https://api.sonorancms.com/v2/community/sessions" \
  --header "Authorization: Bearer YOUR_API_KEY" \
  --header "Accept: application/json" \
  --data '{"serverId":1,"accId":"00000000-0000-0000-0000-000000000000"}'
```

{% endtab %}
{% endtabs %}

## Response

Successful requests return `application/json` and use the standard v2 envelope.

```json
{
  "success": true,
  "data": {
    "serverId": 1,
    "accId": "00000000-0000-0000-0000-000000000000",
    "active": true,
    "startedAt": "2026-04-14T00:00:00.000Z",
    "stoppedAt": null
  },
  "meta": {
    "timestamp": "2026-04-14T00:00:00.000Z",
    "path": "/v2/community/sessions"
  }
}
```
