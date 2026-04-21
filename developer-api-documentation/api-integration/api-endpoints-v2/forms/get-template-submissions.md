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
local Sonoran = require("sonoran")

local sonoran = Sonoran.createClient({
  product = Sonoran.productEnums.CMS,
  apiKey = "YOUR_API_KEY",
  communityId = "YOUR_COMMUNITY_ID",
  defaultServerId = 1,
  timeoutMs = 30000,
})

local templateId = 1
local query = {
  ["skip"] = 0,
  ["take"] = 25
}

local response = sonoran.cms:getFormSubmissionsV2(templateId, query)

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
  const templateId = 1;
  const query = {
  "skip": 0,
  "take": 25
};

  const response = await instance.cms.getFormSubmissionsV2(templateId, query);

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

templateId = 1
query = {
  "skip": 0,
  "take": 25
}

response = instance.cms.getFormSubmissionsV2(templateId, query)

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

var templateId = 1;
var query = new {
  skip = 0,
  take = 25
};

var response = await sonoran.Cms.getFormSubmissionsV2(templateId, query);

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

  title: "Sonoran CMS v2 - Get Template Submissions"

  version: "1.0.0"

  description: "Retrieve submissions for a form template."

servers:

  -

    url: "https://api.sonorancms.com"

paths:

  /v2/community/forms/{templateId}/submissions:

    get:

      summary: "Get Template Submissions"

      operationId: "getTemplateSubmissions"

      parameters:

        -

          description: "Target form template id."

          name: "templateId"

          in: "path"

          schema:

            type: "integer"

          required: true

        -

          description: "Number of rows to skip."

          name: "skip"

          in: "query"

          schema:

            type: "integer"

          required: false

        -

          description: "Number of rows to take."

          name: "take"

          in: "query"

          schema:

            type: "integer"

          required: false

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

                  count: 1

                  forms:

                    -

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

                  path: "/v2/community/forms/1/submissions"

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

