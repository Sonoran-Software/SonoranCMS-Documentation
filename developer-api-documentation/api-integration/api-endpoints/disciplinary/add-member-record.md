---
description: This endpoint allows you to add a disciplinary record to a member
---

# Add Member Record

## Add Member Record

<mark style="color:green;">`POST`</mark> `https://api.sonorancms.com/disciplinary/add_member_record`

Add a Sonoran CMS community member disciplinary record by member search fields.

#### Request Body

| Name                                   | Type   | Description         |
| -------------------------------------- | ------ | ------------------- |
| id<mark style="color:red;">\*</mark>   | string | Community ID        |
| key<mark style="color:red;">\*</mark>  | string | API Key             |
| type<mark style="color:red;">\*</mark> | string | ADD\_MEMBER\_RECORD |
| data<mark style="color:red;">\*</mark> | object | Object              |

{% tabs %}
{% tab title="200: OK " %}
```json
{
      "id": "123",
      "status": true,
      "accId": "123",
      "source": "api",
      "sourceId": "api-request",
      "points": 10,
      "reason": "Some reason",
      "metadata": {},
      "history": [],
}
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
    "type": "ADD_MEMBER_RECORD",
    "data": {
        "apiId": "SOME_API_ID", // Optional - must have one
        "username": "SOMEUSERNAME", // Optional - must have one
        "accId": "SOMEACCID", // Optional - must have one
        "discord": "111122223333444455", // Optional - must have one
        "uniqueId": 1234 // Optional - must have one
        "points": 10, // How many points this disciplinary record incurs
        "reason": "Some reason", // Reason for the disciplinary record
    }
}
```
