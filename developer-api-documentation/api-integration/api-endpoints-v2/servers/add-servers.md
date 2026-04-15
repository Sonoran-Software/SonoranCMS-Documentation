---
description: Append one or more servers to the configuration.
---

# Add Servers

<mark style="color:green;">`POST`</mark> `https://api.sonorancms.com/v2/community/servers`

> **Rate limit:** `9 requests per minute`  
> Authenticated v2 endpoints are rate limited per credential rather than per IP address.

Append one or more servers to the configuration.

## Request Body

| Name | Type | Required | Description |
| --- | --- | --- | --- |
| `servers` | array | Yes | See example request for the shape. |

## Example Request

{% tabs %}
{% tab title="Sonoran.lua" %}

```lua
local response = sonoran:request({
  "method": "POST",
  "path": "/v2/community/servers",
  "body": {
    "servers": [
      {
        "id": 1,
        "name": "Main Server",
        "description": "Primary community server",
        "ip": "127.0.0.1",
        "port": "30120",
        "type": "FiveM",
        "erlcApiKey": "",
        "robloxJoinCode": "ABC123",
        "aceConfig": {},
        "robloxMetadata": {}
      }
    ]
  }
})
```

{% endtab %}
{% tab title="Sonoran.js" %}

```javascript
const response = await sonoran.request({
  "method": "POST",
  "path": "/v2/community/servers",
  "body": {
    "servers": [
      {
        "id": 1,
        "name": "Main Server",
        "description": "Primary community server",
        "ip": "127.0.0.1",
        "port": "30120",
        "type": "FiveM",
        "erlcApiKey": "",
        "robloxJoinCode": "ABC123",
        "aceConfig": {},
        "robloxMetadata": {}
      }
    ]
  }
});
```

{% endtab %}
{% tab title="Sonoran.py" %}

```python
response = sonoran.request({
  "method": "POST",
  "path": "/v2/community/servers",
  "body": {
    "servers": [
      {
        "id": 1,
        "name": "Main Server",
        "description": "Primary community server",
        "ip": "127.0.0.1",
        "port": "30120",
        "type": "FiveM",
        "erlcApiKey": "",
        "robloxJoinCode": "ABC123",
        "aceConfig": {},
        "robloxMetadata": {}
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
      "method": "POST",
      "path": "/v2/community/servers",
      "body": {
        "servers": [
          {
            "id": 1,
            "name": "Main Server",
            "description": "Primary community server",
            "ip": "127.0.0.1",
            "port": "30120",
            "type": "FiveM",
            "erlcApiKey": "",
            "robloxJoinCode": "ABC123",
            "aceConfig": {},
            "robloxMetadata": {}
          }
        ]
      }
    }
});
```

{% endtab %}
{% tab title="OpenAPI" %}

```yaml
post:
  summary: Add Servers
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
curl --request POST \
  --url "https://api.sonorancms.com/v2/community/servers" \
  --header "Authorization: Bearer YOUR_API_KEY" \
  --header "Accept: application/json" \
  --data '{"servers":[{"id":1,"name":"Main Server","description":"Primary community server","ip":"127.0.0.1","port":"30120","type":"FiveM","erlcApiKey":"","robloxJoinCode":"ABC123","aceConfig":{},"robloxMetadata":{}}]}'
```

{% endtab %}
{% endtabs %}

## Response

Successful requests return `application/json` and use the standard v2 envelope.

```json
{
  "success": true,
  "data": {
    "servers": [
      {
        "id": 1,
        "name": "Main Server",
        "description": "Primary community server"
      }
    ]
  },
  "meta": {
    "timestamp": "2026-04-14T00:00:00.000Z",
    "path": "/v2/community/servers"
  }
}
```
