---
description: Cancel an active session.
---

# Cancel Session

<mark style="color:green;">`DELETE`</mark> `https://api.sonorancms.com/v2/community/sessions`

> **Rate limit:** `9 requests per minute`  
> Authenticated v2 endpoints are rate limited per credential rather than per IP address.

Cancel an active session.

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
  "method": "DELETE",
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
  "method": "DELETE",
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
  "method": "DELETE",
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
      "method": "DELETE",
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
delete:
  summary: Cancel Session
  security:
    - v2ApiKey: []
  requestBody:
    required: true
    content:
      application/json:
        schema:
          type: object
  responses:
    '204':
      description: No Content
```

{% endtab %}
{% tab title="cURL" %}

```bash
curl --request DELETE \
  --url "https://api.sonorancms.com/v2/community/sessions" \
  --header "Authorization: Bearer YOUR_API_KEY" \
  --header "Accept: application/json" \
  --data '{"serverId":1,"accId":"00000000-0000-0000-0000-000000000000"}'
```

{% endtab %}
{% endtabs %}

## Response

This endpoint returns `204 No Content` with no JSON body.
