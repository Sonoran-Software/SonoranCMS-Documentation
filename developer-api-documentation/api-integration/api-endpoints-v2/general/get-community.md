---
description: Returns a lightweight summary for the authenticated community.
---

# Get Community

{% hint style="warning" %}
This endpoint requires `Authorization: Bearer <api key>`.
{% endhint %}

{% hint style="info" %}
Recommended safe rate limit: `13 requests/min` per credential.

The Kong gateway is configured slightly higher than this value to leave a small safety buffer for normal gameplay bursts.
{% endhint %}

## Get Community

<mark style="color:green;">`GET`</mark> `https://api.sonorancms.com/v2/community`
{% swagger method="get" path="/community" baseUrl="https://api.sonorancms.com" summary="Get Community" %}
{% swagger-description %}
Returns a lightweight summary for the authenticated community.
{% endswagger-description %}

{% swagger-response status="200: OK" description="" %}
<pre class="language-json"><code class="lang-json">{
    &quot;meta&quot;:  {
                 &quot;timestamp&quot;:  &quot;2026-04-14T00:00:00.000Z&quot;,
                 &quot;path&quot;:  &quot;/community&quot;
             },
    &quot;data&quot;:  {

             },
    &quot;success&quot;:  true
}</code></pre>
{% endswagger-response %}

{% swagger-response status="400: Bad Request" description="The following 400 errors may be sent in response:" %}
<pre class="language-json"><code class="lang-json">{
    &quot;detail&quot;:  &quot;VALID BAD REQUEST REASON&quot;,
    &quot;instance&quot;:  &quot;/community&quot;,
    &quot;traceId&quot;:  &quot;00000000-0000-0000-0000-000000000000&quot;,
    &quot;type&quot;:  &quot;https://httpstatuses.com/400&quot;,
    &quot;title&quot;:  &quot;Bad Request&quot;,
    &quot;status&quot;:  400
}</code></pre>
{% endswagger-response %}
{% endswagger %}


Returns a lightweight summary for the authenticated community.

#### Response

- Returns community metadata such as id, uuid, name, tier, and server count.

```json
{
    "meta":  {
                 "timestamp":  "2026-04-14T00:00:00.000Z",
                 "path":  "/v2/community"
             },
    "data":  {
                 "id":  "community-id",
                 "uuid":  "00000000-0000-0000-0000-000000000000",
                 "servers":  5,
                 "tier":  "PLUS",
                 "name":  "Community Name",
                 "subVersion":  3
             },
    "success":  true
}
```


