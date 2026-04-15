---
description: Clock an account in or out.
---

# Clock Account

<mark style="color:green;">`POST`</mark> `https://api.sonorancms.com/v2/community/accounts/00000000-0000-0000-0000-000000000000/clock`

> **Rate limit:** `22 requests per minute`  
> Authenticated v2 endpoints are rate limited per credential rather than per IP address.

Clock an account in or out.

## Route Parameters

| Name | Type | Required | Description |
| --- | --- | --- | --- |
| `accountId` | string (uuid) | Yes | Target accountId. |

## Request Body

| Name | Type | Required | Description |
| --- | --- | --- | --- |
| `accId` | string | Yes | See example request for the shape. |
| `intention` | string | Yes | See example request for the shape. |
| `type` | string | Yes | See example request for the shape. |

## Example Request

{% tabs %}
{% tab title="Sonoran.lua" %}

```lua
local response = sonoran:request({
  "method": "POST",
  "path": "/v2/community/accounts/00000000-0000-0000-0000-000000000000/clock",
  "body": {
    "accId": "00000000-0000-0000-0000-000000000000",
    "intention": "in",
    "type": "regular"
  }
})
```

{% endtab %}
{% tab title="Sonoran.js" %}

```javascript
const response = await sonoran.request({
  "method": "POST",
  "path": "/v2/community/accounts/00000000-0000-0000-0000-000000000000/clock",
  "body": {
    "accId": "00000000-0000-0000-0000-000000000000",
    "intention": "in",
    "type": "regular"
  }
});
```

{% endtab %}
{% tab title="Sonoran.py" %}

```python
response = sonoran.request({
  "method": "POST",
  "path": "/v2/community/accounts/00000000-0000-0000-0000-000000000000/clock",
  "body": {
    "accId": "00000000-0000-0000-0000-000000000000",
    "intention": "in",
    "type": "regular"
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
      "path": "/v2/community/accounts/00000000-0000-0000-0000-000000000000/clock",
      "body": {
        "accId": "00000000-0000-0000-0000-000000000000",
        "intention": "in",
        "type": "regular"
      }
    }
});
```

{% endtab %}
{% tab title="OpenAPI" %}

```yaml
post:
  summary: Clock Account
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
  --url "https://api.sonorancms.com/v2/community/accounts/00000000-0000-0000-0000-000000000000/clock" \
  --header "Authorization: Bearer YOUR_API_KEY" \
  --header "Accept: application/json" \
  --data '{"accId":"00000000-0000-0000-0000-000000000000","intention":"in","type":"regular"}'
```

{% endtab %}
{% endtabs %}

## Response

Successful requests return `application/json` and use the standard v2 envelope.

```json
{
  "success": true,
  "data": {
    "clockId": "clock-1",
    "accId": "00000000-0000-0000-0000-000000000000",
    "state": "in",
    "type": "regular",
    "time": "2026-04-14T00:00:00.000Z"
  },
  "meta": {
    "timestamp": "2026-04-14T00:00:00.000Z",
    "path": "/v2/community/accounts/00000000-0000-0000-0000-000000000000/clock"
  }
}
```
