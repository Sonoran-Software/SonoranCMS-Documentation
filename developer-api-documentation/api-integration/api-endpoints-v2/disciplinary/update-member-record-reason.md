---

description: Update the reason on a disciplinary record.

---



# Update Member Record Reason



<mark style="color:green;">`PATCH`</mark> `https://api.sonorancms.com/v2/community/disciplinary/records/11111111-1111-1111-1111-111111111111/reason`



> **Rate limit:** `18 requests per minute`  

> Authenticated v2 endpoints are rate limited per credential rather than per IP address.



Update the reason on a disciplinary record.



## Route Parameters



| Name | Type | Required | Description |

| --- | --- | --- | --- |

| `recordId` | string (uuid) | Yes | Target recordId. |



## Request Body



| Name | Type | Required | Description |

| --- | --- | --- | --- |

| `reason` | string | Yes | See example request for the shape. |



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

local recordId = "00000000-0000-0000-0000-000000000000"
local payload = {
  ["reason"] = "Updated reason"
}

local response = sonoran.cms:setDisciplinaryRecordReasonV2(recordId, payload)

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
  const recordId = "00000000-0000-0000-0000-000000000000";
  const payload = {
  "reason": "Updated reason"
};

  const response = await instance.cms.setDisciplinaryRecordReasonV2(recordId, payload);

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

recordId = "00000000-0000-0000-0000-000000000000"
payload = {
  "reason": "Updated reason"
}

response = instance.cms.setDisciplinaryRecordReasonV2(recordId, payload)

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

var recordId = "00000000-0000-0000-0000-000000000000";
var payload = new {
  reason = "Updated reason"
};

var response = await sonoran.Cms.setDisciplinaryRecordReasonV2(recordId, payload);

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

  title: "Sonoran CMS v2 - Update Member Record Reason"

  version: "1.0.0"

  description: "Update the reason on a disciplinary record."

servers:

  -

    url: "https://api.sonorancms.com"

paths:

  /v2/community/disciplinary/records/{recordId}/reason:

    patch:

      summary: "Update Member Record Reason"

      operationId: "updateMemberRecordReason"

      parameters:

        -

          description: "Target disciplinary record id."

          name: "recordId"

          in: "path"

          schema:

            type: "string"

            format: "uuid"

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

                  -

                    id: "55555555-5555-5555-5555-555555555555"

                    status: true

                    accId: "00000000-0000-0000-0000-000000000000"

                    source: "api"

                    sourceId: "api-request"

                    points: 5

                    reason: "Example disciplinary action"

                    metadata:

                      executionSource: "discord"

                    history:

                      2026-04-15T00:00:00.000Z:

                        action: "init"

                        points: 5

                        reason: "Example disciplinary action"

                        metadata:

                          executionSource: "discord"

                        timestamp: "2026-04-15T00:00:00.000Z"

                        source: "api"

                        sourceId: "api-request"

                    createdAt: "2026-04-15T00:00:00.000Z"

                    updatedAt: null

                    expired: false

                meta:

                  timestamp: "2026-04-15T00:00:00.000Z"

                  path: "/v2/community/disciplinary/records/11111111-1111-1111-1111-111111111111/reason"

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

  --url "https://api.sonorancms.com/v2/community/disciplinary/records/11111111-1111-1111-1111-111111111111/reason" \

  --header "Authorization: Bearer YOUR_API_KEY" \

  --header "Accept: application/json" \

  --data '{"reason":"Updated reason"}'
```

{% endtab %}
{% endtabs %}

## Response



The `data` array contains the updated disciplinary record row(s) returned by the update query. The endpoint is reused for points, reason, and status updates.



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

    "path": "/v2/community/disciplinary/records/11111111-1111-1111-1111-111111111111/reason"

  }

}

```

