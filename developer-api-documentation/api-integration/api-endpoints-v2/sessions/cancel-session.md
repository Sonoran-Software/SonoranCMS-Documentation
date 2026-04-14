---
description: Cancels a session without returning a response body.
---

# Cancel Session

{% hint style="warning" %}
This endpoint requires `Authorization: Bearer <api key>`.
{% endhint %}

{% hint style="info" %}
Recommended safe rate limit: `9 requests/min` per credential.

The Kong gateway is configured slightly higher than these values to leave a small safety buffer for normal gameplay bursts.
{% endhint %}

## Cancel Session

<mark style="color:green;">`DELETE`</mark> `https://api.sonorancms.com/v2/community/sessions`
{% swagger method="delete" path="/v2/community/sessions" baseUrl="https://api.sonorancms.com" summary="Cancel Session" %}
{% swagger-description %}
Cancels a session without returning a response body.
{% endswagger-description %}

{% swagger-response status="200: OK" description="" %}
<pre class="language-json"><code class="lang-json">{
    &quot;meta&quot;:  {
                 &quot;timestamp&quot;:  &quot;2026-04-14T00:00:00.000Z&quot;,
                 &quot;path&quot;:  &quot;/v2/community/sessions&quot;
             },
    &quot;data&quot;:  {

             },
    &quot;success&quot;:  true
}</code></pre>
{% endswagger-response %}

{% swagger-response status="400: Bad Request" description="The following 400 errors may be sent in response:" %}
<pre class="language-json"><code class="lang-json">{
    &quot;detail&quot;:  &quot;VALID BAD REQUEST REASON&quot;,
    &quot;instance&quot;:  &quot;/v2/community/sessions&quot;,
    &quot;traceId&quot;:  &quot;00000000-0000-0000-0000-000000000000&quot;,
    &quot;type&quot;:  &quot;https://httpstatuses.com/400&quot;,
    &quot;title&quot;:  &quot;Bad Request&quot;,
    &quot;status&quot;:  400
}</code></pre>
{% endswagger-response %}

{% swagger-response status="204: No Content" description="The session was canceled successfully." %}
No content returned.
{% endswagger-response %}
{% endswagger %}


Cancels a session without returning a response body.

#### Request

- Body uses the same shape as `POST /v2/community/sessions`.

```json
{
    "accId":  "member-account-id",
    "serverId":  1
}
```

#### Response

- Returns `204 No Content`.


