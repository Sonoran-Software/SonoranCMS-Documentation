---
description: >-
  This endpoint allows you to set the form lock status for a specific template
  from your community.
---

# Set Form Lock Status

## Set Form Lock Status

<mark style="color:green;">`POST`</mark> `https://api.sonorancms.com/forms/set_lock_status`

Set the specific form template lock status

#### Request Body

| Name                                   | Type   | Description              |
| -------------------------------------- | ------ | ------------------------ |
| id<mark style="color:red;">\*</mark>   | string | Community ID             |
| key<mark style="color:red;">\*</mark>  | string | API Key                  |
| type<mark style="color:red;">\*</mark> | string | SET\_FORM\_LOCK\_STATUS  |
| data<mark style="color:red;">\*</mark> | array  | Array of request objects |

{% tabs %}
{% tab title="200: OK The following 200 response texts may be sent in response:" %}
```javascript
Successfully set the lock state for ${formTemplateLabel} to: ${state ? 'LOCKED' : 'UNLOCKED'}
```
{% endtab %}

{% tab title="400: Bad Request The following 400 errors may be sent in response:" %}
```javascript
INVALID API KEY
INVALID COMMUNITY ID
INVALID_TEMPLATE_ID
```
{% endtab %}
{% endtabs %}

```json
{
    "id": "YOUR_COMMUNITY_ID",
    "key": "YOUR_API_KEY",
    "type": "SET_FORM_LOCK_STATUS",
    "data": [
        {
            "templateId": 1,
            "state": true
        }
    ]
}
```

### Template ID

The `templateId` number can be taken from the form editor's URL when editing a form template.

<figure><img src="../../../../.gitbook/assets/image (65).png" alt="" width="375"><figcaption></figcaption></figure>
