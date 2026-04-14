---
description: Creates a player record in ER:LC tracking.
---

# Add ERLC Record

{% hint style="warning" %}
This endpoint requires `Authorization: Bearer <api key>`.
{% endhint %}

{% hint style="info" %}
Recommended safe rate limit: `18 requests/min` per credential.

The Kong gateway is configured slightly higher than these values to leave a small safety buffer for normal gameplay bursts.
{% endhint %}

## Add ERLC Record

<mark style="color:green;">`POST`</mark> `https://api.sonorancms.com/v2/community/erlc/records`
{% swagger method="post" path="/v2/community/erlc/records" baseUrl="https://api.sonorancms.com" summary="Add ERLC Record" %}
{% swagger-description %}
Creates a player record in ER:LC tracking.
{% endswagger-description %}

{% swagger-response status="200: OK" description="" %}
<pre class="language-json"><code class="lang-json">{
    &quot;meta&quot;:  {
                 &quot;timestamp&quot;:  &quot;2026-04-14T00:00:00.000Z&quot;,
                 &quot;path&quot;:  &quot;/v2/community/erlc/records&quot;
             },
    &quot;data&quot;:  {

             },
    &quot;success&quot;:  true
}</code></pre>
{% endswagger-response %}

{% swagger-response status="400: Bad Request" description="The following 400 errors may be sent in response:" %}
<pre class="language-json"><code class="lang-json">{
    &quot;detail&quot;:  &quot;VALID BAD REQUEST REASON&quot;,
    &quot;instance&quot;:  &quot;/v2/community/erlc/records&quot;,
    &quot;traceId&quot;:  &quot;00000000-0000-0000-0000-000000000000&quot;,
    &quot;type&quot;:  &quot;https://httpstatuses.com/400&quot;,
    &quot;title&quot;:  &quot;Bad Request&quot;,
    &quot;status&quot;:  400
}</code></pre>
{% endswagger-response %}
{% endswagger %}


Creates a player record in ER:LC tracking.

#### Request

- Body: `robloxJoinCode`, `executerDiscordId`, optional player identifiers, `type`, `reason`, and optional `points`.

```json
{
    "executerDiscordId":  "111122223333444455",
    "robloxJoinCode":  "JOIN-CODE",
    "reason":  "Example",
    "type":  "Note",
    "points":  1
}
```

#### Response

- Returns the tracking result inside the v2 envelope.

```json
{
    "meta":  {
                 "timestamp":  "2026-04-14T00:00:00.000Z",
                 "path":  "/v2/community/erlc/records"
             },
    "data":  {

             },
    "success":  true
}
```


