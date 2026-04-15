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

The `data` array contains the disciplinary records for the account. On the API path the records are annotated with an `expired` flag when the community uses expiration windows.

```json
{
  "success": true,
  "data": [
    {
      "id": "55555555-5555-5555-5555-555555555555",
      "status": true,
      "accId": "00000000-0000-0000-0000-000000000000",
      "source": "api",
      "sourceId": "api-request",
      "points": 5,
      "reason": "Example disciplinary action",
      "metadata": {
        "executionSource": "discord"
      },
      "history": {
        "2026-04-15T00:00:00.000Z": {
          "action": "init",
          "points": 5,
          "reason": "Example disciplinary action",
          "metadata": {
            "executionSource": "discord"
          },
          "timestamp": "2026-04-15T00:00:00.000Z",
          "source": "api",
          "sourceId": "api-request"
        }
      },
      "createdAt": "2026-04-15T00:00:00.000Z",
      "updatedAt": null,
      "expired": false
    }
  ],
  "meta": {
    "timestamp": "2026-04-15T00:00:00.000Z",
    "path": "/v2/community/disciplinary/accounts/00000000-0000-0000-0000-000000000000/records"
  }
}
```
