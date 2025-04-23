---
description: This endpoint allows you to get a member's disciplinary points
---

# Get Member Points

## Get Member Points

<mark style="color:green;">`POST`</mark> `https://api.sonorancms.com/disciplinary/get_member_points`

Get a Sonoran CMS community member's disciplinary points by member search fields.

#### Request Body

| Name                                   | Type   | Description         |
| -------------------------------------- | ------ | ------------------- |
| id<mark style="color:red;">\*</mark>   | string | Community ID        |
| key<mark style="color:red;">\*</mark>  | string | API Key             |
| type<mark style="color:red;">\*</mark> | string | GET\_MEMBER\_POINTS |
| data<mark style="color:red;">\*</mark> | object | Object              |

{% tabs %}
{% tab title="200: OK " %}
```json
10
```
{% endtab %}

{% tab title="400: Bad Request The following 400 errors may be sent in response:" %}
```javascript
INVALID API KEY
INVALID COMMUNITY ID
MEMBER NOT FOUND
```
{% endtab %}
{% endtabs %}

```json
{
    "id": "YOUR_COMMUNITY_ID",
    "key": "YOUR_API_KEY",
    "type": "GET_MEMBER_POINTS",
    "data": {
        "apiId": "SOME_API_ID", // Optional - must have one
        "username": "SOMEUSERNAME", // Optional - must have one
        "accId": "SOMEACCID", // Optional - must have one
        "discord": "111122223333444455", // Optional - must have one
        "uniqueId": 1234 // Optional - must have one
    }
}
```
