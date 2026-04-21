---

description: Retrieve the ER:LC queue.

---



# Get Player Queue



<mark style="color:green;">`GET`</mark> `https://api.sonorancms.com/v2/community/erlc/players/queue`



> **Rate limit:** `27 requests per minute`  

> Authenticated v2 endpoints are rate limited per credential rather than per IP address.



Retrieve the ER:LC queue.



## Query Parameters



| Name | Type | Required | Description |

| --- | --- | --- | --- |

| `robloxJoinCode` | string | Yes | See example request for the shape. |



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
  ["robloxJoinCode"] = "ABC123"
}

local response = sonoran.cms:getPlayerQueueV2(query)

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
  "robloxJoinCode": "ABC123"
};

  const response = await instance.cms.getPlayerQueueV2(query);

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
  "robloxJoinCode": "ABC123"
}

response = instance.cms.getPlayerQueueV2(query)

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
  robloxJoinCode = "ABC123"
};

var response = await sonoran.Cms.getPlayerQueueV2(query);

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

  title: "Sonoran CMS v2 - Get Player Queue"

  version: "1.0.0"

  description: "Retrieve the ER:LC queue."

servers:

  -

    url: "https://api.sonorancms.com"

paths:

  /v2/community/erlc/players/queue:

    get:

      summary: "Get Player Queue"

      operationId: "getPlayerQueue"

      parameters:

        -

          description: "Target Roblox join code."

          name: "robloxJoinCode"

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

                data: 3

                meta:

                  timestamp: "2026-04-15T00:00:00.000Z"

                  path: "/v2/community/erlc/players/queue"

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

  --url "https://api.sonorancms.com/v2/community/erlc/players/queue?robloxJoinCode=ABC123" \

  --header "Authorization: Bearer YOUR_API_KEY" \

  --header "Accept: application/json"
```

{% endtab %}
{% endtabs %}

## Response



The `data` value is the current queue length for the target server, not the queue entries themselves.



```json

{

  "success": true,

  "data": 3,

  "meta": {

    "timestamp": "2026-04-15T00:00:00.000Z",

    "path": "/v2/community/erlc/players/queue"

  }

}

```

