---
description: Triggers one or more promotion flows.
---

# Trigger Promotion Flows

{% hint style="warning" %}
This endpoint requires `Authorization: Bearer <api key>`.
{% endhint %}

{% hint style="info" %}
Recommended safe rate limit: `13 requests/min` per credential.

The Kong gateway is configured slightly higher than these values to leave a small safety buffer for normal gameplay bursts.
{% endhint %}

## Trigger Promotion Flows

<mark style="color:green;">`POST`</mark> `https://api.sonorancms.com/v2/community/promotion-flows/trigger`
{% swagger method="post" path="/v2/community/promotion-flows/trigger" baseUrl="https://api.sonorancms.com" summary="Trigger Promotion Flows" %}
{% swagger-description %}
Triggers one or more promotion flows.
{% endswagger-description %}

{% swagger-response status="200: OK" description="" %}
<pre class="language-json"><code class="lang-json">{
    &quot;meta&quot;:  {
                 &quot;timestamp&quot;:  &quot;2026-04-14T00:00:00.000Z&quot;,
                 &quot;path&quot;:  &quot;/v2/community/promotion-flows/trigger&quot;
             },
    &quot;data&quot;:  {

             },
    &quot;success&quot;:  true
}</code></pre>
{% endswagger-response %}

{% swagger-response status="400: Bad Request" description="The following 400 errors may be sent in response:" %}
<pre class="language-json"><code class="lang-json">{
    &quot;detail&quot;:  &quot;VALID BAD REQUEST REASON&quot;,
    &quot;instance&quot;:  &quot;/v2/community/promotion-flows/trigger&quot;,
    &quot;traceId&quot;:  &quot;00000000-0000-0000-0000-000000000000&quot;,
    &quot;type&quot;:  &quot;https://httpstatuses.com/400&quot;,
    &quot;title&quot;:  &quot;Bad Request&quot;,
    &quot;status&quot;:  400
}</code></pre>
{% endswagger-response %}
{% endswagger %}


Triggers one or more promotion flows.

#### Request

- Body: `data` array of promotion flow trigger items.

```json
{
    "data":  [
                 {
                     "userId":  "00000000-0000-0000-0000-000000000000",
                     "promote":  true,
                     "users":  [
                                   "acc-id-1"
                               ],
                     "flowId":  "promotion-flow-id"
                 }
             ]
}
```

#### Response

- Returns the promotion service result inside the v2 envelope.

```json
{
    "meta":  {
                 "timestamp":  "2026-04-14T00:00:00.000Z",
                 "path":  "/v2/community/promotion-flows/trigger"
             },
    "data":  [

             ],
    "success":  true
}
```


