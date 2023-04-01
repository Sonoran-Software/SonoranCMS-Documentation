---
description: Provides all profile fields associated and configured by the community.
---

# Get Profile Fields

{% hint style="danger" %}
**NOT IN PRODUCTION**
{% endhint %}

{% hint style="warning" %}
API endpoint requires the **Standard** version of Sonoran CMS or higher.\
For more information, see our [pricing ](../../../../pricing/pricing-faq/)page.
{% endhint %}

{% swagger method="post" path="/general/get_profile_fields" baseUrl="https://api.sonorancms.com" summary="Get Profile Fields" %}
{% swagger-description %}
Get a Sonoran CMS community account's ranks by account ID, API ID, or username.
{% endswagger-description %}

{% swagger-parameter in="body" name="id" type="string" required="true" %}
Community ID
{% endswagger-parameter %}

{% swagger-parameter in="body" name="key" type="string" required="true" %}
API Key
{% endswagger-parameter %}

{% swagger-parameter in="body" required="true" name="type" type="string" %}
GET_COM_ACCOUNT
{% endswagger-parameter %}

{% swagger-parameter in="body" required="true" name="data" type="array" %}
Array of request objects
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
<pre class="language-javascript"><code class="lang-javascript">[
    {
<strong>        "id": "d9d1288e-3892-40d6-acc5-be2c3d294bd4",
</strong>        "type": "text array",
        "label": "Steam IDs",
        "options": null
    },
    ...
]
</code></pre>
{% endswagger-response %}

{% swagger-response status="400: Bad Request" description="The following 400 errors may be sent in response:" %}
```javascript
INVALID API KEY
INVALID COMMUNITY ID
API ID NOT LINKED TO AN ACCOUNT IN THIS COMMUNITY
NO ACCOUNT FOUND UNDER GIVEN PARAMETERS IN THIS COMMUNITY
```
{% endswagger-response %}
{% endswagger %}

```
{
    "id": "YOUR_COMMUNITY_ID",
    "key": "YOUR_API_KEY",
    "type": "GET_PROFILE_FIELDS"
}
```
