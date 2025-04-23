---
description: This endpoint allows you to update a disciplinary record's points
---

# Update Member Record Points

## Update Member Record Points

<mark style="color:green;">`POST`</mark> `https://api.sonorancms.com/disciplinary/update_member_record_points`&#x20;

Update a Sonoran CMS community member disciplinary record's points.

#### Request Body

| Name                                   | Type   | Description                    |
| -------------------------------------- | ------ | ------------------------------ |
| id<mark style="color:red;">\*</mark>   | string | Community ID                   |
| key<mark style="color:red;">\*</mark>  | string | API Key                        |
| type<mark style="color:red;">\*</mark> | string | UPDATE\_MEMBER\_RECORD\_POINTS |
| data<mark style="color:red;">\*</mark> | object | Object                         |

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
    "type": "UPDATE_MEMBER_RECORD_POINTS",
    "data": {
        "recordId": "123",
        "points": 10, // How many points this disciplinary record incurs
    }
}
```
