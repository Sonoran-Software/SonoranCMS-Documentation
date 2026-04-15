---
description: Retrieve a list of community accounts.
---

# Get Accounts

<mark style="color:green;">`GET`</mark> `https://api.sonorancms.com/v2/community/accounts`

> **Rate limit:** `22 requests per minute`  
> Authenticated v2 endpoints are rate limited per credential rather than per IP address.

Retrieve a list of community accounts.

## Query Parameters

| Name | Type | Required | Description |
| --- | --- | --- | --- |
| `skip` | number | Yes | See example request for the shape. |
| `take` | number | Yes | See example request for the shape. |
| `sysStatus` | boolean | Yes | See example request for the shape. |

## Example Request

{% tabs %}
{% tab title="Sonoran.lua" %}

```lua
local response = sonoran:request({
  "method": "GET",
  "path": "/v2/community/accounts",
  "query": {
    "skip": 0,
    "take": 25,
    "sysStatus": true
  }
})
```

{% endtab %}
{% tab title="Sonoran.js" %}

```javascript
const response = await sonoran.request({
  "method": "GET",
  "path": "/v2/community/accounts",
  "query": {
    "skip": 0,
    "take": 25,
    "sysStatus": true
  }
});
```

{% endtab %}
{% tab title="Sonoran.py" %}

```python
response = sonoran.request({
  "method": "GET",
  "path": "/v2/community/accounts",
  "query": {
    "skip": 0,
    "take": 25,
    "sysStatus": true
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
      "path": "/v2/community/accounts",
      "query": {
        "skip": 0,
        "take": 25,
        "sysStatus": true
      }
    }
});
```

{% endtab %}
{% tab title="OpenAPI" %}

```yaml
get:
  summary: Get Accounts
  security:
    - v2ApiKey: []
  parameters:
    - name: skip
      in: query
      required: false
      schema:
        type: integer
    - name: take
      in: query
      required: false
      schema:
        type: integer
    - name: sysStatus
      in: query
      required: false
      schema:
        type: boolean
  responses:
    '200':
      description: Successful response
```

{% endtab %}
{% tab title="cURL" %}

```bash
curl --request GET \
  --url "https://api.sonorancms.com/v2/community/accounts?skip=0&take=25&sysStatus=true" \
  --header "Authorization: Bearer YOUR_API_KEY" \
  --header "Accept: application/json"
```

{% endtab %}
{% endtabs %}

## Response

Successful requests return `application/json` and use the standard v2 envelope.

```json
{
  "success": true,
  "data": [
    {
      "accId": "00000000-0000-0000-0000-000000000000",
      "accName": "ExampleAccount",
      "activeApiIds": [],
      "discordId": "1234567890",
      "uniqueId": 1,
      "banned": false,
      "archived": false,
      "comName": "Example Account",
      "comStatus": true,
      "joinDate": "",
      "lastLogin": "",
      "owner": true,
      "identifiers": [],
      "ranks": [],
      "sysStatus": true,
      "profileFields": []
    }
  ],
  "meta": {
    "timestamp": "2026-04-14T00:00:00.000Z",
    "path": "/v2/community/accounts"
  }
}
```
