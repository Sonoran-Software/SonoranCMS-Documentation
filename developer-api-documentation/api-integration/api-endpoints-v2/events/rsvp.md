---

description: Create an RSVP for an event.

---



# RSVP



<mark style="color:green;">`POST`</mark> `https://api.sonorancms.com/v2/community/events/11111111-1111-1111-1111-111111111111/rsvps`



> **Rate limit:** `27 requests per minute`  

> Authenticated v2 endpoints are rate limited per credential rather than per IP address.



Create an RSVP for an event.



## Route Parameters



| Name | Type | Required | Description |

| --- | --- | --- | --- |

| `eventId` | string (uuid) | Yes | Target eventId. |



## Request Body



| Name | Type | Required | Description |

| --- | --- | --- | --- |

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

local eventId = "00000000-0000-0000-0000-000000000000"
local payload = {
  ["accId"] = "00000000-0000-0000-0000-000000000000"
}

local response = sonoran.cms:rsvpEventV2(eventId, payload)

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
  const eventId = "00000000-0000-0000-0000-000000000000";
  const payload = {
  "accId": "00000000-0000-0000-0000-000000000000"
};

  const response = await instance.cms.rsvpEventV2(eventId, payload);

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

eventId = "00000000-0000-0000-0000-000000000000"
payload = {
  "accId": "00000000-0000-0000-0000-000000000000"
}

response = instance.cms.rsvpEventV2(eventId, payload)

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

var eventId = "00000000-0000-0000-0000-000000000000";
var payload = new {
  accId = "00000000-0000-0000-0000-000000000000"
};

var response = await sonoran.Cms.rsvpEventV2(eventId, payload);

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

  title: "Sonoran CMS v2 - Rsvp"

  version: "1.0.0"

  description: "Create an RSVP for an event."

servers:

  -

    url: "https://api.sonorancms.com"

paths:

  /v2/community/events/{eventId}/rsvps:

    post:

      summary: "Rsvp"

      operationId: "createRsvp"

      parameters:

        -

          description: "Target event id."

          name: "eventId"

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

                data: "RSVP_SUCCESS"

                meta:

                  timestamp: "2026-04-15T00:00:00.000Z"

                  path: "/v2/community/events/11111111-1111-1111-1111-111111111111/rsvps"

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

  --url "https://api.sonorancms.com/v2/community/events/11111111-1111-1111-1111-111111111111/rsvps" \

  --header "Authorization: Bearer YOUR_API_KEY" \

  --header "Accept: application/json" \

  --data '{"accId":"00000000-0000-0000-0000-000000000000"}'
```

{% endtab %}
{% endtabs %}

## Response



The `data` value is a toggle code. The service returns `RSVP_SUCCESS` when the account is added and `UNRSVP_SUCCESS` when the existing RSVP is removed.



```json

{

  "success": true,

  "data": "RSVP_SUCCESS",

  "meta": {

    "timestamp": "2026-04-15T00:00:00.000Z",

    "path": "/v2/community/events/11111111-1111-1111-1111-111111111111/rsvps"

  }

}

```

