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
local Sonoran = require("sonoran")

local sonoran = Sonoran.createClient({
  product = Sonoran.productEnums.CMS,
  apiKey = "YOUR_API_KEY",
  communityId = "YOUR_COMMUNITY_ID",
  defaultServerId = 1,
  timeoutMs = 30000,
})

local accountId = "00000000-0000-0000-0000-000000000000"
local query = {
  ["accId"] = "00000000-0000-0000-0000-000000000000",
  ["type"] = "activity"
}

local response = sonoran.cms:getLatestActivityV2(accountId, query)

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
  const accountId = "00000000-0000-0000-0000-000000000000";
  const query = {
  "accId": "00000000-0000-0000-0000-000000000000",
  "type": "activity"
};

  const response = await instance.cms.getLatestActivityV2(accountId, query);

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

accountId = "00000000-0000-0000-0000-000000000000"
query = {
  "accId": "00000000-0000-0000-0000-000000000000",
  "type": "activity"
}

response = instance.cms.getLatestActivityV2(accountId, query)

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

var accountId = "00000000-0000-0000-0000-000000000000";
var query = new {
  accId = "00000000-0000-0000-0000-000000000000",
  type = "activity"
};

var response = await sonoran.Cms.getLatestActivityV2(accountId, query);

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

  title: "Sonoran CMS v2 - Get Latest Activity"

  version: "1.0.0"

  description: "Retrieve the latest activity for an account."

servers:

  -

    url: "https://api.sonorancms.com"

paths:

  /v2/community/accounts/{accountId}/activity/latest:

    get:

      summary: "Get Latest Activity"

      operationId: "getLatestActivity"

      parameters:

        -

          description: "Target account UUID."

          name: "accountId"

          in: "path"

          schema:

            type: "string"

            format: "uuid"

          required: true

        -

          description: "Return clock-in activity or general activity."

          name: "type"

          in: "query"

          schema:

            type: "string"

          required: false

        -

          description: "Query parameter serverId."

          name: "serverId"

          in: "query"

          schema:

            type: "string"

          required: false

        -

          description: "Filter clock-in history by clock-in type id."

          name: "clockInType"

          in: "query"

          schema:

            type: "string"

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

                  -

                    id: "55555555-5555-5555-5555-555555555555"

                    startTime: "2026-04-15T00:00:00.000Z"

                    endTime: null

                    completed: false

                    notes: []

                    type: "patrol"

                meta:

                  timestamp: "2026-04-15T00:00:00.000Z"

                  path: "/v2/community/accounts/00000000-0000-0000-0000-000000000000/activity/latest"

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

  --url "https://api.sonorancms.com/v2/community/accounts/00000000-0000-0000-0000-000000000000/activity/latest?accId=00000000-0000-0000-0000-000000000000&type=activity" \

  --header "Authorization: Bearer YOUR_API_KEY" \

  --header "Accept: application/json"
```

{% endtab %}
{% endtabs %}

## Response



When `type=clockin` the `data` array contains the three newest clock rows. When `type=activity` the same endpoint returns recent activity log rows instead of clock rows.



```json

{

  "success": true,

  "data": [

    {

      "id": "55555555-5555-5555-5555-555555555555",

      "startTime": "2026-04-15T00:00:00.000Z",

      "endTime": null,

      "completed": false,

      "notes": [],

      "type": "patrol"

    }

  ],

  "meta": {

    "timestamp": "2026-04-15T00:00:00.000Z",

    "path": "/v2/community/accounts/00000000-0000-0000-0000-000000000000/activity/latest"

  }

}

```

