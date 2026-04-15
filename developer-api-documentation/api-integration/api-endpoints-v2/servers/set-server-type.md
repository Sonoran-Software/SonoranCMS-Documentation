---
description: Update the server type.
---

# Set Server Type

<mark style="color:green;">`PATCH`</mark> `https://api.sonorancms.com/v2/community/servers/1/type`

> **Rate limit:** `18 requests per minute`  
> Authenticated v2 endpoints are rate limited per credential rather than per IP address.

Update the server type.

## Route Parameters

| Name | Type | Required | Description |
| --- | --- | --- | --- |
| `serverId` | number | Yes | Target serverId. |

## Request Body

| Name | Type | Required | Description |
| --- | --- | --- | --- |
| `type` | string | Yes | See example request for the shape. |

## Example Request

{% tabs %}
{% tab title="Sonoran.lua" %}

```lua
local response = sonoran:request({
  "method": "PATCH",
  "path": "/v2/community/servers/1/type",
  "body": {
    "type": "FiveM"
  }
})
```

{% endtab %}
{% tab title="Sonoran.js" %}

```javascript
const response = await sonoran.request({
  "method": "PATCH",
  "path": "/v2/community/servers/1/type",
  "body": {
    "type": "FiveM"
  }
});
```

{% endtab %}
{% tab title="Sonoran.py" %}

```python
response = sonoran.request({
  "method": "PATCH",
  "path": "/v2/community/servers/1/type",
  "body": {
    "type": "FiveM"
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
      "path": "/v2/community/servers/1/type",
      "body": {
        "type": "FiveM"
      }
    }
});
```

{% endtab %}
{% tab title="OpenAPI" %}

```yaml
patch:
  summary: Set Server Type
  security:
    - v2ApiKey: []
  parameters:
    - name: serverId
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
  --url "https://api.sonorancms.com/v2/community/servers/1/type" \
  --header "Authorization: Bearer YOUR_API_KEY" \
  --header "Accept: application/json" \
  --data '{"type":"FiveM"}'
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
    "type": "FiveM"
  },
  "meta": {
    "timestamp": "2026-04-14T00:00:00.000Z",
    "path": "/v2/community/servers/1/type"
  }
}
```
