---

description: Retrieve the current session for a server.

---



# Get Current Session



<mark style="color:green;">`GET`</mark> `https://api.sonorancms.com/v2/community/sessions/current`



> **Rate limit:** `27 requests per minute`  

> Authenticated v2 endpoints are rate limited per credential rather than per IP address.



Retrieve the current session for a server.



## Query Parameters



| Name | Type | Required | Description |

| --- | --- | --- | --- |

| `serverId` | number | Yes | See example request for the shape. |



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

local response = sonoran.cms:getCurrentSessionV2(serverId)

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

  const response = await instance.cms.getCurrentSessionV2(serverId);

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

response = instance.cms.getCurrentSessionV2(serverId)

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

var response = await sonoran.Cms.getCurrentSessionV2(serverId);

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

  title: "Sonoran CMS v2 - Get Current Session"

  version: "1.0.0"

  description: "Retrieve the current session for a server."

servers:

  -

    url: "https://api.sonorancms.com"

paths:

  /v2/community/sessions/current:

    get:

      summary: "Get Current Session"

      operationId: "getCurrentSession"

      parameters:

        -

          description: "Query parameter serverId."

          name: "serverId"

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

                data:

                  id: "55555555-5555-5555-5555-555555555555"

                  sysStatus: true

                  community: "00000000-0000-0000-0000-000000000000"

                  serverId: 1

                  startedBy: "00000000-0000-0000-0000-000000000000"

                  startedAt: "2026-04-15T00:00:00.000Z"

                  endedBy: null

                  endedAt: null

                  cancelledBy: null

                  stats: {}

                  metadata: {}

                meta:

                  timestamp: "2026-04-15T00:00:00.000Z"

                  path: "/v2/community/sessions/current"

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

  --url "https://api.sonorancms.com/v2/community/sessions/current?serverId=1" \

  --header "Authorization: Bearer YOUR_API_KEY" \

  --header "Accept: application/json"
```

{% endtab %}
{% endtabs %}

## Response



The `data` object is the session row. `GET`, `POST`, and `PATCH` all return the `CommunityServerSession` entity shape on success.



```json

{

  "success": true,

  "data": {

    "id": "55555555-5555-5555-5555-555555555555",

    "sysStatus": true,

    "community": "00000000-0000-0000-0000-000000000000",

    "serverId": 1,

    "startedBy": "00000000-0000-0000-0000-000000000000",

    "startedAt": "2026-04-15T00:00:00.000Z",

    "endedBy": null,

    "endedAt": null,

    "cancelledBy": null,

    "stats": {},

    "metadata": {}

  },

  "meta": {

    "timestamp": "2026-04-15T00:00:00.000Z",

    "path": "/v2/community/sessions/current"

  }

}

```

