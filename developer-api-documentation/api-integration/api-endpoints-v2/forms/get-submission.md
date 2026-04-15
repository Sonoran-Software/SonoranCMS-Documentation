---
description: Retrieve a single form submission.
---

# Get Submission

<mark style="color:green;">`GET`</mark> `https://api.sonorancms.com/v2/community/forms/submissions/1`

> **Rate limit:** `27 requests per minute`  
> Authenticated v2 endpoints are rate limited per credential rather than per IP address.

Retrieve a single form submission.

## Route Parameters

| Name | Type | Required | Description |
| --- | --- | --- | --- |
| `submissionId` | number | Yes | Target submissionId. |

## Example Request

{% tabs %}
{% tab title="Sonoran.lua" %}

```lua
local response = sonoran:request({
  "method": "GET",
  "path": "/v2/community/forms/submissions/1"
})
```

{% endtab %}
{% tab title="Sonoran.js" %}

```javascript
const response = await sonoran.request({
  "method": "GET",
  "path": "/v2/community/forms/submissions/1"
});
```

{% endtab %}
{% tab title="Sonoran.py" %}

```python
response = sonoran.request({
  "method": "GET",
  "path": "/v2/community/forms/submissions/1"
})
```

{% endtab %}
{% tab title="Sonoran.Net" %}

```csharp
var response = await sonoran.RequestAsync(new SonoranRequest
{
    {
      "method": "GET",
      "path": "/v2/community/forms/submissions/1"
    }
});
```

{% endtab %}
{% tab title="OpenAPI" %}

```yaml
get:
  summary: Get Submission
  security:
    - v2ApiKey: []
  parameters:
    - name: submissionId
      in: path
      required: true
      schema:
        type: integer
  responses:
    '200':
      description: Successful response
```

{% endtab %}
{% tab title="cURL" %}

```bash
curl --request GET \
  --url "https://api.sonorancms.com/v2/community/forms/submissions/1" \
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
    "submissionId": 1,
    "formId": 1,
    "accId": "00000000-0000-0000-0000-000000000000",
    "stageId": "review"
  },
  "meta": {
    "timestamp": "2026-04-14T00:00:00.000Z",
    "path": "/v2/community/forms/submissions/1"
  }
}
```
