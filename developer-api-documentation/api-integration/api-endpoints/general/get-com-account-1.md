---
description: >-
  This endpoint allows you to get community accounts paginated by sysStatus,
  comStatus, banned and archived.
---

# Get Accounts

{% swagger method="post" path="/general/get_accounts" baseUrl="https://api.sonorancms.com" summary="Get Accounts" %}
{% swagger-description %}
Get Sonoran CMS community accounts paginated by sysStatus, comStatus, banned and archived.
{% endswagger-description %}

{% swagger-parameter in="body" name="id" type="string" required="true" %}
Community ID
{% endswagger-parameter %}

{% swagger-parameter in="body" name="key" type="string" required="true" %}
API Key
{% endswagger-parameter %}

{% swagger-parameter in="body" required="true" name="type" type="string" %}
GET\_ACCOUNTS
{% endswagger-parameter %}

{% swagger-parameter in="body" required="true" name="data" type="array" %}
Array of request objects
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
<pre class="language-json"><code class="lang-json"><strong>{
</strong><strong>    "total": 10, // Total accounts found within parameters
</strong>    "skip": 0, // Accounts skipped in query
    "take": 25, // Min. 25, max amount of accounts that will be returned
    "accounts": [
        {
            "accId": "00000000-0000-0000-0000-000000000000",
            "accName": "TestAccount",
            "activeApiIds": ["000000000000000"],
            "discordId": "000000000000000",
            "sysStatus": true,
            "comStatus": true,
            "archived": false,
            "banned": false,
        },
        ...
    ]
<strong>}
</strong></code></pre>
{% endswagger-response %}

{% swagger-response status="400: Bad Request" description="The following 400 errors may be sent in response:" %}
```javascript
INVALID API KEY
INVALID COMMUNITY ID
```
{% endswagger-response %}
{% endswagger %}

```
{
    "id": "YOUR_COMMUNITY_ID",
    "key": "YOUR_API_KEY",
    "type": "GET_ACCOUNTS",
    "data": [
        {
            skip: number, // optional - total accounts skipped in query
            take: number, // optional - total accounts grabbed in query (min. 25 - max 100)
            sysStatus: boolean, // Within community acc parameter
            comStatus: boolean, // Active / pending community acc parameter
            banned: boolean, // Banned community acc parameter
            archived: boolean, // Archived community acc paramter
        }
    ]
}
```
