---
description: This endpoint allows you to ban an account from your community.
---

# Ban Account

## Ban Account

<mark style="color:green;">`POST`</mark> `https://api.sonorancms.com/general/ban_account`

Clock in/out a community account found by API ID or account ID.

#### Request Body

| Name                                   | Type   | Description                |
| -------------------------------------- | ------ | -------------------------- |
| id<mark style="color:red;">\*</mark>   | string | Community ID               |
| key<mark style="color:red;">\*</mark>  | string | API Key                    |
| type<mark style="color:red;">\*</mark> | string | CLOCK\_I&#x4E;_\__&#x4F;UT |
| data<mark style="color:red;">\*</mark> | array  | Array of request objects   |

{% tabs %}
{% tab title="200: OK The following 200 response texts may be sent in response:" %}
```javascript
CLOCKED IN
FORCE CLOCKED IN
CLOCKED OUT
```
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

```
{
    "id": "YOUR_COMMUNITY_ID",
    "key": "YOUR_API_KEY",
    "type": "BAN_ACCOUNT",
    "data": [
        {
            "apiId": "SOME_API_ID", // Optional - must have one
            "username": "SOMEUSERNAME", // Optional - must have one
            "accId": "SOMEACCID", // Optional - must have one
            "discord": "111122223333444455", // Optional - must have one
            "uniqueId": 1234 // Optional - must have one
        }
    ]
}
```

