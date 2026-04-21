---

description: Retrieve the contents of a roster.

---



# Get Roster Contents



<mark style="color:green;">`GET`</mark> `https://api.sonorancms.com/v2/community/rosters/1`



> **Rate limit:** `9 requests per minute`  

> Authenticated v2 endpoints are rate limited per credential rather than per IP address.



Retrieve the contents of a roster.



## Route Parameters



| Name | Type | Required | Description |

| --- | --- | --- | --- |

| `rosterId` | number | Yes | Target rosterId. |



## Query Parameters



| Name | Type | Required | Description |

| --- | --- | --- | --- |

| `skip` | number | Yes | See example request for the shape. |

| `limit` | number | Yes | See example request for the shape. |



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

local rosterId = 1
local query = {
  ["skip"] = 0,
  ["limit"] = 25
}

local response = sonoran.cms:getRosterV2(rosterId, query)

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
  const rosterId = 1;
  const query = {
  "skip": 0,
  "limit": 25
};

  const response = await instance.cms.getRosterV2(rosterId, query);

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

rosterId = 1
query = {
  "skip": 0,
  "limit": 25
}

response = instance.cms.getRosterV2(rosterId, query)

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

var rosterId = 1;
var query = new {
  skip = 0,
  limit = 25
};

var response = await sonoran.Cms.getRosterV2(rosterId, query);

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

  title: "Sonoran CMS v2 - Get Roster Contents"

  version: "1.0.0"

  description: "Retrieve the contents of a roster."

servers:

  -

    url: "https://api.sonorancms.com"

paths:

  /v2/community/rosters/{rosterId}:

    get:

      summary: "Get Roster Contents"

      operationId: "getRosterContents"

      parameters:

        -

          description: "Target roster id."

          name: "rosterId"

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

          description: "Maximum number of rows to return."

          name: "limit"

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

                  rows:

                    -

                      uuid: "55555555-5555-5555-5555-555555555555"

                      sortPower: 10

                      name: "ExampleAccount"

                      rank: "Cadet"

                  total: 1

                  skip: 0

                  limit: 25

                  columns:

                    -

                      field: "name"

                      type: "text"

                      mask: ""

                      reverseMask: false

                      label: "Name"

                      options: []

                      metadata: {}

                      cosmetic:

                        font: null

                        textColor: null

                        color: null

                        align: null

                      style: {}

                meta:

                  timestamp: "2026-04-15T00:00:00.000Z"

                  path: "/v2/community/rosters/1"

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

  --url "https://api.sonorancms.com/v2/community/rosters/1?skip=0&limit=25" \

  --header "Authorization: Bearer YOUR_API_KEY" \

  --header "Accept: application/json"
```

{% endtab %}
{% endtabs %}

## Response



The `data` object includes the paginated roster rows, paging metadata, and the roster column definitions that were used to shape the rows. Row keys are dynamic and follow the roster template.



```json

{

  "success": true,

  "data": {

    "rows": [

      {

        "uuid": "55555555-5555-5555-5555-555555555555",

        "sortPower": 10,

        "name": "ExampleAccount",

        "rank": "Cadet"

      }

    ],

    "total": 1,

    "skip": 0,

    "limit": 25,

    "columns": [

      {

        "field": "name",

        "type": "text",

        "mask": "",

        "reverseMask": false,

        "label": "Name",

        "options": [],

        "metadata": {},

        "cosmetic": {

          "font": null,

          "textColor": null,

          "color": null,

          "align": null

        },

        "style": {}

      }

    ]

  },

  "meta": {

    "timestamp": "2026-04-15T00:00:00.000Z",

    "path": "/v2/community/rosters/1"

  }

}

```

