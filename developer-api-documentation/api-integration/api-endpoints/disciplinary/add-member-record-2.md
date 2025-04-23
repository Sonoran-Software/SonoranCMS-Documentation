---
description: This endpoint allows you to update a disciplinary record's reason
---

# Update Member Record Reason

## Update Member Record Reason

<mark style="color:green;">`POST`</mark> `https://api.sonorancms.com/disciplinary/update_member_record_reason`&#x20;

Update a Sonoran CMS community member disciplinary record's reason.

#### Request Body

| Name                                   | Type   | Description                    |
| -------------------------------------- | ------ | ------------------------------ |
| id<mark style="color:red;">\*</mark>   | string | Community ID                   |
| key<mark style="color:red;">\*</mark>  | string | API Key                        |
| type<mark style="color:red;">\*</mark> | string | UPDATE\_MEMBER\_RECORD\_REASON |
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
      "reason": "Some different reason",
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
        "reason": "Some different reason", // Reason for the disciplinary record
    }
}
```
