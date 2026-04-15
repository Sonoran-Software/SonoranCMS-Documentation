---
description: Lock an ER:LC team.
---

# Lock Team

<mark style="color:green;">`POST`</mark> `https://api.sonorancms.com/v2/community/erlc/teams/lock`

> **Rate limit:** `18 requests per minute`  
> Authenticated v2 endpoints are rate limited per credential rather than per IP address.

Lock an ER:LC team.

## Request Body

| Name | Type | Required | Description |
| --- | --- | --- | --- |
| `robloxJoinCode` | string | Yes | See example request for the shape. |
| `team` | string | Yes | See example request for the shape. |
| `maxPlayers` | number | Yes | See example request for the shape. |

## Example Request

{% tabs %}
{% tab title="Sonoran.lua" %}

```lua
local response = sonoran:request({
  "method": "POST",
  "path": "/v2/community/erlc/teams/lock",
  "body": {
    "robloxJoinCode": "ABC123",
    "team": "Police",
    "maxPlayers": 10
  }
})
```

{% endtab %}
{% tab title="Sonoran.js" %}

```javascript
const response = await sonoran.request({
  "method": "POST",
  "path": "/v2/community/erlc/teams/lock",
  "body": {
    "robloxJoinCode": "ABC123",
    "team": "Police",
    "maxPlayers": 10
  }
});
```

{% endtab %}
{% tab title="Sonoran.py" %}

```python
response = sonoran.request({
  "method": "POST",
  "path": "/v2/community/erlc/teams/lock",
  "body": {
    "robloxJoinCode": "ABC123",
    "team": "Police",
    "maxPlayers": 10
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
      "path": "/v2/community/erlc/teams/lock",
      "body": {
        "robloxJoinCode": "ABC123",
        "team": "Police",
        "maxPlayers": 10
      }
    }
});
```

{% endtab %}
{% tab title="OpenAPI" %}

```yaml
post:
  summary: Lock Team
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
  --url "https://api.sonorancms.com/v2/community/erlc/teams/lock" \
  --header "Authorization: Bearer YOUR_API_KEY" \
  --header "Accept: application/json" \
  --data '{"robloxJoinCode":"ABC123","team":"Police","maxPlayers":10}'
```

{% endtab %}
{% endtabs %}

## Response

The `data` value is a confirmation string. The exact wording changes for lock and unlock, but both endpoints return a string rather than a structured object.

```json
{
  "success": true,
  "data": "The police team has been locked down to a maximum of 12 players.",
  "meta": {
    "timestamp": "2026-04-15T00:00:00.000Z",
    "path": "/v2/community/erlc/teams/lock"
  }
}
```
