---
description: Looks up the authenticated community or another community by id or uuid.
---

# Lookup Community

{% hint style="warning" %}
This endpoint requires `Authorization: Bearer <api key>`.
{% endhint %}

{% hint style="info" %}
Recommended safe rate limit: `13 requests/min` per credential.

The Kong gateway is configured slightly higher than these values to leave a small safety buffer for normal gameplay bursts.
{% endhint %}

## Lookup Community

<mark style="color:green;">`GET`</mark> `https://api.sonorancms.com/v2/community/lookup`
{% swagger method="get" path="/v2/community/lookup" baseUrl="https://api.sonorancms.com" summary="Lookup Community" %}
{% swagger-description %}
Looks up the authenticated community or another community by id or uuid.
{% endswagger-description %}

{% swagger-response status="200: OK" description="" %}
<pre class="language-json"><code class="lang-json">{
    &quot;meta&quot;:  {
                 &quot;timestamp&quot;:  &quot;2026-04-14T00:00:00.000Z&quot;,
                 &quot;path&quot;:  &quot;/v2/community/lookup&quot;
             },
    &quot;data&quot;:  {

             },
    &quot;success&quot;:  true
}</code></pre>
{% endswagger-response %}

{% swagger-response status="400: Bad Request" description="The following 400 errors may be sent in response:" %}
<pre class="language-json"><code class="lang-json">{
    &quot;detail&quot;:  &quot;VALID BAD REQUEST REASON&quot;,
    &quot;instance&quot;:  &quot;/v2/community/lookup&quot;,
    &quot;traceId&quot;:  &quot;00000000-0000-0000-0000-000000000000&quot;,
    &quot;type&quot;:  &quot;https://httpstatuses.com/400&quot;,
    &quot;title&quot;:  &quot;Bad Request&quot;,
    &quot;status&quot;:  400
}</code></pre>
{% endswagger-response %}
{% endswagger %}


Looks up the authenticated community or another community by id or uuid.

#### Request

- Query parameters: `id` or `uuid`.

#### Response

- Returns the same summary shape as `GET /v2/community`.

```json
{
    "meta":  {
                 "timestamp":  "2026-04-14T00:00:00.000Z",
                 "path":  "/v2/community/lookup?id=YOUR_COMMUNITY_ID"
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


