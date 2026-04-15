---
description: Create a disciplinary record.
---

# Add Member Record

<mark style="color:green;">`POST`</mark> `https://api.sonorancms.com/v2/community/disciplinary/accounts/00000000-0000-0000-0000-000000000000/records`

> **Rate limit:** `18 requests per minute`  
> Authenticated v2 endpoints are rate limited per credential rather than per IP address.

Create a disciplinary record.

## Route Parameters

| Name | Type | Required | Description |
| --- | --- | --- | --- |
| `accountId` | string (uuid) | Yes | Target accountId. |

## Request Body

| Name | Type | Required | Description |
| --- | --- | --- | --- |
| `points` | number | Yes | See example request for the shape. |
| `reason` | string | Yes | See example request for the shape. |

## Example Request

{% tabs %}
{% tab title="Sonoran.lua" %}

```lua
local response = sonoran:request({
  "method": "POST",
  "path": "/v2/community/disciplinary/accounts/00000000-0000-0000-0000-000000000000/records",
  "body": {
    "points": 5,
    "reason": "Training violation"
  }
})
```

{% endtab %}
{% tab title="Sonoran.js" %}

```javascript
const response = await sonoran.request({
  "method": "POST",
  "path": "/v2/community/disciplinary/accounts/00000000-0000-0000-0000-000000000000/records",
  "body": {
    "points": 5,
    "reason": "Training violation"
  }
});
```

{% endtab %}
{% tab title="Sonoran.py" %}

```python
response = sonoran.request({
  "method": "POST",
  "path": "/v2/community/disciplinary/accounts/00000000-0000-0000-0000-000000000000/records",
  "body": {
    "points": 5,
    "reason": "Training violation"
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
      "path": "/v2/community/disciplinary/accounts/00000000-0000-0000-0000-000000000000/records",
      "body": {
        "points": 5,
        "reason": "Training violation"
      }
    }
});
```

{% endtab %}
{% tab title="OpenAPI" %}

```yaml
post:
  summary: Add Member Record
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
  --url "https://api.sonorancms.com/v2/community/disciplinary/accounts/00000000-0000-0000-0000-000000000000/records" \
  --header "Authorization: Bearer YOUR_API_KEY" \
  --header "Accept: application/json" \
  --data '{"points":5,"reason":"Training violation"}'
```

{% endtab %}
{% endtabs %}

## Response

Successful requests return `application/json` and use the standard v2 envelope.

```json
{
  "success": true,
  "data": {
    "recordId": "11111111-1111-1111-1111-111111111111",
    "accId": "00000000-0000-0000-0000-000000000000",
    "points": 5,
    "reason": "Training violation",
    "status": true
  },
  "meta": {
    "timestamp": "2026-04-14T00:00:00.000Z",
    "path": "/v2/community/disciplinary/accounts/00000000-0000-0000-0000-000000000000/records"
  }
}
```
