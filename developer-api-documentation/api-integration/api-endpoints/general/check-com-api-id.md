---
description: This endpoint allows you to check a community API ID.
---

# Check Com API ID

## Check Com APIID

<mark style="color:green;">`POST`</mark> `https://api.sonorancms.com/general/check_com_apiid`

Check if a API ID is attached to any community account

#### Request Body

| Name                                   | Type   | Description                   |
| -------------------------------------- | ------ | ----------------------------- |
| id<mark style="color:red;">\*</mark>   | string | Community ID                  |
| key<mark style="color:red;">\*</mark>  | string | API Key                       |
| type<mark style="color:red;">\*</mark> | string | CHECK\_CO&#x4D;_\__&#x41;PIID |
| data<mark style="color:red;">\*</mark> | array  | Array of request objects      |

{% tabs %}
{% tab title="200: OK " %}
```javascript
{{Sonoran CMS Account Username}}
```
{% endtab %}

{% tab title="400: Bad Request The following 400 errors may be sent in response:" %}
```javascript
INVALID API KEY
INVALID COMMUNITY ID
API ID NOT LINKED TO AN ACCOUNT IN THIS COMMUNITY
```
{% endtab %}
{% endtabs %}

```
{
    "id": "YOUR_COMMUNITY_ID",
    "key": "YOUR_API_KEY",
    "type": "CHECK_COM_APIID",
    "data": [
        {
            "apiId": "SOME_API_ID"
        }
    ]
}
```

