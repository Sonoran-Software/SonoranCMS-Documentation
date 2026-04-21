---

description: Create a short URL for the community.

---



# Create Short URL



<mark style="color:green;">`POST`</mark> `https://api.sonorancms.com/v2/community/short-urls`



> **Rate limit:** `13 requests per minute`  

> Authenticated v2 endpoints are rate limited per credential rather than per IP address.



Create a short URL for the community.



## Request Body



| Name | Type | Required | Description |

| --- | --- | --- | --- |

| `path` | string | Yes | See example request for the shape. |

| `isCustomDomain` | boolean | Yes | See example request for the shape. |



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
  ["path"] = "/go/example",
  ["isCustomDomain"] = false
}

local response = sonoran.cms:createShortUrlV2(payload)

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
  "path": "/go/example",
  "isCustomDomain": false
};

  const response = await instance.cms.createShortUrlV2(payload);

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
  "path": "/go/example",
  "isCustomDomain": False
}

response = instance.cms.createShortUrlV2(payload)

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
  path = "/go/example",
  isCustomDomain = false
};

var response = await sonoran.Cms.createShortUrlV2(payload);

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

  title: "Sonoran CMS v2 - Create Short Url"

  version: "1.0.0"

  description: "Create a short URL for the community."

servers:

  -

    url: "https://api.sonorancms.com"

paths:

  /v2/community/short-urls:

    post:

      summary: "Create Short Url"

      operationId: "createShortUrl"

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

                  redirect: "https://sonorancms.com/dashboard"

                meta:

                  timestamp: "2026-04-15T00:00:00.000Z"

                  path: "/v2/community/short-urls"

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

  --url "https://api.sonorancms.com/v2/community/short-urls" \

  --header "Authorization: Bearer YOUR_API_KEY" \

  --header "Accept: application/json" \

  --data '{"path":"/go/example","isCustomDomain":false}'
```

{% endtab %}
{% endtabs %}

## Response



The `data` object is the nested short-url lookup result. On success it contains `success: true` and the resolved `redirect` URL.



```json

{

  "success": true,

  "data": {

    "success": true,

    "redirect": "https://sonorancms.com/dashboard"

  },

  "meta": {

    "timestamp": "2026-04-15T00:00:00.000Z",

    "path": "/v2/community/short-urls"

  }

}

```

