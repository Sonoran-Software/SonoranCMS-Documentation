---
description: Lists community accounts with optional filters.
---

# Get Accounts

{% hint style="warning" %}
This endpoint requires `Authorization: Bearer <api key>`.
{% endhint %}

{% hint style="info" %}
Recommended safe rate limit: `22 requests/min` per credential.

The Kong gateway is configured slightly higher than these values to leave a small safety buffer for normal gameplay bursts.
{% endhint %}

## Get Accounts

<mark style="color:green;">`GET`</mark> `https://api.sonorancms.com/v2/community/accounts`
{% swagger method="get" path="/v2/community/accounts" baseUrl="https://api.sonorancms.com" summary="Get Accounts" %}
{% swagger-description %}
Lists community accounts with optional filters.
{% endswagger-description %}

{% swagger-response status="200: OK" description="" %}
<pre class="language-json"><code class="lang-json">{
    &quot;meta&quot;:  {
                 &quot;timestamp&quot;:  &quot;2026-04-14T00:00:00.000Z&quot;,
                 &quot;path&quot;:  &quot;/v2/community/accounts&quot;
             },
    &quot;data&quot;:  {

             },
    &quot;success&quot;:  true
}</code></pre>
{% endswagger-response %}

{% swagger-response status="400: Bad Request" description="The following 400 errors may be sent in response:" %}
<pre class="language-json"><code class="lang-json">{
    &quot;detail&quot;:  &quot;VALID BAD REQUEST REASON&quot;,
    &quot;instance&quot;:  &quot;/v2/community/accounts&quot;,
    &quot;traceId&quot;:  &quot;00000000-0000-0000-0000-000000000000&quot;,
    &quot;type&quot;:  &quot;https://httpstatuses.com/400&quot;,
    &quot;title&quot;:  &quot;Bad Request&quot;,
    &quot;status&quot;:  400
}</code></pre>
{% endswagger-response %}
{% endswagger %}


Lists community accounts with optional filters.

#### Request

- Query parameters: `skip`, `take`, `sysStatus`, `comStatus`, `banned`, `archived`.

#### Response

- Returns `{ items, total, skip, take }` inside the v2 envelope.

```json
{
    "meta":  {
                 "timestamp":  "2026-04-14T00:00:00.000Z",
                 "path":  "/v2/community/accounts"
             },
    "data":  {
                 "total":  1,
                 "take":  25,
                 "skip":  0,
                 "items":  [
                               {
                                   "accId":  "00000000-0000-0000-0000-000000000000",
                                   "accName":  "Test Account"
                               }
                           ]
             },
    "success":  true
}
```


