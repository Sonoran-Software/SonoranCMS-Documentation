---

description: Search for community accounts.

---



# Search Accounts



<mark style="color:green;">`GET`</mark> `https://api.sonorancms.com/v2/community/accounts/search`



> **Rate limit:** `27 requests per minute`  

> Authenticated v2 endpoints are rate limited per credential rather than per IP address.



Search for community accounts.



## Query Parameters



| Name | Type | Required | Description |

| --- | --- | --- | --- |

| `username` | string | Yes | See example request for the shape. |



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
  ["username"] = "ExampleUser"
}

local response = sonoran.cms:searchAccountsV2(query)

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
  "username": "ExampleUser"
};

  const response = await instance.cms.searchAccountsV2(query);

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
  "username": "ExampleUser"
}

response = instance.cms.searchAccountsV2(query)

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
  username = "ExampleUser"
};

var response = await sonoran.Cms.searchAccountsV2(query);

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

  title: "Sonoran CMS v2 - Search Accounts"

  version: "1.0.0"

  description: "Search for community accounts."

servers:

  -

    url: "https://api.sonorancms.com"

paths:

  /v2/community/accounts/search:

    get:

      summary: "Search Accounts"

      operationId: "searchAccounts"

      parameters:

        -

          description: "Target account UUID. Provide exactly one identifier."

          name: "accountId"

          in: "query"

          schema:

            type: "string"

            format: "uuid"

          required: false

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

          description: "Target community account id. Provide exactly one identifier."

          name: "accId"

          in: "query"

          schema:

            type: "string"

            format: "uuid"

          required: false

        -

          description: "Target Discord id. Provide exactly one identifier."

          name: "discord"

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

                meta:

                  timestamp: "2026-04-15T00:00:00.000Z"

                  path: "/v2/community/accounts/search"

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

  --url "https://api.sonorancms.com/v2/community/accounts/search?username=ExampleUser" \

  --header "Authorization: Bearer YOUR_API_KEY" \

  --header "Accept: application/json"
```

{% endtab %}
{% endtabs %}

## Response



The `data` object contains the matched accounts and a `total` count. This search endpoint does not page the result set beyond the service-level filters.



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

    "total": 1

  },

  "meta": {

    "timestamp": "2026-04-15T00:00:00.000Z",

    "path": "/v2/community/accounts/search"

  }

}

```

