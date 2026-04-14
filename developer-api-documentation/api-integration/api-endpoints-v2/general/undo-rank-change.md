---
description: Undoes a promotion or rank change by ID.
---

# Undo Rank Change

{% hint style="warning" %}
This endpoint requires `Authorization: Bearer <api key>`.
{% endhint %}

{% hint style="info" %}
Recommended safe rate limit: `13 requests/min` per credential.

The Kong gateway is configured slightly higher than these values to leave a small safety buffer for normal gameplay bursts.
{% endhint %}

## Undo Rank Change

<mark style="color:green;">`POST`</mark> `https://api.sonorancms.com/v2/community/rank-changes/:undoId/undo`
{% swagger method="post" path="/v2/community/rank-changes/:undoId/undo" baseUrl="https://api.sonorancms.com" summary="Undo Rank Change" %}
{% swagger-description %}
Undoes a promotion or rank change by ID.
{% endswagger-description %}

{% swagger-parameter in="path" name="undoId" type="string" required="true" %}
undo ID
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
<pre class="language-json"><code class="lang-json">{
    &quot;meta&quot;:  {
                 &quot;timestamp&quot;:  &quot;2026-04-14T00:00:00.000Z&quot;,
                 &quot;path&quot;:  &quot;/v2/community/rank-changes/:undoId/undo&quot;
             },
    &quot;data&quot;:  {

             },
    &quot;success&quot;:  true
}</code></pre>
{% endswagger-response %}

{% swagger-response status="400: Bad Request" description="The following 400 errors may be sent in response:" %}
<pre class="language-json"><code class="lang-json">{
    &quot;detail&quot;:  &quot;VALID BAD REQUEST REASON&quot;,
    &quot;instance&quot;:  &quot;/v2/community/rank-changes/:undoId/undo&quot;,
    &quot;traceId&quot;:  &quot;00000000-0000-0000-0000-000000000000&quot;,
    &quot;type&quot;:  &quot;https://httpstatuses.com/400&quot;,
    &quot;title&quot;:  &quot;Bad Request&quot;,
    &quot;status&quot;:  400
}</code></pre>
{% endswagger-response %}

{% swagger-response status="404: Not Found" description="The following 404 errors may be sent in response:" %}
<pre class="language-json"><code class="lang-json">{
    &quot;detail&quot;:  &quot;NOT FOUND&quot;,
    &quot;instance&quot;:  &quot;/v2/community/rank-changes/:undoId/undo&quot;,
    &quot;traceId&quot;:  &quot;00000000-0000-0000-0000-000000000000&quot;,
    &quot;type&quot;:  &quot;https://httpstatuses.com/404&quot;,
    &quot;title&quot;:  &quot;Not Found&quot;,
    &quot;status&quot;:  404
}</code></pre>
{% endswagger-response %}
{% endswagger %}


Undoes a promotion or rank change by ID.

#### Request

- Path parameter: `undoId` (UUID).
- Body: optional `userId` UUID for audit attribution.

```json
{
    "userId":  "00000000-0000-0000-0000-000000000000"
}
```

#### Response

- Returns the undo operation result inside the v2 envelope.

```json
{
    "meta":  {
                 "timestamp":  "2026-04-14T00:00:00.000Z",
                 "path":  "/v2/community/rank-changes/00000000-0000-0000-0000-000000000000/undo"
             },
    "data":  {

             },
    "success":  true
}
```


