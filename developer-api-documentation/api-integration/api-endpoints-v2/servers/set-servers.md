---
description: Replaces the full server list.
---

# Set Servers

{% hint style="warning" %}
This endpoint requires `Authorization: Bearer <api key>`.
{% endhint %}

{% hint style="info" %}
Recommended safe rate limit: `9 requests/min` per credential.

The Kong gateway is configured slightly higher than these values to leave a small safety buffer for normal gameplay bursts.
{% endhint %}

## Set Servers

<mark style="color:green;">`PUT`</mark> `https://api.sonorancms.com/v2/community/servers`
{% swagger method="put" path="/v2/community/servers" baseUrl="https://api.sonorancms.com" summary="Set Servers" %}
{% swagger-description %}
Replaces the full server list.
{% endswagger-description %}

{% swagger-response status="200: OK" description="" %}
<pre class="language-json"><code class="lang-json">{
    &quot;meta&quot;:  {
                 &quot;timestamp&quot;:  &quot;2026-04-14T00:00:00.000Z&quot;,
                 &quot;path&quot;:  &quot;/v2/community/servers&quot;
             },
    &quot;data&quot;:  {

             },
    &quot;success&quot;:  true
}</code></pre>
{% endswagger-response %}

{% swagger-response status="400: Bad Request" description="The following 400 errors may be sent in response:" %}
<pre class="language-json"><code class="lang-json">{
    &quot;detail&quot;:  &quot;VALID BAD REQUEST REASON&quot;,
    &quot;instance&quot;:  &quot;/v2/community/servers&quot;,
    &quot;traceId&quot;:  &quot;00000000-0000-0000-0000-000000000000&quot;,
    &quot;type&quot;:  &quot;https://httpstatuses.com/400&quot;,
    &quot;title&quot;:  &quot;Bad Request&quot;,
    &quot;status&quot;:  400
}</code></pre>
{% endswagger-response %}
{% endswagger %}


Replaces the full server list.

#### Request

- Body: `servers` array of server objects.

```json
{
    "servers":  [
                    {
                        "id":  1,
                        "name":  "Main Server",
                        "type":  "fivem",
                        "description":  "Primary game server",
                        "ip":  "127.0.0.1",
                        "port":  "30120"
                    }
                ]
}
```

#### Response

- Returns the updated server list inside the v2 envelope.

```json
{
    "meta":  {
                 "timestamp":  "2026-04-14T00:00:00.000Z",
                 "path":  "/v2/community/servers"
             },
    "data":  [

             ],
    "success":  true
}
```


