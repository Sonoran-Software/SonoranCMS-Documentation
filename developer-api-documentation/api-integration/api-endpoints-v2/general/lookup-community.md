---

description: Look up the community by ID or UUID.

---



# Lookup Community



<mark style="color:green;">`GET`</mark> `https://api.sonorancms.com/v2/community/lookup`



> **Rate limit:** `13 requests per minute`  

> Authenticated v2 endpoints are rate limited per credential rather than per IP address.



Look up the community by ID or UUID.



## Query Parameters



| Name | Type | Required | Description |

| --- | --- | --- | --- |

| `id` | string | Yes | See example request for the shape. |



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
  ["id"] = "YOUR_COMMUNITY_ID"
}

local response = sonoran.cms:lookupCommunityV2(query)

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
  "id": "YOUR_COMMUNITY_ID"
};

  const response = await instance.cms.lookupCommunityV2(query);

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
  "id": "YOUR_COMMUNITY_ID"
}

response = instance.cms.lookupCommunityV2(query)

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
  id = "YOUR_COMMUNITY_ID"
};

var response = await sonoran.Cms.lookupCommunityV2(query);

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

  title: "Sonoran CMS v2 - Lookup Community"

  version: "1.0.0"

  description: "Look up the community by ID or UUID."

servers:

  -

    url: "https://api.sonorancms.com"

paths:

  /v2/community/lookup:

    get:

      summary: "Lookup Community"

      operationId: "lookupCommunity"

      parameters:

        -

          description: "Community id. Provide exactly one identifier."

          name: "id"

          in: "query"

          schema:

            type: "string"

          required: false

        -

          description: "Community UUID. Provide exactly one identifier."

          name: "uuid"

          in: "query"

          schema:

            type: "string"

            format: "uuid"

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

                  id: "CMS-1000"

                  uuid: "00000000-0000-0000-0000-000000000000"

                  name: "Example Community"

                  subVersion: 5

                  tier: "SonoranOne"

                  servers: 3

                meta:

                  timestamp: "2026-04-15T00:00:00.000Z"

                  path: "/v2/community/lookup"

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

  --url "https://api.sonorancms.com/v2/community/lookup?id=YOUR_COMMUNITY_ID" \

  --header "Authorization: Bearer YOUR_API_KEY" \

  --header "Accept: application/json"
```

{% endtab %}
{% endtabs %}

## Response



The `data` object is the community summary returned by `V2Service.summary()`. It includes the community identifier, UUID, name, sub-version, resolved tier, and server count.



This lookup returns the same community summary shape as `GET /v2/community`, but it can resolve the community by id or UUID.



```json

{

  "success": true,

  "data": {

    "id": "CMS-1000",

    "uuid": "00000000-0000-0000-0000-000000000000",

    "name": "Example Community",

    "subVersion": 5,

    "tier": "SonoranOne",

    "servers": 3

  },

  "meta": {

    "timestamp": "2026-04-15T00:00:00.000Z",

    "path": "/v2/community/lookup"

  }

}

```

