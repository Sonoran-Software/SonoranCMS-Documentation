---
description: Search for community accounts.
---

# Search Accounts

<mark style="color:green;">`GET`</mark> `https://api.sonorancms.com/v2/community/accounts/search`

> **Rate limit:** `27 requests per minute`  
> Authenticated v2 endpoints are rate limited per credential rather than per IP address.

Search for community accounts.

## Query Parameters

| Name | Type | Required | Description |
| --- | --- | --- | --- |
| `username` | string | Yes | See example request for the shape. |

## Example Request

{% tabs %}
{% tab title="Sonoran.lua" %}

```lua
local response = sonoran:request({
  "method": "GET",
  "path": "/v2/community/accounts/search",
  "query": {
    "username": "ExampleUser"
  }
})
```

{% endtab %}
{% tab title="Sonoran.js" %}

```javascript
const response = await sonoran.request({
  "method": "GET",
  "path": "/v2/community/accounts/search",
  "query": {
    "username": "ExampleUser"
  }
});
```

{% endtab %}
{% tab title="Sonoran.py" %}

```python
response = sonoran.request({
  "method": "GET",
  "path": "/v2/community/accounts/search",
  "query": {
    "username": "ExampleUser"
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
      "path": "/v2/community/accounts/search",
      "query": {
        "username": "ExampleUser"
      }
    }
});
```

{% endtab %}
{% tab title="OpenAPI" %}

```yaml
get:
  summary: Search Accounts
  security:
    - v2ApiKey: []
  parameters:
    - name: username
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
  --url "https://api.sonorancms.com/v2/community/accounts/search?username=ExampleUser" \
  --header "Authorization: Bearer YOUR_API_KEY" \
  --header "Accept: application/json"
```

{% endtab %}
{% endtabs %}

## Response

The `data` object contains the matched accounts and a `total` count. This search endpoint does not page the result set beyond the service-level filters.

```json
{
  "success": true,
  "data": {
    "items": [
      {
        "accId": "00000000-0000-0000-0000-000000000000",
        "uniqueId": 1001,
        "accName": "ExampleAccount",
        "comName": "Example Community",
        "activeApiIds": [
          "discord:1234567890"
        ],
        "discordId": "1234567890",
        "sysStatus": true,
        "comStatus": true,
        "archived": false,
        "banned": false,
        "teamspeakId": null
      }
    ],
    "total": 1
  },
  "meta": {
    "timestamp": "2026-04-15T00:00:00.000Z",
    "path": "/v2/community/accounts/search"
  }
}
```
