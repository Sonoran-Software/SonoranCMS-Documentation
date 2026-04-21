---

description: Retrieve disciplinary point totals for a member.

---



# Get Member Points



<mark style="color:green;">`GET`</mark> `https://api.sonorancms.com/v2/community/disciplinary/accounts/00000000-0000-0000-0000-000000000000/points`



> **Rate limit:** `27 requests per minute`  

> Authenticated v2 endpoints are rate limited per credential rather than per IP address.



Retrieve disciplinary point totals for a member.



## Route Parameters



| Name | Type | Required | Description |

| --- | --- | --- | --- |

| `accountId` | string (uuid) | Yes | Target accountId. |



## Query Parameters



| Name | Type | Required | Description |

| --- | --- | --- | --- |

| `accId` | string | Yes | See example request for the shape. |



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
  ["accId"] = "00000000-0000-0000-0000-000000000000"
}

local response = sonoran.cms:getDisciplinaryPointsV2(accountId, query)

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
  "accId": "00000000-0000-0000-0000-000000000000"
};

  const response = await instance.cms.getDisciplinaryPointsV2(accountId, query);

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
  "accId": "00000000-0000-0000-0000-000000000000"
}

response = instance.cms.getDisciplinaryPointsV2(accountId, query)

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
  accId = "00000000-0000-0000-0000-000000000000"
};

var response = await sonoran.Cms.getDisciplinaryPointsV2(accountId, query);

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

  title: "Sonoran CMS v2 - Get Member Points"

  version: "1.0.0"

  description: "Retrieve disciplinary point totals for a member."

servers:

  -

    url: "https://api.sonorancms.com"

paths:

  /v2/community/disciplinary/accounts/{accountId}/points:

    get:

      summary: "Get Member Points"

      operationId: "getMemberPoints"

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

          description: "Target API identifier. Provide exactly one identifier."

          name: "apiId"

          in: "query"

          schema:

            type: "string"

          required: false

        -

          description: "Target username. Provide exactly one identifier."

          name: "username"

          in: "query"

          schema:

            type: "string"

          required: false

        -

          description: "Target Discord id. Provide exactly one identifier."

          name: "discordId"

          in: "query"

          schema:

            type: "string"

          required: false

        -

          description: "Target community unique id. Provide exactly one identifier."

          name: "uniqueId"

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

                data: 12

                meta:

                  timestamp: "2026-04-15T00:00:00.000Z"

                  path: "/v2/community/disciplinary/accounts/00000000-0000-0000-0000-000000000000/points"

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

  --url "https://api.sonorancms.com/v2/community/disciplinary/accounts/00000000-0000-0000-0000-000000000000/points?accId=00000000-0000-0000-0000-000000000000" \

  --header "Authorization: Bearer YOUR_API_KEY" \

  --header "Accept: application/json"
```

{% endtab %}
{% endtabs %}

## Response



The `data` value is the computed disciplinary point total for the account.



```json

{

  "success": true,

  "data": 12,

  "meta": {

    "timestamp": "2026-04-15T00:00:00.000Z",

    "path": "/v2/community/disciplinary/accounts/00000000-0000-0000-0000-000000000000/points"

  }

}

```

