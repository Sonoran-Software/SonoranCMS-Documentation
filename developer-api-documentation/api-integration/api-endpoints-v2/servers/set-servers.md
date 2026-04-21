---

description: Replace the configured server list.

---



# Set Servers



<mark style="color:green;">`PUT`</mark> `https://api.sonorancms.com/v2/community/servers`



> **Rate limit:** `9 requests per minute`  

> Authenticated v2 endpoints are rate limited per credential rather than per IP address.



Replace the configured server list.



## Request Body



| Name | Type | Required | Description |

| --- | --- | --- | --- |

| `servers` | array | Yes | See example request for the shape. |



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
  ["servers"] = {
    {
      ["id"] = 1,
      ["name"] = "Main Server",
      ["description"] = "Primary community server",
      ["ip"] = "127.0.0.1",
      ["port"] = "30120",
      ["type"] = "FiveM",
      ["erlcApiKey"] = "",
      ["robloxJoinCode"] = "ABC123",
      ["aceConfig"] = { },
      ["robloxMetadata"] = { }
    }
  }
}

local response = sonoran.cms:setServersV2(payload)

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
  "servers": [
    {
      "id": 1,
      "name": "Main Server",
      "description": "Primary community server",
      "ip": "127.0.0.1",
      "port": "30120",
      "type": "FiveM",
      "erlcApiKey": "",
      "robloxJoinCode": "ABC123",
      "aceConfig": {},
      "robloxMetadata": {}
    }
  ]
};

  const response = await instance.cms.setServersV2(payload);

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
  "servers": [
    {
      "id": 1,
      "name": "Main Server",
      "description": "Primary community server",
      "ip": "127.0.0.1",
      "port": "30120",
      "type": "FiveM",
      "erlcApiKey": "",
      "robloxJoinCode": "ABC123",
      "aceConfig": {},
      "robloxMetadata": {}
    }
  ]
}

response = instance.cms.setServersV2(payload)

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
  servers = new[] {
    new {
      id = 1,
      name = "Main Server",
      description = "Primary community server",
      ip = "127.0.0.1",
      port = "30120",
      type = "FiveM",
      erlcApiKey = "",
      robloxJoinCode = "ABC123",
      aceConfig = new { },
      robloxMetadata = new { }
    }
  }
};

var response = await sonoran.Cms.setServersV2(payload);

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

  title: "Sonoran CMS v2 - Set Servers"

  version: "1.0.0"

  description: "Replace the configured server list."

servers:

  -

    url: "https://api.sonorancms.com"

paths:

  /v2/community/servers:

    put:

      summary: "Set Servers"

      operationId: "setServers"

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

                  servers:

                    -

                      id: 1

                      name: "Main Server"

                      description: "Primary gameplay server"

                      ip: "127.0.0.1"

                      port: "30120"

                      typeLastUpdated: "2026-04-15T00:00:00.000Z"

                      type: "erlc"

                      robloxJoinCode: "ABCD-1234"

                      aceConfig:

                        mappings:

                          -

                            ranks:

                              - "22222222-2222-2222-2222-222222222222"

                            principal: "group:123456"

                meta:

                  timestamp: "2026-04-15T00:00:00.000Z"

                  path: "/v2/community/servers"

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
curl --request PUT \

  --url "https://api.sonorancms.com/v2/community/servers" \

  --header "Authorization: Bearer YOUR_API_KEY" \

  --header "Accept: application/json" \

  --data '{"servers":[{"id":1,"name":"Main Server","description":"Primary community server","ip":"127.0.0.1","port":"30120","type":"FiveM","erlcApiKey":"","robloxJoinCode":"ABC123","aceConfig":{},"robloxMetadata":{}}]}'
```

{% endtab %}
{% endtabs %}

## Response



The `data` object is the community `servers` container. It exposes the server list the backend stores for the community.



```json

{

  "success": true,

  "data": {

    "servers": [

      {

        "id": 1,

        "name": "Main Server",

        "description": "Primary gameplay server",

        "ip": "127.0.0.1",

        "port": "30120",

        "typeLastUpdated": "2026-04-15T00:00:00.000Z",

        "type": "erlc",

        "robloxJoinCode": "ABCD-1234",

        "aceConfig": {

          "mappings": [

            {

              "ranks": [

                "22222222-2222-2222-2222-222222222222"

              ],

              "principal": "group:123456"

            }

          ]

        }

      }

    ]

  },

  "meta": {

    "timestamp": "2026-04-15T00:00:00.000Z",

    "path": "/v2/community/servers"

  }

}

```

