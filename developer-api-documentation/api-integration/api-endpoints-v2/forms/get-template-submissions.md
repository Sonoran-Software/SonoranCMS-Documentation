---
description: Retrieve submissions for a form template.
---

# Get Template Submissions

<mark style="color:green;">`GET`</mark> `https://api.sonorancms.com/v2/community/forms/1/submissions`

> **Rate limit:** `13 requests per minute`  
> Authenticated v2 endpoints are rate limited per credential rather than per IP address.

Retrieve submissions for a form template.

## Route Parameters

| Name | Type | Required | Description |
| --- | --- | --- | --- |
| `templateId` | number | Yes | Target templateId. |

## Query Parameters

| Name | Type | Required | Description |
| --- | --- | --- | --- |
| `skip` | number | Yes | See example request for the shape. |
| `take` | number | Yes | See example request for the shape. |

## Example Request

{% tabs %}
{% tab title="Sonoran.lua" %}

```lua
local response = sonoran:request({
  "method": "GET",
  "path": "/v2/community/forms/1/submissions",
  "query": {
    "skip": 0,
    "take": 25
  }
})
```

{% endtab %}
{% tab title="Sonoran.js" %}

```javascript
const response = await sonoran.request({
  "method": "GET",
  "path": "/v2/community/forms/1/submissions",
  "query": {
    "skip": 0,
    "take": 25
  }
});
```

{% endtab %}
{% tab title="Sonoran.py" %}

```python
response = sonoran.request({
  "method": "GET",
  "path": "/v2/community/forms/1/submissions",
  "query": {
    "skip": 0,
    "take": 25
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
      "path": "/v2/community/forms/1/submissions",
      "query": {
        "skip": 0,
        "take": 25
      }
    }
});
```

{% endtab %}
{% tab title="OpenAPI" %}

```yaml
get:
  summary: Get Template Submissions
  security:
    - v2ApiKey: []
  parameters:
    - name: templateId
      in: path
      required: true
      schema:
        type: integer
  parameters:
    - name: skip
      in: query
      required: false
      schema:
        type: integer
    - name: take
      in: query
      required: false
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
  --url "https://api.sonorancms.com/v2/community/forms/1/submissions?skip=0&take=25" \
  --header "Authorization: Bearer YOUR_API_KEY" \
  --header "Accept: application/json"
```

{% endtab %}
{% endtabs %}

## Response

The `data` object contains the total submission count and the audited form list for the requested template id.

```json
{
  "success": true,
  "data": {
    "count": 1,
    "forms": [
      {
        "formId": 42,
        "sysStatus": true,
        "submissionTime": "2026-04-15T00:00:00.000Z",
        "lastActionTime": "2026-04-15T00:00:00.000Z",
        "formSubmitter": "00000000-0000-0000-0000-000000000000",
        "formContextUser": null,
        "relatedUsers": [],
        "formStructure": {
          "_label": "Example Form Submission",
          "fields": []
        },
        "formComments": {
          "comments": []
        },
        "stageId": "22222222-2222-2222-2222-222222222222",
        "stageGroupId": "11111111-1111-1111-1111-111111111111",
        "stageInfoBackup": {
          "stages": [],
          "groups": []
        },
        "formTemplateId": 100,
        "formType": 0,
        "formReplySettings": {
          "locked": false,
          "submitter": true,
          "rankIds": []
        },
        "showInProfile": false,
        "stages": []
      }
    ]
  },
  "meta": {
    "timestamp": "2026-04-15T00:00:00.000Z",
    "path": "/v2/community/forms/1/submissions"
  }
}
```
