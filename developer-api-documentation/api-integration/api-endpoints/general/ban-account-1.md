---
description: >-
  This endpoint allows you to edit an account's profile field within your
  community.
---

# Edit Account Profile Fields

## Edit Account Profile Fields

<mark style="color:green;">`POST`</mark> `https://api.sonorancms.com/general/edit_acc_profile_fields`

Edit profile fields on a community account found by API ID or account ID.

#### Request Body

| Name                                   | Type   | Description                |
| -------------------------------------- | ------ | -------------------------- |
| id<mark style="color:red;">\*</mark>   | string | Community ID               |
| key<mark style="color:red;">\*</mark>  | string | API Key                    |
| type<mark style="color:red;">\*</mark> | string | CLOCK\_I&#x4E;_\__&#x4F;UT |
| data<mark style="color:red;">\*</mark> | array  | Array of request objects   |

{% tabs %}
{% tab title="200: OK The following 200 response texts may be sent in response:" %}
<pre class="language-javascript"><code class="lang-javascript"><strong>[
</strong><strong>    {
</strong><strong>        "id": "d9d1288e-3892-40d6-acc5-be2c3d294bd4",
</strong>        "value": ["some", "strings", "for", "array"]
<strong>    },
</strong><strong>    ... // This will return all profile fields that have data associated from the account
</strong><strong>]
</strong></code></pre>
{% endtab %}

{% tab title="400: Bad Request The following 400 errors may be sent in response:" %}
```javascript
INVALID API KEY
INVALID COMMUNITY ID
API ID NOT LINKED TO AN ACCOUNT IN THIS COMMUNITY
```
{% endtab %}

{% tab title="404: Not Found The following 404 errors may be sent in response:" %}
```javascript
API ID NOT LINKED TO AN ACCOUNT IN THIS COMMUNITY
```
{% endtab %}
{% endtabs %}

```json
{
    "id": "YOUR_COMMUNITY_ID",
    "key": "YOUR_API_KEY",
    "type": "EDIT_ACC_PROFLIE_FIELDS",
    "data": [
        {
            // User Identification
            "apiId": "SOME_API_ID", // Optional - must have one
            "username": "SOMEUSERNAME", // Optional - must have one
            "accId": "SOMEACCID", // Optional - must have one
            "discord": "111122223333444455", // Optional - must have one
            "uniqueId": 1234 // Optional - must have one
            // Configuration
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

