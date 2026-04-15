---
description: Retrieve the latest activity for an account.
---

# Get Latest Activity

<mark style="color:green;">`GET`</mark> `https://api.sonorancms.com/v2/community/accounts/00000000-0000-0000-0000-000000000000/activity/latest`

> **Rate limit:** `27 requests per minute`  
> Authenticated v2 endpoints are rate limited per credential rather than per IP address.

Retrieve the latest activity for an account.

## Route Parameters

| Name | Type | Required | Description |
| --- | --- | --- | --- |
| `accountId` | string (uuid) | Yes | Target accountId. |

## Query Parameters

| Name | Type | Required | Description |
| --- | --- | --- | --- |
| `accId` | string | Yes | See example request for the shape. |
| `type` | string | Yes | See example request for the shape. |

## Example Request

{% tabs %}
{% tab title="Sonoran.lua" %}

```lua
local response = sonoran:request({
  "method": "GET",
  "path": "/v2/community/accounts/00000000-0000-0000-0000-000000000000/activity/latest",
  "query": {
    "accId": "00000000-0000-0000-0000-000000000000",
    "type": "activity"
  }
})
```

{% endtab %}
{% tab title="Sonoran.js" %}

```javascript
const response = await sonoran.request({
  "method": "GET",
  "path": "/v2/community/accounts/00000000-0000-0000-0000-000000000000/activity/latest",
  "query": {
    "accId": "00000000-0000-0000-0000-000000000000",
    "type": "activity"
  }
});
```

{% endtab %}
{% tab title="Sonoran.py" %}

```python
response = sonoran.request({
  "method": "GET",
  "path": "/v2/community/accounts/00000000-0000-0000-0000-000000000000/activity/latest",
  "query": {
    "accId": "00000000-0000-0000-0000-000000000000",
    "type": "activity"
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
      "path": "/v2/community/accounts/00000000-0000-0000-0000-000000000000/activity/latest",
      "query": {
        "accId": "00000000-0000-0000-0000-000000000000",
        "type": "activity"
      }
    }
});
```

{% endtab %}
{% tab title="OpenAPI" %}

```yaml
get:
  summary: Get Latest Activity
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
    - name: type
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
  --url "https://api.sonorancms.com/v2/community/accounts/00000000-0000-0000-0000-000000000000/activity/latest?accId=00000000-0000-0000-0000-000000000000&type=activity" \
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
    "type": "activity",
    "createdAt": "2026-04-14T00:00:00.000Z"
  },
  "meta": {
    "timestamp": "2026-04-14T00:00:00.000Z",
    "path": "/v2/community/accounts/00000000-0000-0000-0000-000000000000/activity/latest"
  }
}
```
