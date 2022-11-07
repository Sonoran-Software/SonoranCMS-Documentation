---
description: >-
  View all of our API endpoints, learn about our data structuring, and integrate
  your framework with Sonoran CMS.
---

# API Endpoints

{% hint style="info" %}
API endpoints are not enabled with the free version of Sonoran CMS.\
For more information, see our [pricing](../../../pricing/pricing-faq/) or view how to check your community [limits](../../../tutorials/getting-started/view-your-limits.md).
{% endhint %}

{% hint style="success" %}
Looking for VPS, web, or dedicated hosting? Check out our official [server hosting](https://info.sonorancad.com/other-products/server-hosting)!
{% endhint %}

## Sonoran JS - NPM Library

Sonoran CMS offers a complete Node API library from NPM!

`npm i @sonoransoftware/sonoran.js`

[Learn more about our NPM library](https://www.npmjs.com/package/@sonoransoftware/sonoran.js)!

## Available API Endpoints

### General Endpoints

View all general endpoints for user account actions, administrative actions, and more!

{% content-ref url="general/" %}
[general](general/)
{% endcontent-ref %}

### Server Endpoints

View all server endpoints for game server whitelist, server management, etc.

{% content-ref url="servers/" %}
[servers](servers/)
{% endcontent-ref %}



## API Code Examples

### Javascript

This example makes a [get community account request](general/get-com-account.md) based on a given API ID (Discord ID here). This uses the [Axios library](https://www.npmjs.com/package/axios) to help make the HTTP POST request.

The server response is then logged to console.

```javascript
// Import Axios library
// https://www.npmjs.com/package/axios
// Install command: `npm i axios` 
import axios from 'axios';
// Set the API URL (CMS backend)
let baseURL = 'https://api.sonorancms.com';
// Set the `api` object to be used
let api = axios.create({ baseURL });

// Format the POST body data
// https://info.sonorancms.com/developer-api-documentation/api-integration/api-endpoints/general/get-com-account
const data = {
  id: 'YOUR_COMMUNITY_ID',
  key: 'YOUR_API_KEY',
  type: 'GET_COM_ACCOUNT',
  data: [
    {
      apiId: "235947056630333440" // Discord ID
    }
  ],
};

// Send the POST request
//  Format the data to JSON
api.post('/general/get_com_account', JSON.stringify(data))
  .then((response) => {
    // Response back from the backend
    console.log(response);
  })
  .catch((err) => {
    // Error response back from the backend
    console.log(err);
 });
```

### Lua

This example makes a [get community account request](general/get-com-account.md) based on a given API ID (Discord ID here). This uses the[ FiveM performHttpRequest native](https://docs.fivem.net/docs/scripting-reference/runtimes/lua/functions/PerformHttpRequest/) to help make the HTTP POST request.

The server response is then logged to console.

```lua
-- Body payload object
local payload = {}

-- Specify our community ID, API key, and API method type (Panic)
payload["id"] = "YOUR_COMMUNITY_ID"
payload["key"] = "YOUR_API_KEY"
payload["type"] = "GET_COM_ACCOUNT"

-- Data: List (array) of unit panic objects
--    Here, we're specifying one unit to PANIC
local postData = {
    {
        ["apiId"] = "235947056630333440",  -- Discord ID
    },
}
-- Add this data to our payload
payload["data"] = postData

-- Send POST request with JSON encoded body (payload)
PerformHttpRequest("https://api.sonorancms.com/general/get_com_account", function(statusCode, res, headers)
    if statusCode == 200 and res ~= nil then
        -- Status code 200 (Success)
        print("result: "..tostring(res))
    else
        -- Error code
        print(("CMS API ERROR: %s %s"):format(statusCode, res))
    end
end, "POST", json.encode(payload), {["Content-Type"]="application/json"})
```

## Endpoints Subscription Requirements

Each endpoint requires a certain subscription, some may be available for communities on the Free plan or some may require the Pro plan, the table below shows what subscription is required per endpoint.

<table><thead><tr><th>Endpoint</th><th data-type="select">Minimum Subscription Level</th></tr></thead><tbody><tr><td>/general/get_sub_version</td><td></td></tr><tr><td>/general/check_com_apiid</td><td></td></tr><tr><td>/general/get_com<em>_</em>account</td><td></td></tr><tr><td>/general/get_account<em>_</em>ranks</td><td></td></tr><tr><td>/general/clock_in<em>_</em>out</td><td></td></tr><tr><td>/servers/get_game_servers</td><td></td></tr><tr><td>/servers/verify_whitelist</td><td></td></tr><tr><td>/servers/full_whitelist</td><td></td></tr></tbody></table>
