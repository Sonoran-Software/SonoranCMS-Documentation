---

description: Retrieve the identifiers stored for an account.

---



# Get Account Identifiers



<mark style="color:green;">`GET`</mark> `https://api.sonorancms.com/v2/community/accounts/00000000-0000-0000-0000-000000000000/identifiers`



> **Rate limit:** `22 requests per minute`  

> Authenticated v2 endpoints are rate limited per credential rather than per IP address.



Retrieve the identifiers stored for an account.



## Route Parameters



| Name | Type | Required | Description |

| --- | --- | --- | --- |

| `accountId` | string (uuid) | Yes | Target accountId. |



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

local response = sonoran.cms:getAccountIdentifiersV2(accountId)

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

  const response = await instance.cms.getAccountIdentifiersV2(accountId);

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

response = instance.cms.getAccountIdentifiersV2(accountId)

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

var response = await sonoran.Cms.getAccountIdentifiersV2(accountId);

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

  title: "Sonoran CMS v2 - Get Account Identifiers"

  version: "1.0.0"

  description: "Retrieve the identifiers stored for an account."

servers:

  -

    url: "https://api.sonorancms.com"

paths:

  /v2/community/accounts/{accountId}/identifiers:

    get:

      summary: "Get Account Identifiers"

      operationId: "getAccountIdentifiers"

      parameters:

        -

          description: "Target account UUID."

          name: "accountId"

          in: "path"

          schema:

            type: "string"

            format: "uuid"

          required: true

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

                    id: "55555555-5555-5555-5555-555555555555"

                    accId: "00000000-0000-0000-0000-000000000000"

                    type: "discord"

                    value: "1234567890"

                    refCount: 1

                    verified: true

                    metadata: {}

                    flagId: null

                    createdAt: "2026-04-15T00:00:00.000Z"

                    updatedAt: null

                meta:

                  timestamp: "2026-04-15T00:00:00.000Z"

                  path: "/v2/community/accounts/00000000-0000-0000-0000-000000000000/identifiers"

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

  --url "https://api.sonorancms.com/v2/community/accounts/00000000-0000-0000-0000-000000000000/identifiers" \

  --header "Authorization: Bearer YOUR_API_KEY" \

  --header "Accept: application/json"
```

{% endtab %}
{% endtabs %}

## Response



The `data` array contains the full security identifier entities for the account, including verification, metadata, and optional flag information.



```json

{

  "success": true,

  "data": [

    {

      "id": "55555555-5555-5555-5555-555555555555",

      "accId": "00000000-0000-0000-0000-000000000000",

      "type": "discord",

      "value": "1234567890",

      "refCount": 1,

      "verified": true,

      "metadata": {},

      "flagId": null,

      "createdAt": "2026-04-15T00:00:00.000Z",

      "updatedAt": null

    }

  ],

  "meta": {

    "timestamp": "2026-04-15T00:00:00.000Z",

    "path": "/v2/community/accounts/00000000-0000-0000-0000-000000000000/identifiers"

  }

}

```

