---
description: Creates an RSVP for a community event.
---

# RSVP

{% hint style="warning" %}
This endpoint requires `Authorization: Bearer <api key>`.
{% endhint %}

{% hint style="info" %}
Recommended safe rate limit: `27 requests/min` per credential.

The Kong gateway is configured slightly higher than these values to leave a small safety buffer for normal gameplay bursts.
{% endhint %}

## RSVP

<mark style="color:green;">`POST`</mark> `https://api.sonorancms.com/v2/community/events/:eventId/rsvps`
{% swagger method="post" path="/v2/community/events/:eventId/rsvps" baseUrl="https://api.sonorancms.com" summary="RSVP" %}
{% swagger-description %}
Creates an RSVP for a community event.
{% endswagger-description %}

{% swagger-parameter in="path" name="eventId" type="string" required="true" %}
event ID
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
<pre class="language-json"><code class="lang-json">{
    &quot;meta&quot;:  {
                 &quot;timestamp&quot;:  &quot;2026-04-14T00:00:00.000Z&quot;,
                 &quot;path&quot;:  &quot;/v2/community/events/:eventId/rsvps&quot;
             },
    &quot;data&quot;:  {

             },
    &quot;success&quot;:  true
}</code></pre>
{% endswagger-response %}

{% swagger-response status="400: Bad Request" description="The following 400 errors may be sent in response:" %}
<pre class="language-json"><code class="lang-json">{
    &quot;detail&quot;:  &quot;VALID BAD REQUEST REASON&quot;,
    &quot;instance&quot;:  &quot;/v2/community/events/:eventId/rsvps&quot;,
    &quot;traceId&quot;:  &quot;00000000-0000-0000-0000-000000000000&quot;,
    &quot;type&quot;:  &quot;https://httpstatuses.com/400&quot;,
    &quot;title&quot;:  &quot;Bad Request&quot;,
    &quot;status&quot;:  400
}</code></pre>
{% endswagger-response %}

{% swagger-response status="404: Not Found" description="The following 404 errors may be sent in response:" %}
<pre class="language-json"><code class="lang-json">{
    &quot;detail&quot;:  &quot;NOT FOUND&quot;,
    &quot;instance&quot;:  &quot;/v2/community/events/:eventId/rsvps&quot;,
    &quot;traceId&quot;:  &quot;00000000-0000-0000-0000-000000000000&quot;,
    &quot;type&quot;:  &quot;https://httpstatuses.com/404&quot;,
    &quot;title&quot;:  &quot;Not Found&quot;,
    &quot;status&quot;:  404
}</code></pre>
{% endswagger-response %}
{% endswagger %}


Creates an RSVP for a community event.

#### Request

- Path parameter: `eventId` (UUID).
- Body supports the standard identity fields used by the backend.

```json
{
    "accId":  "00000000-0000-0000-0000-000000000000"
}
```

#### Response

- Returns the RSVP service result inside the v2 envelope.

```json
{
    "meta":  {
                 "timestamp":  "2026-04-14T00:00:00.000Z",
                 "path":  "/v2/community/events/00000000-0000-0000-0000-000000000000/rsvps"
             },
    "data":  {

             },
    "success":  true
}
```


