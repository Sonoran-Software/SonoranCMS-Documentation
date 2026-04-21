---

description: Update the ACE configuration for a server.

---



# Set ACE Config



<mark style="color:green;">`PATCH`</mark> `https://api.sonorancms.com/v2/community/servers/1/ace-config`



> **Rate limit:** `18 requests per minute`  

> Authenticated v2 endpoints are rate limited per credential rather than per IP address.



Update the ACE configuration for a server.



## Route Parameters



| Name | Type | Required | Description |

| --- | --- | --- | --- |

| `serverId` | number | Yes | Target serverId. |



## Request Body



| Name | Type | Required | Description |

| --- | --- | --- | --- |

| `mappings` | array | Yes | See example request for the shape. |



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

local serverId = 1
local payload = {
  ["mappings"] = {
    {
      ["discordRoleId"] = "1234567890",
      ["aceGroup"] = "admin"
    }
  }
}

local response = sonoran.cms:setAceConfigV2(serverId, payload)

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
  const serverId = 1;
  const payload = {
  "mappings": [
    {
      "discordRoleId": "1234567890",
      "aceGroup": "admin"
    }
  ]
};

  const response = await instance.cms.setAceConfigV2(serverId, payload);

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

serverId = 1
payload = {
  "mappings": [
    {
      "discordRoleId": "1234567890",
      "aceGroup": "admin"
    }
  ]
}

response = instance.cms.setAceConfigV2(serverId, payload)

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

var serverId = 1;
var payload = new {
  mappings = new[] {
    new {
      discordRoleId = "1234567890",
      aceGroup = "admin"
    }
  }
};

var response = await sonoran.Cms.setAceConfigV2(serverId, payload);

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

  title: "Sonoran CMS v2 - Set Ace Config"

  version: "1.0.0"

  description: "Update the ACE configuration for a server."

servers:

  -

    url: "https://api.sonorancms.com"

paths:

  /v2/community/servers/{serverId}/ace-config:

    patch:

      summary: "Set Ace Config"

      operationId: "setAceConfig"

      parameters:

        -

          description: "Target server id."

          name: "serverId"

          in: "path"

          schema:

            type: "integer"

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

                data:

                  mappings:

                    -

                      ranks:

                        - "22222222-2222-2222-2222-222222222222"

                      principal: "group:123456"

                meta:

                  timestamp: "2026-04-15T00:00:00.000Z"

                  path: "/v2/community/servers/1/ace-config"

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

  --url "https://api.sonorancms.com/v2/community/servers/1/ace-config" \

  --header "Authorization: Bearer YOUR_API_KEY" \

  --header "Accept: application/json" \

  --data '{"mappings":[{"discordRoleId":"1234567890","aceGroup":"admin"}]}'
```

{% endtab %}
{% endtabs %}

## Response



The `data` object is the updated ACE config wrapper with the saved `mappings` array.



```json

{

  "success": true,

  "data": {

    "mappings": [

      {

        "ranks": [

          "22222222-2222-2222-2222-222222222222"

        ],

        "principal": "group:123456"

      }

    ]

  },

  "meta": {

    "timestamp": "2026-04-15T00:00:00.000Z",

    "path": "/v2/community/servers/1/ace-config"

  }

}

```

