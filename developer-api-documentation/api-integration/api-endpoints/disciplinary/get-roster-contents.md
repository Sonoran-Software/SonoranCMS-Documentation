---
description: This endpoint allows you to get a member's disciplinary records
---

# Get Member Records

## Get Member Records

<mark style="color:green;">`POST`</mark> `https://api.sonorancms.com/disciplinary/get_member_records`

Get a Sonoran CMS community member's disciplinary records by member search fields.

#### Request Body

| Name                                   | Type   | Description          |
| -------------------------------------- | ------ | -------------------- |
| id<mark style="color:red;">\*</mark>   | string | Community ID         |
| key<mark style="color:red;">\*</mark>  | string | API Key              |
| type<mark style="color:red;">\*</mark> | string | GET\_MEMBER\_RECORDS |
| data<mark style="color:red;">\*</mark> | object | Object               |

{% tabs %}
{% tab title="200: OK " %}
```json
  [
    {
      "id": "123",
      "status": true,
      "accId": "123",
      "source": "user",
      "sourceId": "123",
      "points": 5,
      "reason": "",
      "metadata": {},
      "history": [],
    }
  ]
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
    "type": "GET_MEMBER_RECORDS",
    "data": {
        "apiId": "SOME_API_ID", // Optional - must have one
        "username": "SOMEUSERNAME", // Optional - must have one
        "accId": "SOMEACCID", // Optional - must have one
        "discord": "111122223333444455", // Optional - must have one
        "uniqueId": 1234 // Optional - must have one
    }
}
```
