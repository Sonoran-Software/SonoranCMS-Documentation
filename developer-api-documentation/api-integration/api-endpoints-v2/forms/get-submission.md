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
{% tab title="OpenAPI" %}

```yaml
openapi: "3.0.3"
info:
  title: "Sonoran CMS v2 - Get Submission"
  version: "1.0.0"
  description: "Retrieve a single form submission."
servers:
  -
    url: "https://api.sonorancms.com"
paths:
  /v2/community/forms/submissions/{submissionId}:
    get:
      summary: "Get Submission"
      operationId: "getFormSubmission"
      parameters:
        -
          description: "Target form submission id."
          name: "submissionId"
          in: "path"
          schema:
            type: "integer"
          required: true
      security:
        -
          bearerAuth: []
      responses:
        "200":
          description: "Successful response"
          content:
            application/json:
              schema:
                type: "object"
              example:
                success: true
                data:
                  formId: 42
                  sysStatus: true
                  submissionTime: "2026-04-15T00:00:00.000Z"
                  lastActionTime: "2026-04-15T00:00:00.000Z"
                  formSubmitter: "00000000-0000-0000-0000-000000000000"
                  formContextUser: null
                  relatedUsers: []
                  formStructure:
                    _label: "Example Form Submission"
                    fields: []
                  formComments:
                    comments: []
                  stageId: "22222222-2222-2222-2222-222222222222"
                  stageGroupId: "11111111-1111-1111-1111-111111111111"
                  stageInfoBackup:
                    stages: []
                    groups: []
                  formTemplateId: 100
                  formType: 0
                  formReplySettings:
                    locked: false
                    submitter: true
                    rankIds: []
                  showInProfile: false
                  stages: []
                meta:
                  timestamp: "2026-04-15T00:00:00.000Z"
                  path: "/v2/community/forms/submissions/1"
components:
  securitySchemes:
    bearerAuth:
      type: "http"
      scheme: "bearer"
      bearerFormat: "JWT"
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

The `data` object is the audited form submission. It includes the hydrated template `stages` plus the normalized `formReplySettings` block.

```json
{
  "success": true,
  "data": {
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
  },
  "meta": {
    "timestamp": "2026-04-15T00:00:00.000Z",
    "path": "/v2/community/forms/submissions/1"
  }
}
```
