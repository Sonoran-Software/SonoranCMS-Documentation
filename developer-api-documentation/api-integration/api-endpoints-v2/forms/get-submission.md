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
local Sonoran = require("sonoran")

local sonoran = Sonoran.createClient({
  product = Sonoran.productEnums.CMS,
  apiKey = "YOUR_API_KEY",
  communityId = "YOUR_COMMUNITY_ID",
  defaultServerId = 1,
  timeoutMs = 30000,
})

local submissionId = 1

local response = sonoran.cms:getSubmissionV2(submissionId)

if response.success then
  print(response.data)
else
  print(response.reason)
end
```

{% endtab %}
{% tab title="Sonoran.js" %}

```javascript
const Sonoran = require("sonoran.js");

const instance = Sonoran.instance({
  apiKey: "YOUR_API_KEY",
  communityId: "YOUR_COMMUNITY_ID",
  product: Sonoran.productEnums.CMS,
  serverId: 1,
});

async function main() {
  const submissionId = 1;

  const response = await instance.cms.getSubmissionV2(submissionId);

  if (response.success) {
    console.log(response.data);
  } else {
    console.error(response.reason);
  }
}

main().catch((error) => {
  console.error(error);
});
```

{% endtab %}
{% tab title="Sonoran.py" %}

```python
from sonoran import Instance, productEnums

instance = Instance(
    apiKey="YOUR_API_KEY",
    communityId="YOUR_COMMUNITY_ID",
    product=productEnums.CMS,
    serverId=1,
)

submissionId = 1

response = instance.cms.getSubmissionV2(submissionId)

if response.success:
    print(response.data)
else:
    print(response.reason)
```

{% endtab %}
{% tab title="Sonoran.Net" %}

```csharp
using Sonoran;
using System.Text.Json;

using var sonoran = new SonoranClient(new SonoranClientOptions
{
    product = SonoranProduct.CMS,
    apiKey = "YOUR_API_KEY",
    communityId = "YOUR_COMMUNITY_ID",
    defaultServerId = 1
});

var submissionId = 1;

var response = await sonoran.Cms.getSubmissionV2(submissionId);

if (response.success)
{
    Console.WriteLine(JsonSerializer.Serialize(response.data));
}
else
{
    Console.WriteLine(response.reason);
}
```

{% endtab %}
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

