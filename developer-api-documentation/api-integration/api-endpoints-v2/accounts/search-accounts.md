---
description: Searches accounts by identity fields.
---

# Search Accounts

{% hint style="warning" %}
This endpoint requires `Authorization: Bearer <api key>`.
{% endhint %}

{% hint style="info" %}
Recommended safe rate limit: `27 requests/min` per credential.

The Kong gateway is configured slightly higher than these values to leave a small safety buffer for normal gameplay bursts.
{% endhint %}

## Search Accounts

<mark style="color:green;">`GET`</mark> `https://api.sonorancms.com/v2/community/accounts/search`
{% swagger method="get" path="/v2/community/accounts/search" baseUrl="https://api.sonorancms.com" summary="Search Accounts" %}
{% swagger-description %}
Searches accounts by identity fields.
{% endswagger-description %}

{% swagger-response status="200: OK" description="" %}
<pre class="language-json"><code class="lang-json">{
    &quot;meta&quot;:  {
                 &quot;timestamp&quot;:  &quot;2026-04-14T00:00:00.000Z&quot;,
                 &quot;path&quot;:  &quot;/v2/community/accounts/search&quot;
             },
    &quot;data&quot;:  {

             },
    &quot;success&quot;:  true
}</code></pre>
{% endswagger-response %}

{% swagger-response status="400: Bad Request" description="The following 400 errors may be sent in response:" %}
<pre class="language-json"><code class="lang-json">{
    &quot;detail&quot;:  &quot;VALID BAD REQUEST REASON&quot;,
    &quot;instance&quot;:  &quot;/v2/community/accounts/search&quot;,
    &quot;traceId&quot;:  &quot;00000000-0000-0000-0000-000000000000&quot;,
    &quot;type&quot;:  &quot;https://httpstatuses.com/400&quot;,
    &quot;title&quot;:  &quot;Bad Request&quot;,
    &quot;status&quot;:  400
}</code></pre>
{% endswagger-response %}
{% endswagger %}


Searches accounts by identity fields.

#### Request

- Query parameters can include `accountId`, `apiId`, `accId`, `username`, `discord`, `discordId`, and `uniqueId`.

#### Response

- Returns matching accounts inside an `items` array.

```json
{
    "meta":  {
                 "timestamp":  "2026-04-14T00:00:00.000Z",
                 "path":  "/v2/community/accounts/search?username=Test"
             },
    "data":  {
                 "items":  [
                               {
                                   "accId":  "00000000-0000-0000-0000-000000000000",
                                   "accName":  "Test Account"
                               }
                           ],
                 "total":  1
             },
    "success":  true
}
```


