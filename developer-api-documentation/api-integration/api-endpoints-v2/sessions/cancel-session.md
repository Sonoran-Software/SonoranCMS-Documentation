---

description: Cancel an active session.

---



# Cancel Session



<mark style="color:green;">`DELETE`</mark> `https://api.sonorancms.com/v2/community/sessions`



> **Rate limit:** `9 requests per minute`  

> Authenticated v2 endpoints are rate limited per credential rather than per IP address.



Cancel an active session.



## Request Body



| Name | Type | Required | Description |

| --- | --- | --- | --- |

| `serverId` | number | Yes | See example request for the shape. |

| `accId` | string | Yes | See example request for the shape. |



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

local payload = {
  ["serverId"] = 1,
  ["accId"] = "00000000-0000-0000-0000-000000000000"
}

local response = sonoran.cms:cancelSessionV2(payload)

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
  const payload = {
  "serverId": 1,
  "accId": "00000000-0000-0000-0000-000000000000"
};

  const response = await instance.cms.cancelSessionV2(payload);

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

payload = {
  "serverId": 1,
  "accId": "00000000-0000-0000-0000-000000000000"
}

response = instance.cms.cancelSessionV2(payload)

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

var payload = new {
  serverId = 1,
  accId = "00000000-0000-0000-0000-000000000000"
};

var response = await sonoran.Cms.cancelSessionV2(payload);

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

  title: "Sonoran CMS v2 - Cancel Session"

  version: "1.0.0"

  description: "Cancel an active session."

servers:

  -

    url: "https://api.sonorancms.com"

paths:

  /v2/community/sessions:

    delete:

      summary: "Cancel Session"

      operationId: "cancelSession"

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

        "204":

          description: "No Content"

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
curl --request DELETE \

  --url "https://api.sonorancms.com/v2/community/sessions" \

  --header "Authorization: Bearer YOUR_API_KEY" \

  --header "Accept: application/json" \

  --data '{"serverId":1,"accId":"00000000-0000-0000-0000-000000000000"}'
```

{% endtab %}
{% endtabs %}

## Response



The cancel endpoint intentionally returns no JSON body when it succeeds.



This endpoint returns `204 No Content` on success, so there is no response body.

