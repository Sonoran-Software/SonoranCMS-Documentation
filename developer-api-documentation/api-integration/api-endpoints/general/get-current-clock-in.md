---
description: >-
  This endpoint allows you to get the current clock in for a community account
  by account ID, API ID, Discord ID, Unique ID, or username.
---

# Get Current Clock In

## Get Current Clock In

<mark style="color:green;">`POST`</mark> `https://api.sonorancms.com/general/get_current_clock_in`

Get a Sonoran CMS community account's current clock in by account ID, API ID, Discord ID, Unique ID, or username.

#### Request Body

| Name                                   | Type   | Description        |
| -------------------------------------- | ------ | ------------------ |
| id<mark style="color:red;">\*</mark>   | string | Community ID       |
| key<mark style="color:red;">\*</mark>  | string | API Key            |
| type<mark style="color:red;">\*</mark> | string | GET\_COM\_ACCOUNT  |
| data<mark style="color:red;">\*</mark> | object | Requst Data Object |

{% tabs %}
{% tab title="201: OK " %}
```javascript
{
  "id": 1,
  "startTime": "2025-02-22 20:28:40.000 -0800",
  "endTime": null,
  "completed": false,
  "notes": [];
}
```

```
Not Clocked In
```
{% endtab %}

{% tab title="400: Bad Request The following 400 errors may be sent in response:" %}
```javascript
INVALID API KEY
INVALID COMMUNITY ID
API ID NOT LINKED TO AN ACCOUNT IN THIS COMMUNITY
NO ACCOUNT FOUND UNDER GIVEN PARAMETERS IN THIS COMMUNITY
```
{% endtab %}
{% endtabs %}

```
{
    "id": "YOUR_COMMUNITY_ID",
    "key": "YOUR_API_KEY",
    "type": "GET_CURRENT_CLOCK_IN",
    "data": {
        "apiId": "SOME_API_ID", // Optional - must have one
        "username": "SOMEUSERNAME", // Optional - must have one
        "accId": "SOMEACCID", // Optional - must have one
        "discord": "111122223333444455", // Optional - must have one
        "uniqueId": 1234 // Optional - must have one
    }
}
```
