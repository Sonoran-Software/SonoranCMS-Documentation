---
description: Retrieve a single community account.
---

# Get Account

<mark style="color:green;">`GET`</mark> `https://api.sonorancms.com/v2/community/accounts/00000000-0000-0000-0000-000000000000`

> **Rate limit:** `27 requests per minute`  
> Authenticated v2 endpoints are rate limited per credential rather than per IP address.

Retrieve a single community account.

## Route Parameters

| Name | Type | Required | Description |
| --- | --- | --- | --- |
| `accountId` | string (uuid) | Yes | Target accountId. |

## Example Request

{% tabs %}
{% tab title="Sonoran.lua" %}

```lua
local response = sonoran:request({
  "method": "GET",
  "path": "/v2/community/accounts/00000000-0000-0000-0000-000000000000"
})
```

{% endtab %}
{% tab title="Sonoran.js" %}

```javascript
const response = await sonoran.request({
  "method": "GET",
  "path": "/v2/community/accounts/00000000-0000-0000-0000-000000000000"
});
```

{% endtab %}
{% tab title="Sonoran.py" %}

```python
response = sonoran.request({
  "method": "GET",
  "path": "/v2/community/accounts/00000000-0000-0000-0000-000000000000"
})
```

{% endtab %}
{% tab title="Sonoran.Net" %}

```csharp
var response = await sonoran.RequestAsync(new SonoranRequest
{
    {
      "method": "GET",
      "path": "/v2/community/accounts/00000000-0000-0000-0000-000000000000"
    }
});
```

{% endtab %}
{% tab title="OpenAPI" %}

```yaml
get:
  summary: Get Account
  security:
    - v2ApiKey: []
  parameters:
    - name: accountId
      in: path
      required: true
      schema:
        type: string
        format: uuid
  responses:
    '200':
      description: Successful response
```

{% endtab %}
{% tab title="cURL" %}

```bash
curl --request GET \
  --url "https://api.sonorancms.com/v2/community/accounts/00000000-0000-0000-0000-000000000000" \
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
  "data": {
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
  },
  "meta": {
    "timestamp": "2026-04-14T00:00:00.000Z",
    "path": "/v2/community/accounts/00000000-0000-0000-0000-000000000000"
  }
}
```
