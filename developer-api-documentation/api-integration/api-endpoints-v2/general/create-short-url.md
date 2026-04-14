---
description: Creates or resolves a short URL for the community.
---

# Create Short URL

{% hint style="warning" %}
This endpoint requires `Authorization: Bearer <api key>`.
{% endhint %}

{% hint style="info" %}
Recommended safe rate limit: `13 requests/min` per credential.

The Kong gateway is configured slightly higher than these values to leave a small safety buffer for normal gameplay bursts.
{% endhint %}

## Create Short URL

<mark style="color:green;">`POST`</mark> `https://api.sonorancms.com/v2/community/short-urls`
{% swagger method="post" path="/v2/community/short-urls" baseUrl="https://api.sonorancms.com" summary="Create Short URL" %}
{% swagger-description %}
Creates or resolves a short URL for the community.
{% endswagger-description %}

{% swagger-response status="200: OK" description="" %}
<pre class="language-json"><code class="lang-json">{
    &quot;meta&quot;:  {
                 &quot;timestamp&quot;:  &quot;2026-04-14T00:00:00.000Z&quot;,
                 &quot;path&quot;:  &quot;/v2/community/short-urls&quot;
             },
    &quot;data&quot;:  {

             },
    &quot;success&quot;:  true
}</code></pre>
{% endswagger-response %}

{% swagger-response status="400: Bad Request" description="The following 400 errors may be sent in response:" %}
<pre class="language-json"><code class="lang-json">{
    &quot;detail&quot;:  &quot;VALID BAD REQUEST REASON&quot;,
    &quot;instance&quot;:  &quot;/v2/community/short-urls&quot;,
    &quot;traceId&quot;:  &quot;00000000-0000-0000-0000-000000000000&quot;,
    &quot;type&quot;:  &quot;https://httpstatuses.com/400&quot;,
    &quot;title&quot;:  &quot;Bad Request&quot;,
    &quot;status&quot;:  400
}</code></pre>
{% endswagger-response %}
{% endswagger %}


Creates or resolves a short URL for the community.

#### Request

- Body: `path` and optional `isCustomDomain`.

```json
{
    "isCustomDomain":  false,
    "path":  "docs"
}
```

#### Response

- Returns the resolved URL or a short URL lookup result.

```json
{
    "meta":  {
                 "timestamp":  "2026-04-14T00:00:00.000Z",
                 "path":  "/v2/community/short-urls"
             },
    "data":  {
                 "url":  "https://example.com/docs"
             },
    "success":  true
}
```


