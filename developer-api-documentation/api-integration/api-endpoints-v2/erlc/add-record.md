---
description: Create an ER:LC record.
---

# Add ERLC Record

<mark style="color:green;">`POST`</mark> `https://api.sonorancms.com/v2/community/erlc/records`

> **Rate limit:** `18 requests per minute`  
> Authenticated v2 endpoints are rate limited per credential rather than per IP address.

Create an ER:LC record.

## Request Body

| Name | Type | Required | Description |
| --- | --- | --- | --- |
| `robloxJoinCode` | string | Yes | See example request for the shape. |
| `executerDiscordId` | string | Yes | See example request for the shape. |
| `type` | string | Yes | See example request for the shape. |
| `reason` | string | Yes | See example request for the shape. |
| `points` | number | Yes | See example request for the shape. |

## Example Request

{% tabs %}
{% tab title="Sonoran.lua" %}

```lua
local response = sonoran:request({
  "method": "POST",
  "path": "/v2/community/erlc/records",
  "body": {
    "robloxJoinCode": "ABC123",
    "executerDiscordId": "1234567890",
    "type": "note",
    "reason": "Example note",
    "points": 0
  }
})
```

{% endtab %}
{% tab title="Sonoran.js" %}

```javascript
const response = await sonoran.request({
  "method": "POST",
  "path": "/v2/community/erlc/records",
  "body": {
    "robloxJoinCode": "ABC123",
    "executerDiscordId": "1234567890",
    "type": "note",
    "reason": "Example note",
    "points": 0
  }
});
```

{% endtab %}
{% tab title="Sonoran.py" %}

```python
response = sonoran.request({
  "method": "POST",
  "path": "/v2/community/erlc/records",
  "body": {
    "robloxJoinCode": "ABC123",
    "executerDiscordId": "1234567890",
    "type": "note",
    "reason": "Example note",
    "points": 0
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
      "path": "/v2/community/erlc/records",
      "body": {
        "robloxJoinCode": "ABC123",
        "executerDiscordId": "1234567890",
        "type": "note",
        "reason": "Example note",
        "points": 0
      }
    }
});
```

{% endtab %}
{% tab title="OpenAPI" %}

```yaml
post:
  summary: Add ERLC Record
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
  --url "https://api.sonorancms.com/v2/community/erlc/records" \
  --header "Authorization: Bearer YOUR_API_KEY" \
  --header "Accept: application/json" \
  --data '{"robloxJoinCode":"ABC123","executerDiscordId":"1234567890","type":"note","reason":"Example note","points":0}'
```

{% endtab %}
{% endtabs %}

## Response

The response shape varies by record `type`:

- `note`, `kick`, and custom log types return a confirmation object such as `{ success: true, message: "Records added successfully" }`.
- `ban` returns `{ success: true }` after the ban queue is updated.
- `disciplinary` returns the disciplinary service payload, which is usually `{ success: true, data: [DisciplinaryRecord] }`.

```json
{
  "success": true,
  "data": {
    "success": true,
    "message": "Records added successfully"
  },
  "meta": {
    "timestamp": "2026-04-15T00:00:00.000Z",
    "path": "/v2/community/erlc/records"
  }
}
```
