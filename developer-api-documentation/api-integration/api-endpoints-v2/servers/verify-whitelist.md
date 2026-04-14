---
description: Checks whether an identity is whitelisted on the server.
---

# Verify Whitelist

{% hint style="warning" %}
This endpoint requires `Authorization: Bearer <api key>`.
{% endhint %}

{% hint style="info" %}
Recommended safe rate limit: `27 requests/min` per credential.

The Kong gateway is configured slightly higher than these values to leave a small safety buffer for normal gameplay bursts.
{% endhint %}

## Verify Whitelist

<mark style="color:green;">`POST`</mark> `https://api.sonorancms.com/v2/community/servers/:serverId/whitelist/check`
{% swagger method="post" path="/v2/community/servers/:serverId/whitelist/check" baseUrl="https://api.sonorancms.com" summary="Verify Whitelist" %}
{% swagger-description %}
Checks whether an identity is whitelisted on the server.
{% endswagger-description %}

{% swagger-parameter in="path" name="serverId" type="number" required="true" %}
server ID
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
<pre class="language-json"><code class="lang-json">{
    &quot;meta&quot;:  {
                 &quot;timestamp&quot;:  &quot;2026-04-14T00:00:00.000Z&quot;,
                 &quot;path&quot;:  &quot;/v2/community/servers/:serverId/whitelist/check&quot;
             },
    &quot;data&quot;:  {

             },
    &quot;success&quot;:  true
}</code></pre>
{% endswagger-response %}

{% swagger-response status="400: Bad Request" description="The following 400 errors may be sent in response:" %}
<pre class="language-json"><code class="lang-json">{
    &quot;detail&quot;:  &quot;VALID BAD REQUEST REASON&quot;,
    &quot;instance&quot;:  &quot;/v2/community/servers/:serverId/whitelist/check&quot;,
    &quot;traceId&quot;:  &quot;00000000-0000-0000-0000-000000000000&quot;,
    &quot;type&quot;:  &quot;https://httpstatuses.com/400&quot;,
    &quot;title&quot;:  &quot;Bad Request&quot;,
    &quot;status&quot;:  400
}</code></pre>
{% endswagger-response %}

{% swagger-response status="404: Not Found" description="The following 404 errors may be sent in response:" %}
<pre class="language-json"><code class="lang-json">{
    &quot;detail&quot;:  &quot;NOT FOUND&quot;,
    &quot;instance&quot;:  &quot;/v2/community/servers/:serverId/whitelist/check&quot;,
    &quot;traceId&quot;:  &quot;00000000-0000-0000-0000-000000000000&quot;,
    &quot;type&quot;:  &quot;https://httpstatuses.com/404&quot;,
    &quot;title&quot;:  &quot;Not Found&quot;,
    &quot;status&quot;:  404
}</code></pre>
{% endswagger-response %}
{% endswagger %}


Checks whether an identity is whitelisted on the server.

#### Request

- Body supports the standard identity fields used elsewhere in v2.
- Path parameter: `serverId` (integer).

```json
{
    "accId":  "00000000-0000-0000-0000-000000000000",
    "username":  "TestUser"
}
```

#### Response

- Returns the whitelist result as a plain success response or a problem-details error if access is denied.

```json
{
    "meta":  {
                 "timestamp":  "2026-04-14T00:00:00.000Z",
                 "path":  "/v2/community/servers/1/whitelist/check"
             },
    "data":  {
                 "whitelisted":  true
             },
    "success":  true
}
```


