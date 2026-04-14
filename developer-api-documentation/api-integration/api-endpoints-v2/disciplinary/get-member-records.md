---
description: Returns the member disciplinary record history.
---

# Get Member Records

{% hint style="warning" %}
This endpoint requires `Authorization: Bearer <api key>`.
{% endhint %}

{% hint style="info" %}
Recommended safe rate limit: `27 requests/min` per credential.

The Kong gateway is configured slightly higher than these values to leave a small safety buffer for normal gameplay bursts.
{% endhint %}

## Get Member Records

<mark style="color:green;">`GET`</mark> `https://api.sonorancms.com/v2/community/disciplinary/accounts/:accountId/records`
{% swagger method="get" path="/v2/community/disciplinary/accounts/:accountId/records" baseUrl="https://api.sonorancms.com" summary="Get Member Records" %}
{% swagger-description %}
Returns the member disciplinary record history.
{% endswagger-description %}

{% swagger-parameter in="path" name="accountId" type="string" required="true" %}
account ID
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
<pre class="language-json"><code class="lang-json">{
    &quot;meta&quot;:  {
                 &quot;timestamp&quot;:  &quot;2026-04-14T00:00:00.000Z&quot;,
                 &quot;path&quot;:  &quot;/v2/community/disciplinary/accounts/:accountId/records&quot;
             },
    &quot;data&quot;:  {

             },
    &quot;success&quot;:  true
}</code></pre>
{% endswagger-response %}

{% swagger-response status="400: Bad Request" description="The following 400 errors may be sent in response:" %}
<pre class="language-json"><code class="lang-json">{
    &quot;detail&quot;:  &quot;VALID BAD REQUEST REASON&quot;,
    &quot;instance&quot;:  &quot;/v2/community/disciplinary/accounts/:accountId/records&quot;,
    &quot;traceId&quot;:  &quot;00000000-0000-0000-0000-000000000000&quot;,
    &quot;type&quot;:  &quot;https://httpstatuses.com/400&quot;,
    &quot;title&quot;:  &quot;Bad Request&quot;,
    &quot;status&quot;:  400
}</code></pre>
{% endswagger-response %}

{% swagger-response status="404: Not Found" description="The following 404 errors may be sent in response:" %}
<pre class="language-json"><code class="lang-json">{
    &quot;detail&quot;:  &quot;NOT FOUND&quot;,
    &quot;instance&quot;:  &quot;/v2/community/disciplinary/accounts/:accountId/records&quot;,
    &quot;traceId&quot;:  &quot;00000000-0000-0000-0000-000000000000&quot;,
    &quot;type&quot;:  &quot;https://httpstatuses.com/404&quot;,
    &quot;title&quot;:  &quot;Not Found&quot;,
    &quot;status&quot;:  404
}</code></pre>
{% endswagger-response %}
{% endswagger %}


Returns the member disciplinary record history.

#### Request

- Path parameter: `accountId` (UUID).
- Optional identity lookup query fields are supported.

#### Response

- Returns the member records list inside the v2 envelope.

```json
{
    "meta":  {
                 "timestamp":  "2026-04-14T00:00:00.000Z",
                 "path":  "/v2/community/disciplinary/accounts/00000000-0000-0000-0000-000000000000/records"
             },
    "data":  [

             ],
    "success":  true
}
```


