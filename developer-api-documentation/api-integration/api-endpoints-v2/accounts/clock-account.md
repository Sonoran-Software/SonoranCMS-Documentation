---

description: Clock an account in or out.

---



# Clock Account



<mark style="color:green;">`POST`</mark> `https://api.sonorancms.com/v2/community/accounts/00000000-0000-0000-0000-000000000000/clock`



> **Rate limit:** `22 requests per minute`  

> Authenticated v2 endpoints are rate limited per credential rather than per IP address.



Clock an account in or out.



## Route Parameters



| Name | Type | Required | Description |

| --- | --- | --- | --- |

| `accountId` | string (uuid) | Yes | Target accountId. |



## Request Body



| Name | Type | Required | Description |

| --- | --- | --- | --- |

| `accId` | string | Yes | See example request for the shape. |

| `intention` | string | Yes | See example request for the shape. |

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
local payload = {
  ["accId"] = "00000000-0000-0000-0000-000000000000",
  ["intention"] = "in",
  ["type"] = "regular"
}

local response = sonoran.cms:clockAccountV2(accountId, payload)

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
  const payload = {
  "accId": "00000000-0000-0000-0000-000000000000",
  "intention": "in",
  "type": "regular"
};

  const response = await instance.cms.clockAccountV2(accountId, payload);

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
payload = {
  "accId": "00000000-0000-0000-0000-000000000000",
  "intention": "in",
  "type": "regular"
}

response = instance.cms.clockAccountV2(accountId, payload)

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
var payload = new {
  accId = "00000000-0000-0000-0000-000000000000",
  intention = "in",
  type = "regular"
};

var response = await sonoran.Cms.clockAccountV2(accountId, payload);

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

  title: "Sonoran CMS v2 - Clock Account"

  version: "1.0.0"

  description: "Clock an account in or out."

servers:

  -

    url: "https://api.sonorancms.com"

paths:

  /v2/community/accounts/{accountId}/clock:

    post:

      summary: "Clock Account"

      operationId: "clockAccount"

      parameters:

        -

          description: "Target account UUID."

          name: "accountId"

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

                  id: "55555555-5555-5555-5555-555555555555"

                  startTime: "2026-04-15T00:00:00.000Z"

                  endTime: null

                  completed: false

                  notes: []

                  type: "patrol"

                meta:

                  timestamp: "2026-04-15T00:00:00.000Z"

                  path: "/v2/community/accounts/00000000-0000-0000-0000-000000000000/clock"

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
curl --request POST \

  --url "https://api.sonorancms.com/v2/community/accounts/00000000-0000-0000-0000-000000000000/clock" \

  --header "Authorization: Bearer YOUR_API_KEY" \

  --header "Accept: application/json" \

  --data '{"accId":"00000000-0000-0000-0000-000000000000","intention":"in","type":"regular"}'
```

{% endtab %}
{% endtabs %}

## Response



The `data` value is usually the saved clock row. In no-op cases, the service can also return `true` when the requested clock action does not need to write a new row.



```json

{

  "success": true,

  "data": {

    "id": "55555555-5555-5555-5555-555555555555",

    "startTime": "2026-04-15T00:00:00.000Z",

    "endTime": null,

    "completed": false,

    "notes": [],

    "type": "patrol"

  },

  "meta": {

    "timestamp": "2026-04-15T00:00:00.000Z",

    "path": "/v2/community/accounts/00000000-0000-0000-0000-000000000000/clock"

  }

}

```

