---
description: >-
  This endpoint allows you to get a community account by account ID, API ID, or
  username.
---

# Get Com Account

{% swagger method="post" path="/general/get_com_account" baseUrl="https://api.sonorancms.com" summary="Get Com Account" %}
{% swagger-description %}
Get a Sonoran CMS community account by account ID, API ID, or username.
{% endswagger-description %}

{% swagger-parameter in="body" name="id" type="string" required="true" %}
Community ID
{% endswagger-parameter %}

{% swagger-parameter in="body" name="key" type="string" required="true" %}
API Key
{% endswagger-parameter %}

{% swagger-parameter in="body" required="true" name="type" type="string" %}
GET\_COM\_ACCOUNT
{% endswagger-parameter %}

{% swagger-parameter in="body" required="true" name="data" type="array" %}
Array of request objects
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```javascript
{
    "accId": "67ceebae-ee63-43c1-a6a6-5234b2210abf",
    "comStatus": true,
    "accName": "Dawson G.",
    "comName": "Dawson G.",
    "primaryIdentifier": "1A-1",
    "secondaryIdentifiers": [],
    "primaryRank": "fc2c3825-df41-4485-ad9a-6c2ac900b4f4",
    "secondaryRanks": [
        "331d4ece-b582-4c9c-885b-7060341cf482"
    ],
    "primaryDepartment": "00116ef0-9d22-491e-964c-1eb1b6ffd167",
    "secondaryDepartments": [
        "7dbedb0e-4df2-4405-b241-cb5dee253ab8"
    ],
    "joinDate": "2022-02-22 20:28:40.000 -0800",
    "owner": true,
    "banned": false,
    "lastLogin": "2022-02-22 22:43:46.000 -0800",
    "activeApiIds": [
        "235947056630333440"
    ],
    "profileFields": {
        "data": [
            {
                "id": "d9d1288e-3892-40d6-acc5-be2c3d294bd4",
                "value": ["some", "strings", "for", "array"]
            },
            ...
        ]
    }
}
```
{% endswagger-response %}

{% swagger-response status="400: Bad Request" description="The following 400 errors may be sent in response:" %}
```javascript
INVALID API KEY
INVALID COMMUNITY ID
API ID NOT LINKED TO AN ACCOUNT IN THIS COMMUNITY
NO ACCOUNT FOUND UNDER GIVEN PARAMETERS IN THIS COMMUNITY
```
{% endswagger-response %}
{% endswagger %}

```
{
    "id": "YOUR_COMMUNITY_ID",
    "key": "YOUR_API_KEY",
    "type": "GET_COM_ACCOUNT",
    "data": [
        {
            "apiId": "SOME_API_ID", // Optional - must have one
            "username": "SOMEUSERNAME", // Optional - must have one
            "accId": "SOMEACCID", // Optional - must have one
            "discord": "111122223333444455", // Optional - must have one
            "uniqueId": 1234 // Optional - must have one
        }
    ]
}
```
