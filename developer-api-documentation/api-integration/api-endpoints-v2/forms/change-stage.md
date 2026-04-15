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
{% tab title="OpenAPI" %}

```yaml
openapi: "3.0.3"
info:
  title: "Sonoran CMS v2 - Change Stage"
  version: "1.0.0"
  description: "Move a form submission to a new stage."
servers:
  -
    url: "https://api.sonorancms.com"
paths:
  /v2/community/forms/{formId}/stage:
    patch:
      summary: "Change Stage"
      operationId: "changeFormStage"
      parameters:
        -
          description: "Target form id."
          name: "formId"
          in: "path"
          schema:
            type: "integer"
          required: true
      requestBody:
        required: true
        content:
          application/json:
            schema:
              type: "object"
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
                  authorized: true
                  failed: false
                  data:
                    form:
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
                    newStage:
                      id: "33333333-3333-3333-3333-333333333333"
                      label: "Interview"
                    availableStages:
                      -
                        id: "44444444-4444-4444-4444-444444444444"
                        label: "Training"
                meta:
                  timestamp: "2026-04-15T00:00:00.000Z"
                  path: "/v2/community/forms/1/stage"
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
curl --request PATCH \
  --url "https://api.sonorancms.com/v2/community/forms/1/stage" \
  --header "Authorization: Bearer YOUR_API_KEY" \
  --header "Accept: application/json" \
  --data '{"accId":"00000000-0000-0000-0000-000000000000","newStageId":"review","optionalReason":"Reviewed manually."}'
```

{% endtab %}
{% endtabs %}

## Response

The `data` object includes the saved form, the chosen stage, and the remaining available stages. The outer service contract also carries `authorized` and `failed` flags.

```json
{
  "success": true,
  "data": {
    "authorized": true,
    "failed": false,
    "data": {
      "form": {
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
      "newStage": {
        "id": "33333333-3333-3333-3333-333333333333",
        "label": "Interview"
      },
      "availableStages": [
        {
          "id": "44444444-4444-4444-4444-444444444444",
          "label": "Training"
        }
      ]
    }
  },
  "meta": {
    "timestamp": "2026-04-15T00:00:00.000Z",
    "path": "/v2/community/forms/1/stage"
  }
}
```
