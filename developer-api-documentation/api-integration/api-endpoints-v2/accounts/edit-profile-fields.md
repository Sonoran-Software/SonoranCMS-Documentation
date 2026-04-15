---
description: Update profile field values for an account.
---

# Edit Profile Fields

<mark style="color:green;">`PATCH`</mark> `https://api.sonorancms.com/v2/community/accounts/00000000-0000-0000-0000-000000000000/profile-fields`

> **Rate limit:** `22 requests per minute`  
> Authenticated v2 endpoints are rate limited per credential rather than per IP address.

Update profile field values for an account.

## Route Parameters

| Name | Type | Required | Description |
| --- | --- | --- | --- |
| `accountId` | string (uuid) | Yes | Target accountId. |

## Request Body

| Name | Type | Required | Description |
| --- | --- | --- | --- |
| `profileFields` | array | Yes | See example request for the shape. |

## Example Request

{% tabs %}
{% tab title="Sonoran.lua" %}

```lua
local response = sonoran:request({
  "method": "PATCH",
  "path": "/v2/community/accounts/00000000-0000-0000-0000-000000000000/profile-fields",
  "body": {
    "profileFields": [
      {
        "id": "discord",
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
  "method": "PATCH",
  "path": "/v2/community/accounts/00000000-0000-0000-0000-000000000000/profile-fields",
  "body": {
    "profileFields": [
      {
        "id": "discord",
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
  "method": "PATCH",
  "path": "/v2/community/accounts/00000000-0000-0000-0000-000000000000/profile-fields",
  "body": {
    "profileFields": [
      {
        "id": "discord",
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
      "method": "PATCH",
      "path": "/v2/community/accounts/00000000-0000-0000-0000-000000000000/profile-fields",
      "body": {
        "profileFields": [
          {
            "id": "discord",
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
patch:
  summary: Edit Profile Fields
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
curl --request PATCH \
  --url "https://api.sonorancms.com/v2/community/accounts/00000000-0000-0000-0000-000000000000/profile-fields" \
  --header "Authorization: Bearer YOUR_API_KEY" \
  --header "Accept: application/json" \
  --data '{"profileFields":[{"id":"discord","value":"1234567890"}]}'
```

{% endtab %}
{% endtabs %}

## Response

The `data` array is the updated profile field payload saved back onto the account. Each entry is just an `{ id, value }` pair.

```json
{
  "success": true,
  "data": [
    {
      "id": "discord",
      "value": "1234567890"
    }
  ],
  "meta": {
    "timestamp": "2026-04-15T00:00:00.000Z",
    "path": "/v2/community/accounts/00000000-0000-0000-0000-000000000000/profile-fields"
  }
}
```
