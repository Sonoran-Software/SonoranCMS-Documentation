---
description: Record a server activity event.
---

# Activity Tracker

<mark style="color:green;">`POST`</mark> `https://api.sonorancms.com/v2/community/servers/1/activity`

> **Rate limit:** `27 requests per minute`  
> Authenticated v2 endpoints are rate limited per credential rather than per IP address.

Record a server activity event.

## Route Parameters

| Name | Type | Required | Description |
| --- | --- | --- | --- |
| `serverId` | number | Yes | Target serverId. |

## Request Body

| Name | Type | Required | Description |
| --- | --- | --- | --- |
| `accId` | string | Yes | See example request for the shape. |
| `forceStart` | boolean | Yes | See example request for the shape. |

## Example Request

{% tabs %}
{% tab title="Sonoran.lua" %}

```lua
local response = sonoran:request({
  "method": "POST",
  "path": "/v2/community/servers/1/activity",
  "body": {
    "accId": "00000000-0000-0000-0000-000000000000",
    "forceStart": true
  }
})
```

{% endtab %}
{% tab title="Sonoran.js" %}

```javascript
const response = await sonoran.request({
  "method": "POST",
  "path": "/v2/community/servers/1/activity",
  "body": {
    "accId": "00000000-0000-0000-0000-000000000000",
    "forceStart": true
  }
});
```

{% endtab %}
{% tab title="Sonoran.py" %}

```python
response = sonoran.request({
  "method": "POST",
  "path": "/v2/community/servers/1/activity",
  "body": {
    "accId": "00000000-0000-0000-0000-000000000000",
    "forceStart": true
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
      "path": "/v2/community/servers/1/activity",
      "body": {
        "accId": "00000000-0000-0000-0000-000000000000",
        "forceStart": true
      }
    }
});
```

{% endtab %}
{% tab title="OpenAPI" %}

```yaml
post:
  summary: Activity Tracker
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
curl --request POST \
  --url "https://api.sonorancms.com/v2/community/servers/1/activity" \
  --header "Authorization: Bearer YOUR_API_KEY" \
  --header "Accept: application/json" \
  --data '{"accId":"00000000-0000-0000-0000-000000000000","forceStart":true}'
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
    "tracked": true,
    "forceStart": false,
    "forceStop": false
  },
  "meta": {
    "timestamp": "2026-04-14T00:00:00.000Z",
    "path": "/v2/community/servers/1/activity"
  }
}
```
