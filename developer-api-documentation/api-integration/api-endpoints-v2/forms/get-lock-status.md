---

description: Retrieve the lock status for a form template.

---



# Get Form Lock Status



<mark style="color:green;">`GET`</mark> `https://api.sonorancms.com/v2/community/forms/1/lock`



> **Rate limit:** `27 requests per minute`  

> Authenticated v2 endpoints are rate limited per credential rather than per IP address.



Retrieve the lock status for a form template.



## Route Parameters



| Name | Type | Required | Description |

| --- | --- | --- | --- |

| `templateId` | number | Yes | Target templateId. |



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

local templateId = 1

local response = sonoran.cms:getFormLockV2(templateId)

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
  const templateId = 1;

  const response = await instance.cms.getFormLockV2(templateId);

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

templateId = 1

response = instance.cms.getFormLockV2(templateId)

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

var templateId = 1;

var response = await sonoran.Cms.getFormLockV2(templateId);

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

  title: "Sonoran CMS v2 - Get Lock Status"

  version: "1.0.0"

  description: "Retrieve the lock status for a form template."

servers:

  -

    url: "https://api.sonorancms.com"

paths:

  /v2/community/forms/{templateId}/lock:

    get:

      summary: "Get Lock Status"

      operationId: "getFormLockStatus"

      parameters:

        -

          description: "Target form template id."

          name: "templateId"

          in: "path"

          schema:

            type: "integer"

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

                data: true

                meta:

                  timestamp: "2026-04-15T00:00:00.000Z"

                  path: "/v2/community/forms/1/lock"

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

  --url "https://api.sonorancms.com/v2/community/forms/1/lock" \

  --header "Authorization: Bearer YOUR_API_KEY" \

  --header "Accept: application/json"
```

{% endtab %}
{% endtabs %}

## Response



The `data` value is a boolean. `true` means the form template is locked; `false` means it is open.



```json

{

  "success": true,

  "data": true,

  "meta": {

    "timestamp": "2026-04-15T00:00:00.000Z",

    "path": "/v2/community/forms/1/lock"

  }

}

```

