---
description: Move a form submission to a new stage.
---

# Change Form Stage

<mark style="color:green;">`PATCH`</mark> `https://api.sonorancms.com/v2/community/forms/1/stage`

> **Rate limit:** `27 requests per minute`  
> Authenticated v2 endpoints are rate limited per credential rather than per IP address.

Move a form submission to a new stage.

## Route Parameters

| Name | Type | Required | Description |
| --- | --- | --- | --- |
| `formId` | number | Yes | Target formId. |

## Request Body

| Name | Type | Required | Description |
| --- | --- | --- | --- |
| `accId` | string | Yes | See example request for the shape. |
| `newStageId` | string | Yes | See example request for the shape. |
| `optionalReason` | string | Yes | See example request for the shape. |

## Example Request

{% tabs %}
{% tab title="Sonoran.lua" %}

```lua
local response = sonoran:request({
  "method": "PATCH",
  "path": "/v2/community/forms/1/stage",
  "body": {
    "accId": "00000000-0000-0000-0000-000000000000",
    "newStageId": "review",
    "optionalReason": "Reviewed manually."
  }
})
```

{% endtab %}
{% tab title="Sonoran.js" %}

```javascript
const response = await sonoran.request({
  "method": "PATCH",
  "path": "/v2/community/forms/1/stage",
  "body": {
    "accId": "00000000-0000-0000-0000-000000000000",
    "newStageId": "review",
    "optionalReason": "Reviewed manually."
  }
});
```

{% endtab %}
{% tab title="Sonoran.py" %}

```python
response = sonoran.request({
  "method": "PATCH",
  "path": "/v2/community/forms/1/stage",
  "body": {
    "accId": "00000000-0000-0000-0000-000000000000",
    "newStageId": "review",
    "optionalReason": "Reviewed manually."
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
      "path": "/v2/community/forms/1/stage",
      "body": {
        "accId": "00000000-0000-0000-0000-000000000000",
        "newStageId": "review",
        "optionalReason": "Reviewed manually."
      }
    }
});
```

{% endtab %}
{% tab title="OpenAPI" %}

```yaml
patch:
  summary: Change Form Stage
  security:
    - v2ApiKey: []
  parameters:
    - name: formId
      in: path
      required: true
      schema:
        type: integer
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
  --url "https://api.sonorancms.com/v2/community/forms/1/stage" \
  --header "Authorization: Bearer YOUR_API_KEY" \
  --header "Accept: application/json" \
  --data '{"accId":"00000000-0000-0000-0000-000000000000","newStageId":"review","optionalReason":"Reviewed manually."}'
```

{% endtab %}
{% endtabs %}

## Response

Successful requests return `application/json` and use the standard v2 envelope.

```json
{
  "success": true,
  "data": {
    "formId": 1,
    "accId": "00000000-0000-0000-0000-000000000000",
    "stageId": "review",
    "reason": "Reviewed manually."
  },
  "meta": {
    "timestamp": "2026-04-14T00:00:00.000Z",
    "path": "/v2/community/forms/1/stage"
  }
}
```
