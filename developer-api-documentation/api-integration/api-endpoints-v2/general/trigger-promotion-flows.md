---
description: Trigger one or more promotion flow actions.
---

# Trigger Promotion Flows

<mark style="color:green;">`POST`</mark> `https://api.sonorancms.com/v2/community/promotion-flows/trigger`

> **Rate limit:** `13 requests per minute`  
> Authenticated v2 endpoints are rate limited per credential rather than per IP address.

Trigger one or more promotion flow actions.

## Request Body

| Name | Type | Required | Description |
| --- | --- | --- | --- |
| `data` | array | Yes | See example request for the shape. |

## Example Request

{% tabs %}
{% tab title="Sonoran.lua" %}

```lua
local response = sonoran:request({
  "method": "POST",
  "path": "/v2/community/promotion-flows/trigger",
  "body": {
    "data": [
      {
        "flowId": "flow-1",
        "users": [
          "ExampleUser"
        ],
        "promote": true
      }
    ]
  }
})
```

{% endtab %}
{% tab title="Sonoran.js" %}

```javascript
const response = await sonoran.request({
  "method": "POST",
  "path": "/v2/community/promotion-flows/trigger",
  "body": {
    "data": [
      {
        "flowId": "flow-1",
        "users": [
          "ExampleUser"
        ],
        "promote": true
      }
    ]
  }
});
```

{% endtab %}
{% tab title="Sonoran.py" %}

```python
response = sonoran.request({
  "method": "POST",
  "path": "/v2/community/promotion-flows/trigger",
  "body": {
    "data": [
      {
        "flowId": "flow-1",
        "users": [
          "ExampleUser"
        ],
        "promote": true
      }
    ]
  }
})
```

{% endtab %}
{% tab title="Sonoran.Net" %}

```csharp
var response = await sonoran.RequestAsync(new SonoranRequest
{
    {
      "method": "POST",
      "path": "/v2/community/promotion-flows/trigger",
      "body": {
        "data": [
          {
            "flowId": "flow-1",
            "users": [
              "ExampleUser"
            ],
            "promote": true
          }
        ]
      }
    }
});
```

{% endtab %}
{% tab title="OpenAPI" %}

```yaml
post:
  summary: Trigger Promotion Flows
  security:
    - v2ApiKey: []
  requestBody:
    required: true
    content:
      application/json:
        schema:
          type: object
  responses:
    '200':
      description: Successful response
```

{% endtab %}
{% tab title="cURL" %}

```bash
curl --request POST \
  --url "https://api.sonorancms.com/v2/community/promotion-flows/trigger" \
  --header "Authorization: Bearer YOUR_API_KEY" \
  --header "Accept: application/json" \
  --data '{"data":[{"flowId":"flow-1","users":["ExampleUser"],"promote":true}]}'
```

{% endtab %}
{% endtabs %}

## Response

Successful requests return `application/json` and use the standard v2 envelope.

```json
{
  "success": true,
  "data": {
    "triggered": 1,
    "results": [
      {
        "flowId": "flow-1",
        "status": "queued"
      }
    ]
  },
  "meta": {
    "timestamp": "2026-04-14T00:00:00.000Z",
    "path": "/v2/community/promotion-flows/trigger"
  }
}
```
