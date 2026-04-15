---
description: Update the ACE configuration for a server.
---

# Set ACE Config

<mark style="color:green;">`PATCH`</mark> `https://api.sonorancms.com/v2/community/servers/1/ace-config`

> **Rate limit:** `18 requests per minute`  
> Authenticated v2 endpoints are rate limited per credential rather than per IP address.

Update the ACE configuration for a server.

## Route Parameters

| Name | Type | Required | Description |
| --- | --- | --- | --- |
| `serverId` | number | Yes | Target serverId. |

## Request Body

| Name | Type | Required | Description |
| --- | --- | --- | --- |
| `mappings` | array | Yes | See example request for the shape. |

## Example Request

{% tabs %}
{% tab title="Sonoran.lua" %}

```lua
local response = sonoran:request({
  "method": "PATCH",
  "path": "/v2/community/servers/1/ace-config",
  "body": {
    "mappings": [
      {
        "discordRoleId": "1234567890",
        "aceGroup": "admin"
      }
    ]
  }
})
```

{% endtab %}
{% tab title="Sonoran.js" %}

```javascript
const response = await sonoran.request({
  "method": "PATCH",
  "path": "/v2/community/servers/1/ace-config",
  "body": {
    "mappings": [
      {
        "discordRoleId": "1234567890",
        "aceGroup": "admin"
      }
    ]
  }
});
```

{% endtab %}
{% tab title="Sonoran.py" %}

```python
response = sonoran.request({
  "method": "PATCH",
  "path": "/v2/community/servers/1/ace-config",
  "body": {
    "mappings": [
      {
        "discordRoleId": "1234567890",
        "aceGroup": "admin"
      }
    ]
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
      "path": "/v2/community/servers/1/ace-config",
      "body": {
        "mappings": [
          {
            "discordRoleId": "1234567890",
            "aceGroup": "admin"
          }
        ]
      }
    }
});
```

{% endtab %}
{% tab title="OpenAPI" %}

```yaml
patch:
  summary: Set ACE Config
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
  --url "https://api.sonorancms.com/v2/community/servers/1/ace-config" \
  --header "Authorization: Bearer YOUR_API_KEY" \
  --header "Accept: application/json" \
  --data '{"mappings":[{"discordRoleId":"1234567890","aceGroup":"admin"}]}'
```

{% endtab %}
{% endtabs %}

## Response

The `data` object is the updated ACE config wrapper with the saved `mappings` array.

```json
{
  "success": true,
  "data": {
    "mappings": [
      {
        "ranks": [
          "22222222-2222-2222-2222-222222222222"
        ],
        "principal": "group:123456"
      }
    ]
  },
  "meta": {
    "timestamp": "2026-04-15T00:00:00.000Z",
    "path": "/v2/community/servers/1/ace-config"
  }
}
```
