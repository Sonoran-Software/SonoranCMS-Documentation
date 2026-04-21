---

description: Retrieve a list of community accounts.

---



# Get Accounts



<mark style="color:green;">`GET`</mark> `https://api.sonorancms.com/v2/community/accounts`



> **Rate limit:** `22 requests per minute`  

> Authenticated v2 endpoints are rate limited per credential rather than per IP address.



Retrieve a list of community accounts.



## Query Parameters



| Name | Type | Required | Description |

| --- | --- | --- | --- |

| `skip` | number | Yes | See example request for the shape. |

| `take` | number | Yes | See example request for the shape. |

| `sysStatus` | boolean | Yes | See example request for the shape. |



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

local query = {
  ["skip"] = 0,
  ["take"] = 25,
  ["sysStatus"] = true
}

local response = sonoran.cms:getAccountsV2(query)

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
  const query = {
  "skip": 0,
  "take": 25,
  "sysStatus": true
};

  const response = await instance.cms.getAccountsV2(query);

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

query = {
  "skip": 0,
  "take": 25,
  "sysStatus": True
}

response = instance.cms.getAccountsV2(query)

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

var query = new {
  skip = 0,
  take = 25,
  sysStatus = true
};

var response = await sonoran.Cms.getAccountsV2(query);

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

  title: "Sonoran CMS v2 - Get Accounts"

  version: "1.0.0"

  description: "Retrieve a list of community accounts."

servers:

  -

    url: "https://api.sonorancms.com"

paths:

  /v2/community/accounts:

    get:

      summary: "Get Accounts"

      operationId: "getAccounts"

      parameters:

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

        -

          description: "Filter by system status."

          name: "sysStatus"

          in: "query"

          schema:

            type: "boolean"

          required: false

        -

          description: "Filter by community status."

          name: "comStatus"

          in: "query"

          schema:

            type: "boolean"

          required: false

        -

          description: "Filter by banned state."

          name: "banned"

          in: "query"

          schema:

            type: "boolean"

          required: false

        -

          description: "Filter by archived state."

          name: "archived"

          in: "query"

          schema:

            type: "boolean"

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

                  items:

                    -

                      accId: "00000000-0000-0000-0000-000000000000"

                      uniqueId: 1001

                      accName: "ExampleAccount"

                      comName: "Example Community"

                      activeApiIds:

                        - "discord:1234567890"

                      discordId: "1234567890"

                      sysStatus: true

                      comStatus: true

                      archived: false

                      banned: false

                      teamspeakId: null

                  total: 1

                  skip: 0

                  take: 25

                meta:

                  timestamp: "2026-04-15T00:00:00.000Z"

                  path: "/v2/community/accounts"

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

  --url "https://api.sonorancms.com/v2/community/accounts?skip=0&take=25&sysStatus=true" \

  --header "Authorization: Bearer YOUR_API_KEY" \

  --header "Accept: application/json"
```

{% endtab %}
{% endtabs %}

## Response



The `data` object is a paginated account collection. `items` contains the selected account fields plus `teamspeakId`, and `total`, `skip`, and `take` describe the page.



```json

{

  "success": true,

  "data": {

    "items": [

      {

        "accId": "00000000-0000-0000-0000-000000000000",

        "uniqueId": 1001,

        "accName": "ExampleAccount",

        "comName": "Example Community",

        "activeApiIds": [

          "discord:1234567890"

        ],

        "discordId": "1234567890",

        "sysStatus": true,

        "comStatus": true,

        "archived": false,

        "banned": false,

        "teamspeakId": null

      }

    ],

    "total": 1,

    "skip": 0,

    "take": 25

  },

  "meta": {

    "timestamp": "2026-04-15T00:00:00.000Z",

    "path": "/v2/community/accounts"

  }

}

```

