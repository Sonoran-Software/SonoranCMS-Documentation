---
description: Update the status of a disciplinary record.
---

# Update Member Record Status

<mark style="color:green;">`PATCH`</mark> `https://api.sonorancms.com/v2/community/disciplinary/records/11111111-1111-1111-1111-111111111111/status`

> **Rate limit:** `18 requests per minute`  
> Authenticated v2 endpoints are rate limited per credential rather than per IP address.

Update the status of a disciplinary record.

## Route Parameters

| Name | Type | Required | Description |
| --- | --- | --- | --- |
| `recordId` | string (uuid) | Yes | Target recordId. |

## Request Body

| Name | Type | Required | Description |
| --- | --- | --- | --- |
| `status` | boolean | Yes | See example request for the shape. |

## Example Request

{% tabs %}
{% tab title="Sonoran.lua" %}

```lua
local response = sonoran:request({
  "method": "PATCH",
  "path": "/v2/community/disciplinary/records/11111111-1111-1111-1111-111111111111/status",
  "body": {
    "status": true
  }
})
```

{% endtab %}
{% tab title="Sonoran.js" %}

```javascript
const response = await sonoran.request({
  "method": "PATCH",
  "path": "/v2/community/disciplinary/records/11111111-1111-1111-1111-111111111111/status",
  "body": {
    "status": true
  }
});
```

{% endtab %}
{% tab title="Sonoran.py" %}

```python
response = sonoran.request({
  "method": "PATCH",
  "path": "/v2/community/disciplinary/records/11111111-1111-1111-1111-111111111111/status",
  "body": {
    "status": true
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
      "path": "/v2/community/disciplinary/records/11111111-1111-1111-1111-111111111111/status",
      "body": {
        "status": true
      }
    }
});
```

{% endtab %}
{% tab title="OpenAPI" %}

```yaml
patch:
  summary: Update Member Record Status
  security:
    - v2ApiKey: []
  parameters:
    - name: recordId
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
  --url "https://api.sonorancms.com/v2/community/disciplinary/records/11111111-1111-1111-1111-111111111111/status" \
  --header "Authorization: Bearer YOUR_API_KEY" \
  --header "Accept: application/json" \
  --data '{"status":true}'
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
    "path": "/v2/community/disciplinary/records/11111111-1111-1111-1111-111111111111/status"
  }
}
```
