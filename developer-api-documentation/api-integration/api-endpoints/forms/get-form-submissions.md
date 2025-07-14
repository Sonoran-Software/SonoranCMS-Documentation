---
description: >-
  This endpoint allows you to get form submissions for a specific template from
  your community.
---

# Get Form Submissions

## Get Form Submissions

<mark style="color:green;">`POST`</mark> `https://api.sonorancms.com/forms/get_template_submissions`

Get all form submissions for a specific template with pagination

#### Request Body

| Name                                   | Type   | Description                      |
| -------------------------------------- | ------ | -------------------------------- |
| id<mark style="color:red;">\*</mark>   | string | Community ID                     |
| key<mark style="color:red;">\*</mark>  | string | API Key                          |
| type<mark style="color:red;">\*</mark> | string | GET\_FORM\_TEMPLATE\_SUBMISSIONS |
| data<mark style="color:red;">\*</mark> | array  | Array of request objects         |

{% tabs %}
{% tab title="200: OK The following 200 response texts may be sent in response:" %}
```javascript
[
    {
        ...
    }
]
```
{% endtab %}

{% tab title="400: Bad Request The following 400 errors may be sent in response:" %}
```javascript
INVALID API KEY
INVALID COMMUNITY ID
```
{% endtab %}
{% endtabs %}

```json
{
    "id": "YOUR_COMMUNITY_ID",
    "key": "YOUR_API_KEY",
    "type": "GET_FORM_TEMPLATE_SUBMISSIONS",
    "data": [
        {
            "templateId": 1,
            "skip": 0,
            "take": 50, // Capped at 50
        }
    ]
}
```
