---
description: This endpoint allows you to check your Sonoran CMS subscription version.
---

# Get Sub Version

{% hint style="warning" %}
API endpoint requires the **FREE** version of Sonoran CMS or higher.\
For more information, see our [pricing ](../../../../pricing/pricing-faq/)page.
{% endhint %}

## Get Sub Version

<mark style="color:green;">`POST`</mark> `https://api.sonorancms.com/general/get_sub_version`

Get Sonoran CMS subscription version of a community.

#### Request Body

| Name                                   | Type   | Description                   |
| -------------------------------------- | ------ | ----------------------------- |
| id<mark style="color:red;">\*</mark>   | string | Community ID                  |
| key<mark style="color:red;">\*</mark>  | string | API Key                       |
| type<mark style="color:red;">\*</mark> | string | GET\_SU&#x42;_\__&#x56;ERSION |
| data<mark style="color:red;">\*</mark> | array  | Array of request objects      |

{% tabs %}
{% tab title="200: OK " %}
```javascript
0 - FREE
1 - STARTER
2 - STANDARD
3 - PLUS
4 - PRO
5 - SONORANONE
```
{% endtab %}

{% tab title="400: Bad Request The following 400 errors may be sent in response:" %}
```javascript
INVALID API KEY
INVALID COMMUNITY ID
```
{% endtab %}
{% endtabs %}

```
{
    "id": "YOUR_COMMUNITY_ID",
    "key": "YOUR_API_KEY",
    "type": "GET_SUB_VERSION",
    "data": []
}
```
