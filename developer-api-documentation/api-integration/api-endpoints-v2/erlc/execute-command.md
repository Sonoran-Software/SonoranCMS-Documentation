---
description: Executes an ER:LC command.
---

# Execute Command

{% hint style="warning" %}
This endpoint requires `Authorization: Bearer <api key>`.
{% endhint %}

{% hint style="info" %}
Recommended safe rate limit: `18 requests/min` per credential.

The Kong gateway is configured slightly higher than these values to leave a small safety buffer for normal gameplay bursts.
{% endhint %}

## Execute Command

<mark style="color:green;">`POST`</mark> `https://api.sonorancms.com/v2/community/erlc/commands`
{% swagger method="post" path="/v2/community/erlc/commands" baseUrl="https://api.sonorancms.com" summary="Execute Command" %}
{% swagger-description %}
Executes an ER:LC command.
{% endswagger-description %}

{% swagger-response status="200: OK" description="" %}
<pre class="language-json"><code class="lang-json">{
    &quot;meta&quot;:  {
                 &quot;timestamp&quot;:  &quot;2026-04-14T00:00:00.000Z&quot;,
                 &quot;path&quot;:  &quot;/v2/community/erlc/commands&quot;
             },
    &quot;data&quot;:  {

             },
    &quot;success&quot;:  true
}</code></pre>
{% endswagger-response %}

{% swagger-response status="400: Bad Request" description="The following 400 errors may be sent in response:" %}
<pre class="language-json"><code class="lang-json">{
    &quot;detail&quot;:  &quot;VALID BAD REQUEST REASON&quot;,
    &quot;instance&quot;:  &quot;/v2/community/erlc/commands&quot;,
    &quot;traceId&quot;:  &quot;00000000-0000-0000-0000-000000000000&quot;,
    &quot;type&quot;:  &quot;https://httpstatuses.com/400&quot;,
    &quot;title&quot;:  &quot;Bad Request&quot;,
    &quot;status&quot;:  400
}</code></pre>
{% endswagger-response %}
{% endswagger %}


Executes an ER:LC command.

#### Request

- Body: `robloxJoinCode`, `discordId`, `type`, `args`, and optional `includesPlayerNameOrId`.

```json
{
    "args":  "test",
    "discordId":  "111122223333444455",
    "robloxJoinCode":  "JOIN-CODE",
    "includesPlayerNameOrId":  false,
    "type":  "Command"
}
```

#### Response

- Returns the command execution result inside the v2 envelope.

```json
{
    "meta":  {
                 "timestamp":  "2026-04-14T00:00:00.000Z",
                 "path":  "/v2/community/erlc/commands"
             },
    "data":  {

             },
    "success":  true
}
```


