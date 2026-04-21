---

description: Update the ranks assigned to an account.

---



# Set Account Ranks



<mark style="color:green;">`PATCH`</mark> `https://api.sonorancms.com/v2/community/accounts/00000000-0000-0000-0000-000000000000/ranks`



> **Rate limit:** `22 requests per minute`  

> Authenticated v2 endpoints are rate limited per credential rather than per IP address.



Update the ranks assigned to an account.



## Route Parameters



| Name | Type | Required | Description |

| --- | --- | --- | --- |

| `accountId` | string (uuid) | Yes | Target accountId. |



## Request Body



| Name | Type | Required | Description |

| --- | --- | --- | --- |

| `accId` | string | Yes | See example request for the shape. |

| `add` | array | Yes | See example request for the shape. |

| `active` | boolean | Yes | See example request for the shape. |



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
  ["accId"] = "00000000-0000-0000-0000-000000000000",
  ["add"] = {
    "rank-1"
  },
  ["active"] = true
}

local response = sonoran.cms:setAccountRanksV2(accountId, payload)

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
  "accId": "00000000-0000-0000-0000-000000000000",
  "add": [
    "rank-1"
  ],
  "active": true
};

  const response = await instance.cms.setAccountRanksV2(accountId, payload);

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
  "accId": "00000000-0000-0000-0000-000000000000",
  "add": [
    "rank-1"
  ],
  "active": True
}

response = instance.cms.setAccountRanksV2(accountId, payload)

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
  accId = "00000000-0000-0000-0000-000000000000",
  add = new[] {
    "rank-1"
  },
  active = true
};

var response = await sonoran.Cms.setAccountRanksV2(accountId, payload);

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

  title: "Sonoran CMS v2 - Set Account Ranks"

  version: "1.0.0"

  description: "Update the ranks assigned to an account."

servers:

  -

    url: "https://api.sonorancms.com"

paths:

  /v2/community/accounts/{accountId}/ranks:

    patch:

      summary: "Set Account Ranks"

      operationId: "setAccountRanks"

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

                data:

                  accId: "00000000-0000-0000-0000-000000000000"

                  sysStatus: true

                  comStatus: true

                  accName: "ExampleAccount"

                  comName: "Example Community"

                  joinDate: "2026-04-15T00:00:00.000Z"

                  lastLogin: "2026-04-15T00:00:00.000Z"

                  owner: false

                  banned: false

                  banInfo: null

                  banExpiration: null

                  apiIdPreference: 0

                  apiIds:

                    ids: []

                  activeApiIds:

                    - "discord:1234567890"

                  identifiers:

                    idents:

                      -

                        id: "55555555-5555-5555-5555-555555555555"

                        accId: "00000000-0000-0000-0000-000000000000"

                        type: "discord"

                        value: "1234567890"

                        refCount: 1

                        verified: true

                        metadata: {}

                        flagId: null

                        createdAt: "2026-04-15T00:00:00.000Z"

                        updatedAt: null

                  ranks:

                    - "22222222-2222-2222-2222-222222222222"

                  clockData:

                    data:

                      -

                        id: "55555555-5555-5555-5555-555555555555"

                        startTime: "2026-04-15T00:00:00.000Z"

                        endTime: null

                        completed: false

                        notes: []

                        type: "patrol"

                  profileFields:

                    data:

                      -

                        id: "discord"

                        value: "1234567890"

                  bio: null

                  archived: false

                  discordId: "1234567890"

                  robloxId: "987654321"

                  uniqueId: 1001

                  customUniqueId: false

                  notificationPreferences:

                    forms:

                      statusChange:

                        inbox: true

                        desktop: true

                        mobile: true

                        email: true

                        discord: true

                  teamspeakId: null

                meta:

                  timestamp: "2026-04-15T00:00:00.000Z"

                  path: "/v2/community/accounts/00000000-0000-0000-0000-000000000000/ranks"

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

  --url "https://api.sonorancms.com/v2/community/accounts/00000000-0000-0000-0000-000000000000/ranks" \

  --header "Authorization: Bearer YOUR_API_KEY" \

  --header "Accept: application/json" \

  --data '{"accId":"00000000-0000-0000-0000-000000000000","add":["rank-1"],"active":true}'
```

{% endtab %}
{% endtabs %}

## Response



The `data` object is the updated account row returned by the rank update service. It reflects the new `ranks` and community status after the update.



```json

{

  "success": true,

  "data": {

    "accId": "00000000-0000-0000-0000-000000000000",

    "sysStatus": true,

    "comStatus": true,

    "accName": "ExampleAccount",

    "comName": "Example Community",

    "joinDate": "2026-04-15T00:00:00.000Z",

    "lastLogin": "2026-04-15T00:00:00.000Z",

    "owner": false,

    "banned": false,

    "banInfo": null,

    "banExpiration": null,

    "apiIdPreference": 0,

    "apiIds": {

      "ids": []

    },

    "activeApiIds": [

      "discord:1234567890"

    ],

    "identifiers": {

      "idents": [

        {

          "id": "55555555-5555-5555-5555-555555555555",

          "accId": "00000000-0000-0000-0000-000000000000",

          "type": "discord",

          "value": "1234567890",

          "refCount": 1,

          "verified": true,

          "metadata": {},

          "flagId": null,

          "createdAt": "2026-04-15T00:00:00.000Z",

          "updatedAt": null

        }

      ]

    },

    "ranks": [

      "22222222-2222-2222-2222-222222222222"

    ],

    "clockData": {

      "data": [

        {

          "id": "55555555-5555-5555-5555-555555555555",

          "startTime": "2026-04-15T00:00:00.000Z",

          "endTime": null,

          "completed": false,

          "notes": [],

          "type": "patrol"

        }

      ]

    },

    "profileFields": {

      "data": [

        {

          "id": "discord",

          "value": "1234567890"

        }

      ]

    },

    "bio": null,

    "archived": false,

    "discordId": "1234567890",

    "robloxId": "987654321",

    "uniqueId": 1001,

    "customUniqueId": false,

    "notificationPreferences": {

      "forms": {

        "statusChange": {

          "inbox": true,

          "desktop": true,

          "mobile": true,

          "email": true,

          "discord": true

        }

      }

    },

    "teamspeakId": null

  },

  "meta": {

    "timestamp": "2026-04-15T00:00:00.000Z",

    "path": "/v2/community/accounts/00000000-0000-0000-0000-000000000000/ranks"

  }

}

```

