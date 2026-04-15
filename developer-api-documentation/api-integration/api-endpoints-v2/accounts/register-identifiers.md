---
description: Register one or more identifiers for an account.
---

# Register Identifiers

<mark style="color:green;">`POST`</mark> `https://api.sonorancms.com/v2/community/accounts/00000000-0000-0000-0000-000000000000/identifiers`

> **Rate limit:** `22 requests per minute`  
> Authenticated v2 endpoints are rate limited per credential rather than per IP address.

Register one or more identifiers for an account.

## Route Parameters

| Name | Type | Required | Description |
| --- | --- | --- | --- |
| `accountId` | string (uuid) | Yes | Target accountId. |

## Request Body

| Name | Type | Required | Description |
| --- | --- | --- | --- |
| `identifiers` | array | Yes | See example request for the shape. |

## Example Request

{% tabs %}
{% tab title="Sonoran.lua" %}

```lua
local response = sonoran:request({
  "method": "POST",
  "path": "/v2/community/accounts/00000000-0000-0000-0000-000000000000/identifiers",
  "body": {
    "identifiers": [
      {
        "type": "discord",
        "value": "1234567890"
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
  "path": "/v2/community/accounts/00000000-0000-0000-0000-000000000000/identifiers",
  "body": {
    "identifiers": [
      {
        "type": "discord",
        "value": "1234567890"
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
  "path": "/v2/community/accounts/00000000-0000-0000-0000-000000000000/identifiers",
  "body": {
    "identifiers": [
      {
        "type": "discord",
        "value": "1234567890"
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
      "path": "/v2/community/accounts/00000000-0000-0000-0000-000000000000/identifiers",
      "body": {
        "identifiers": [
          {
            "type": "discord",
            "value": "1234567890"
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
  summary: Register Identifiers
  security:
    - v2ApiKey: []
  parameters:
    - name: accountId
      in: path
      required: true
      schema:
        type: string
        format: uuid
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
  --url "https://api.sonorancms.com/v2/community/accounts/00000000-0000-0000-0000-000000000000/identifiers" \
  --header "Authorization: Bearer YOUR_API_KEY" \
  --header "Accept: application/json" \
  --data '{"identifiers":[{"type":"discord","value":"1234567890"}]}'
```

{% endtab %}
{% endtabs %}

## Response

The `data` array contains only the identifier type/value pairs that were registered successfully for the account.

```json
{
  "success": true,
  "data": [
    {
      "type": "discord",
      "value": "1234567890"
    },
    {
      "type": "roblox",
      "value": "987654321"
    }
  ],
  "meta": {
    "timestamp": "2026-04-15T00:00:00.000Z",
    "path": "/v2/community/accounts/00000000-0000-0000-0000-000000000000/identifiers"
  }
}
```
