---
description: >-
  This endpoint allows you to edit an account's profile field within your
  community.
---

# Edit Account Profile Fields

{% swagger method="post" path="/general/edit_acc_profile_fields" baseUrl="https://api.sonorancms.com" summary="Edit Account Profile Fields" %}
{% swagger-description %}
Edit profile fields on a community account found by API ID or account ID.
{% endswagger-description %}

{% swagger-parameter in="body" name="id" type="string" required="true" %}
Community ID
{% endswagger-parameter %}

{% swagger-parameter in="body" name="key" type="string" required="true" %}
API Key
{% endswagger-parameter %}

{% swagger-parameter in="body" required="true" name="type" type="string" %}
CLOCK\_IN_\__OUT
{% endswagger-parameter %}

{% swagger-parameter in="body" required="true" name="data" type="array" %}
Array of request objects
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="The following 200 response texts may be sent in response:" %}
<pre class="language-javascript"><code class="lang-javascript"><strong>[
</strong><strong>    {
</strong><strong>        "id": "d9d1288e-3892-40d6-acc5-be2c3d294bd4",
</strong>        "value": ["some", "strings", "for", "array"]
<strong>    },
</strong><strong>    ... // This will return all profile fields that have data associated from the account
</strong><strong>]
</strong></code></pre>
{% endswagger-response %}

{% swagger-response status="400: Bad Request" description="The following 400 errors may be sent in response:" %}
```javascript
INVALID API KEY
INVALID COMMUNITY ID
API ID NOT LINKED TO AN ACCOUNT IN THIS COMMUNITY
```
{% endswagger-response %}

{% swagger-response status="404: Not Found" description="The following 404 errors may be sent in response:" %}
```javascript
API ID NOT LINKED TO AN ACCOUNT IN THIS COMMUNITY
```
{% endswagger-response %}
{% endswagger %}

```json
{
    "id": "YOUR_COMMUNITY_ID",
    "key": "YOUR_API_KEY",
    "type": "EDIT_ACC_PROFLIE_FIELDS",
    "data": [
        {
            "apiId": "SOME_API_ID", // Optional - must have one (apiId or accId)
            "accId": "SOMEACCID", // Optional - must have one (apiId or accId)
            "profileFields": [
                {
                    "id": "d9d1288e-3892-40d6-acc5-be2c3d294bd4",
                    "value": ["some", "strings", "for", "array"]
                },
                ... // You can supply a min. of one profile field but can take as many "update" objects as needed.
            ]
        }
    ]
}
```

