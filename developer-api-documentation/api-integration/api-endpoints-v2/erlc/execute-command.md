---
description: Execute an ER:LC command.
---

# Execute Command

<mark style="color:green;">`POST`</mark> `https://api.sonorancms.com/v2/community/erlc/commands`

> **Rate limit:** `18 requests per minute`  
> Authenticated v2 endpoints are rate limited per credential rather than per IP address.

Execute an ER:LC command.

## Request Body

| Name | Type | Required | Description |
| --- | --- | --- | --- |
| `robloxJoinCode` | string | Yes | See example request for the shape. |
| `discordId` | string | Yes | See example request for the shape. |
| `type` | string | Yes | See example request for the shape. |
| `args` | string | Yes | See example request for the shape. |
| `includesPlayerNameOrId` | boolean | Yes | See example request for the shape. |

## Example Request

{% tabs %}
{% tab title="Sonoran.lua" %}

```lua
local response = sonoran:request({
  "method": "POST",
  "path": "/v2/community/erlc/commands",
  "body": {
    "robloxJoinCode": "ABC123",
    "discordId": "1234567890",
    "type": "announce",
    "args": "Server restart in 10 minutes",
    "includesPlayerNameOrId": false
  }
})
```

{% endtab %}
{% tab title="Sonoran.js" %}

```javascript
const response = await sonoran.request({
  "method": "POST",
  "path": "/v2/community/erlc/commands",
  "body": {
    "robloxJoinCode": "ABC123",
    "discordId": "1234567890",
    "type": "announce",
    "args": "Server restart in 10 minutes",
    "includesPlayerNameOrId": false
  }
});
```

{% endtab %}
{% tab title="Sonoran.py" %}

```python
response = sonoran.request({
  "method": "POST",
  "path": "/v2/community/erlc/commands",
  "body": {
    "robloxJoinCode": "ABC123",
    "discordId": "1234567890",
    "type": "announce",
    "args": "Server restart in 10 minutes",
    "includesPlayerNameOrId": false
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
      "path": "/v2/community/erlc/commands",
      "body": {
        "robloxJoinCode": "ABC123",
        "discordId": "1234567890",
        "type": "announce",
        "args": "Server restart in 10 minutes",
        "includesPlayerNameOrId": false
      }
    }
});
```

{% endtab %}
{% tab title="OpenAPI" %}

```yaml
post:
  summary: Execute Command
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
  --url "https://api.sonorancms.com/v2/community/erlc/commands" \
  --header "Authorization: Bearer YOUR_API_KEY" \
  --header "Accept: application/json" \
  --data '{"robloxJoinCode":"ABC123","discordId":"1234567890","type":"announce","args":"Server restart in 10 minutes","includesPlayerNameOrId":false}'
```

{% endtab %}
{% endtabs %}

## Response

Successful requests return `application/json` and use the standard v2 envelope.

```json
{
  "success": true,
  "data": {
    "commandId": "cmd-1",
    "queued": true,
    "output": "Command queued."
  },
  "meta": {
    "timestamp": "2026-04-14T00:00:00.000Z",
    "path": "/v2/community/erlc/commands"
  }
}
```
