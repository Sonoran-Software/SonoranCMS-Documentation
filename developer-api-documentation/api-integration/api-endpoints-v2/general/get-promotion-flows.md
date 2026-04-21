---

description: Retrieve the configured promotion flows.

---



# Get Promotion Flows



<mark style="color:green;">`GET`</mark> `https://api.sonorancms.com/v2/community/promotion-flows`



> **Rate limit:** `13 requests per minute`  

> Authenticated v2 endpoints are rate limited per credential rather than per IP address.



Retrieve the configured promotion flows.



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

local response = sonoran.cms:getPromotionFlowsV2()

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
  const response = await instance.cms.getPromotionFlowsV2();

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

response = instance.cms.getPromotionFlowsV2()

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

var response = await sonoran.Cms.getPromotionFlowsV2();

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

  title: "Sonoran CMS v2 - Get Promotion Flows"

  version: "1.0.0"

  description: "Retrieve the configured promotion flows."

servers:

  -

    url: "https://api.sonorancms.com"

paths:

  /v2/community/promotion-flows:

    get:

      summary: "Get Promotion Flows"

      operationId: "getPromotionFlows"

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

                    id: "44444444-4444-4444-4444-444444444444"

                    communityUuid: "00000000-0000-0000-0000-000000000000"

                    labelFrom: "Cadet"

                    labelTo: "Officer"

                    ranksToAdd:

                      - "22222222-2222-2222-2222-222222222222"

                    ranksToRemove: []

                    actions:

                      data: []

                      promotionType: "both"

                    promotionType: "both"

                meta:

                  timestamp: "2026-04-15T00:00:00.000Z"

                  path: "/v2/community/promotion-flows"

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

  --url "https://api.sonorancms.com/v2/community/promotion-flows" \

  --header "Authorization: Bearer YOUR_API_KEY" \

  --header "Accept: application/json"
```

{% endtab %}
{% endtabs %}

## Response



The `data` array contains promotion flow entities with the derived `promotionType` field added by the v2 service.



```json

{

  "success": true,

  "data": [

    {

      "id": "44444444-4444-4444-4444-444444444444",

      "communityUuid": "00000000-0000-0000-0000-000000000000",

      "labelFrom": "Cadet",

      "labelTo": "Officer",

      "ranksToAdd": [

        "22222222-2222-2222-2222-222222222222"

      ],

      "ranksToRemove": [],

      "actions": {

        "data": [],

        "promotionType": "both"

      },

      "promotionType": "both"

    }

  ],

  "meta": {

    "timestamp": "2026-04-15T00:00:00.000Z",

    "path": "/v2/community/promotion-flows"

  }

}

```

