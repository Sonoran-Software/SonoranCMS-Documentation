---

description: Retrieve the configured custom log types.

---



# Get Custom Log Types



<mark style="color:green;">`GET`</mark> `https://api.sonorancms.com/v2/community/custom-log-types`



> **Rate limit:** `13 requests per minute`  

> Authenticated v2 endpoints are rate limited per credential rather than per IP address.



Retrieve the configured custom log types.



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

local response = sonoran.cms:getCustomLogTypesV2()

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
  const response = await instance.cms.getCustomLogTypesV2();

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

response = instance.cms.getCustomLogTypesV2()

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

var response = await sonoran.Cms.getCustomLogTypesV2();

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

  title: "Sonoran CMS v2 - Get Custom Log Types"

  version: "1.0.0"

  description: "Retrieve the configured custom log types."

servers:

  -

    url: "https://api.sonorancms.com"

paths:

  /v2/community/custom-log-types:

    get:

      summary: "Get Custom Log Types"

      operationId: "getCustomLogTypes"

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

                    id: "33333333-3333-3333-3333-333333333333"

                    label: "Internal Warning"

                    shortCode: "warn"

                    melonlyId: "101"

                meta:

                  timestamp: "2026-04-15T00:00:00.000Z"

                  path: "/v2/community/custom-log-types"

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

  --url "https://api.sonorancms.com/v2/community/custom-log-types" \

  --header "Authorization: Bearer YOUR_API_KEY" \

  --header "Accept: application/json"
```

{% endtab %}
{% endtabs %}

## Response



The `data` array contains the configured custom log types used by ERLC and disciplinary integrations.



```json

{

  "success": true,

  "data": [

    {

      "id": "33333333-3333-3333-3333-333333333333",

      "label": "Internal Warning",

      "shortCode": "warn",

      "melonlyId": "101"

    }

  ],

  "meta": {

    "timestamp": "2026-04-15T00:00:00.000Z",

    "path": "/v2/community/custom-log-types"

  }

}

```

