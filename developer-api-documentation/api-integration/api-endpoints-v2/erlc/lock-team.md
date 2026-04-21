---

description: Lock an ER:LC team.

---



# Lock Team



<mark style="color:green;">`POST`</mark> `https://api.sonorancms.com/v2/community/erlc/teams/lock`



> **Rate limit:** `18 requests per minute`  

> Authenticated v2 endpoints are rate limited per credential rather than per IP address.



Lock an ER:LC team.



## Request Body



| Name | Type | Required | Description |

| --- | --- | --- | --- |

| `robloxJoinCode` | string | Yes | See example request for the shape. |

| `team` | string | Yes | See example request for the shape. |

| `maxPlayers` | number | Yes | See example request for the shape. |



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
  ["robloxJoinCode"] = "ABC123",
  ["team"] = "Police",
  ["maxPlayers"] = 10
}

local response = sonoran.cms:lockTeamV2(payload)

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
  "robloxJoinCode": "ABC123",
  "team": "Police",
  "maxPlayers": 10
};

  const response = await instance.cms.lockTeamV2(payload);

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
  "robloxJoinCode": "ABC123",
  "team": "Police",
  "maxPlayers": 10
}

response = instance.cms.lockTeamV2(payload)

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
  robloxJoinCode = "ABC123",
  team = "Police",
  maxPlayers = 10
};

var response = await sonoran.Cms.lockTeamV2(payload);

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

  title: "Sonoran CMS v2 - Lock Team"

  version: "1.0.0"

  description: "Lock an ER:LC team."

servers:

  -

    url: "https://api.sonorancms.com"

paths:

  /v2/community/erlc/teams/lock:

    post:

      summary: "Lock Team"

      operationId: "lockTeam"

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

                data: "The police team has been locked down to a maximum of 12 players."

                meta:

                  timestamp: "2026-04-15T00:00:00.000Z"

                  path: "/v2/community/erlc/teams/lock"

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
curl --request POST \

  --url "https://api.sonorancms.com/v2/community/erlc/teams/lock" \

  --header "Authorization: Bearer YOUR_API_KEY" \

  --header "Accept: application/json" \

  --data '{"robloxJoinCode":"ABC123","team":"Police","maxPlayers":10}'
```

{% endtab %}
{% endtabs %}

## Response



The `data` value is a confirmation string. The exact wording changes for lock and unlock, but both endpoints return a string rather than a structured object.



```json

{

  "success": true,

  "data": "The police team has been locked down to a maximum of 12 players.",

  "meta": {

    "timestamp": "2026-04-15T00:00:00.000Z",

    "path": "/v2/community/erlc/teams/lock"

  }

}

```

