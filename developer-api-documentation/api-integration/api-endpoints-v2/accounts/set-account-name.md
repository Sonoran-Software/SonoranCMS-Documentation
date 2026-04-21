---

description: Update the display name for an account.

---



# Set Account Name



<mark style="color:green;">`PATCH`</mark> `https://api.sonorancms.com/v2/community/accounts/00000000-0000-0000-0000-000000000000/name`



> **Rate limit:** `22 requests per minute`  

> Authenticated v2 endpoints are rate limited per credential rather than per IP address.



Update the display name for an account.



## Route Parameters



| Name | Type | Required | Description |

| --- | --- | --- | --- |

| `accountId` | string (uuid) | Yes | Target accountId. |



## Request Body



| Name | Type | Required | Description |

| --- | --- | --- | --- |

| `newName` | string | Yes | See example request for the shape. |



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
local payload = {
  ["newName"] = "Example Account"
}

local response = sonoran.cms:setAccountNameV2(accountId, payload)

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
  const payload = {
  "newName": "Example Account"
};

  const response = await instance.cms.setAccountNameV2(accountId, payload);

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
payload = {
  "newName": "Example Account"
}

response = instance.cms.setAccountNameV2(accountId, payload)

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
var payload = new {
  newName = "Example Account"
};

var response = await sonoran.Cms.setAccountNameV2(accountId, payload);

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

  title: "Sonoran CMS v2 - Set Account Name"

  version: "1.0.0"

  description: "Update the display name for an account."

servers:

  -

    url: "https://api.sonorancms.com"

paths:

  /v2/community/accounts/{accountId}/name:

    patch:

      summary: "Set Account Name"

      operationId: "setAccountName"

      parameters:

        -

          description: "Target account UUID."

          name: "accountId"

          in: "path"

          schema:

            type: "string"

            format: "uuid"

          required: true

      requestBody:

        required: true

        content:

          application/json:

            schema:

              type: "object"

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

                data: "New Community Name (00000000-0000-0000-0000-000000000000): Example Account"

                meta:

                  timestamp: "2026-04-15T00:00:00.000Z"

                  path: "/v2/community/accounts/00000000-0000-0000-0000-000000000000/name"

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
curl --request PATCH \

  --url "https://api.sonorancms.com/v2/community/accounts/00000000-0000-0000-0000-000000000000/name" \

  --header "Authorization: Bearer YOUR_API_KEY" \

  --header "Accept: application/json" \

  --data '{"newName":"Example Account"}'
```

{% endtab %}
{% endtabs %}

## Response



The `data` value is a confirmation string, not an account object. The account update still happens in the background through the service layer.



```json

{

  "success": true,

  "data": "New Community Name (00000000-0000-0000-0000-000000000000): Example Account",

  "meta": {

    "timestamp": "2026-04-15T00:00:00.000Z",

    "path": "/v2/community/accounts/00000000-0000-0000-0000-000000000000/name"

  }

}

```

