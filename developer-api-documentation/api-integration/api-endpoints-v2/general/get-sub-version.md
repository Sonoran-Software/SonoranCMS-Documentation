---

description: Retrieve the community subscription tier.

---



# Get Sub Version



<mark style="color:green;">`GET`</mark> `https://api.sonorancms.com/v2/community/sub-version`



> **Rate limit:** `13 requests per minute`  

> Authenticated v2 endpoints are rate limited per credential rather than per IP address.



Retrieve the community subscription tier.



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

local response = sonoran.cms:getSubVersionV2()

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
  const response = await instance.cms.getSubVersionV2();

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

response = instance.cms.getSubVersionV2()

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

var response = await sonoran.Cms.getSubVersionV2();

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

  title: "Sonoran CMS v2 - Get Sub Version"

  version: "1.0.0"

  description: "Retrieve the community subscription tier."

servers:

  -

    url: "https://api.sonorancms.com"

paths:

  /v2/community/sub-version:

    get:

      summary: "Get Sub Version"

      operationId: "getSubVersion"

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

                  subVersion: 5

                  tier: "SonoranOne"

                meta:

                  timestamp: "2026-04-15T00:00:00.000Z"

                  path: "/v2/community/sub-version"

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

  --url "https://api.sonorancms.com/v2/community/sub-version" \

  --header "Authorization: Bearer YOUR_API_KEY" \

  --header "Accept: application/json"
```

{% endtab %}
{% endtabs %}

## Response



The `data` object is the current community sub-version and the resolved tier name from `SubNumLevelToName()`.



```json

{

  "success": true,

  "data": {

    "subVersion": 5,

    "tier": "SonoranOne"

  },

  "meta": {

    "timestamp": "2026-04-15T00:00:00.000Z",

    "path": "/v2/community/sub-version"

  }

}

```

