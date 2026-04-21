---

description: Create an ER:LC record.

---



# Add ERLC Record



<mark style="color:green;">`POST`</mark> `https://api.sonorancms.com/v2/community/erlc/records`



> **Rate limit:** `18 requests per minute`  

> Authenticated v2 endpoints are rate limited per credential rather than per IP address.



Create an ER:LC record.



## Request Body



| Name | Type | Required | Description |

| --- | --- | --- | --- |

| `robloxJoinCode` | string | Yes | See example request for the shape. |

| `executerDiscordId` | string | Yes | See example request for the shape. |

| `type` | string | Yes | See example request for the shape. |

| `reason` | string | Yes | See example request for the shape. |

| `points` | number | Yes | See example request for the shape. |



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
  ["executerDiscordId"] = "1234567890",
  ["type"] = "note",
  ["reason"] = "Example note",
  ["points"] = 0
}

local response = sonoran.cms:addErlcRecordV2(payload)

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
  "executerDiscordId": "1234567890",
  "type": "note",
  "reason": "Example note",
  "points": 0
};

  const response = await instance.cms.addErlcRecordV2(payload);

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
  "executerDiscordId": "1234567890",
  "type": "note",
  "reason": "Example note",
  "points": 0
}

response = instance.cms.addErlcRecordV2(payload)

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
  executerDiscordId = "1234567890",
  type = "note",
  reason = "Example note",
  points = 0
};

var response = await sonoran.Cms.addErlcRecordV2(payload);

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

  title: "Sonoran CMS v2 - Add Record"

  version: "1.0.0"

  description: "Create an ER:LC record."

servers:

  -

    url: "https://api.sonorancms.com"

paths:

  /v2/community/erlc/records:

    post:

      summary: "Add Record"

      operationId: "addErlcRecord"

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

        "201":

          description: "Successful response"

          content:

            application/json:

              schema:

                type: "object"

              example:

                success: true

                data:

                  success: true

                  message: "Records added successfully"

                meta:

                  timestamp: "2026-04-15T00:00:00.000Z"

                  path: "/v2/community/erlc/records"

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

  --url "https://api.sonorancms.com/v2/community/erlc/records" \

  --header "Authorization: Bearer YOUR_API_KEY" \

  --header "Accept: application/json" \

  --data '{"robloxJoinCode":"ABC123","executerDiscordId":"1234567890","type":"note","reason":"Example note","points":0}'
```

{% endtab %}
{% endtabs %}

## Response



The response shape varies by record `type`:



- `note`, `kick`, and custom log types return a confirmation object such as `{ success: true, message: "Records added successfully" }`.

- `ban` returns `{ success: true }` after the ban queue is updated.

- `disciplinary` returns the disciplinary service payload, which is usually `{ success: true, data: [DisciplinaryRecord] }`.



```json

{

  "success": true,

  "data": {

    "success": true,

    "message": "Records added successfully"

  },

  "meta": {

    "timestamp": "2026-04-15T00:00:00.000Z",

    "path": "/v2/community/erlc/records"

  }

}

```

