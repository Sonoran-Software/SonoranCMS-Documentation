---
description: Retrieve disciplinary records for a member.
---

# Get Member Records

<mark style="color:green;">`GET`</mark> `https://api.sonorancms.com/v2/community/disciplinary/accounts/00000000-0000-0000-0000-000000000000/records`

> **Rate limit:** `27 requests per minute`  
> Authenticated v2 endpoints are rate limited per credential rather than per IP address.

Retrieve disciplinary records for a member.

## Route Parameters

| Name | Type | Required | Description |
| --- | --- | --- | --- |
| `accountId` | string (uuid) | Yes | Target accountId. |

## Query Parameters

| Name | Type | Required | Description |
| --- | --- | --- | --- |
| `accId` | string | Yes | See example request for the shape. |

## Example Request

{% tabs %}
{% tab title="Sonoran.lua" %}

```lua
local response = sonoran:request({
  "method": "GET",
  "path": "/v2/community/disciplinary/accounts/00000000-0000-0000-0000-000000000000/records",
  "query": {
    "accId": "00000000-0000-0000-0000-000000000000"
  }
})
```

{% endtab %}
{% tab title="Sonoran.js" %}

```javascript
const response = await sonoran.request({
  "method": "GET",
  "path": "/v2/community/disciplinary/accounts/00000000-0000-0000-0000-000000000000/records",
  "query": {
    "accId": "00000000-0000-0000-0000-000000000000"
  }
});
```

{% endtab %}
{% tab title="Sonoran.py" %}

```python
response = sonoran.request({
  "method": "GET",
  "path": "/v2/community/disciplinary/accounts/00000000-0000-0000-0000-000000000000/records",
  "query": {
    "accId": "00000000-0000-0000-0000-000000000000"
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
      "path": "/v2/community/disciplinary/accounts/00000000-0000-0000-0000-000000000000/records",
      "query": {
        "accId": "00000000-0000-0000-0000-000000000000"
      }
    }
});
```

{% endtab %}
{% tab title="OpenAPI" %}

```yaml
get:
  summary: Get Member Records
  security:
    - v2ApiKey: []
  parameters:
    - name: accountId
      in: path
      required: true
      schema:
        type: string
        format: uuid
  parameters:
    - name: accId
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
  --url "https://api.sonorancms.com/v2/community/disciplinary/accounts/00000000-0000-0000-0000-000000000000/records?accId=00000000-0000-0000-0000-000000000000" \
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
      "recordId": "11111111-1111-1111-1111-111111111111",
      "accId": "00000000-0000-0000-0000-000000000000",
      "points": 5,
      "reason": "Training violation",
      "status": true
    }
  ],
  "meta": {
    "timestamp": "2026-04-14T00:00:00.000Z",
    "path": "/v2/community/disciplinary/accounts/00000000-0000-0000-0000-000000000000/records"
  }
}
```
