---
description: This endpoint allows you to get a community columns and rows with pagination.
---

# Get Roster Contents

## Get Roster Contents

<mark style="color:green;">`POST`</mark> `https://api.sonorancms.com/rosters/get`

Get a Sonoran CMS community roster contents by ID & pagination.

#### Request Body

| Name                                   | Type   | Description           |
| -------------------------------------- | ------ | --------------------- |
| id<mark style="color:red;">\*</mark>   | string | Community ID          |
| key<mark style="color:red;">\*</mark>  | string | API Key               |
| type<mark style="color:red;">\*</mark> | string | GET\_ROSTER\_CONTENTS |
| data<mark style="color:red;">\*</mark> | array  | Object                |

{% tabs %}
{% tab title="200: OK " %}
```json
{
  "rows": [
    {
      "uuid": "d5663516-ee35-11e9-9714-5600023b2434",
      "entryId": 1,
      "sortPower": 0,
      "type": 0,
      "overrideColumns": [],
      "1a76a820-c97f-4756-8254-0f2514f748a4": "235947056630333440",
      "f4cf4bf7-b4f8-41e9-8b60-7f5513b07e46": "Test Account Name",
      "2809b5c5-84c1-412b-bfde-ac70bf9ed8d4": {
        "label": "Community Lead",
        "id": "e88236cb-2af0-4d68-b5f5-aa2058ba8427"
      },
      "57fd7d49-c2b4-4afa-89b0-a6136d9679a9": {
        "label": "456",
        "value": "4a761370-b78e-4639-8891-741bdda19b8b"
      },
      "5bc02f25-3376-4897-b1c4-200d2559095a": {
        "uuid": "4ed5bc6d-e139-4336-9390-6f2851f623ab",
        "color": "#119913",
        "label": "Active"
      },
      "e354b1b4-4c50-474c-bf3f-7f293ed5a825": "22/05/24",
      "6fb54c8f-6a00-4f3e-94e4-3b3baf021649": "0:00"
    }
  ],
  "total": 1,
  "skip": 0,
  "limit": 10,
  "columns": [
    {
      "type": "Community ID",
      "align": "left",
      "field": "1a76a820-c97f-4756-8254-0f2514f748a4",
      "label": "Member ID",
      "style": {
        "cosmetic": {
          "font": null,
          "align": "center",
          "color": "#313131",
          "textColor": null
        },
        "formattedStyles": []
      },
      "options": [],
      "cosmetic": {
        "font": null,
        "align": "center",
        "color": "#313131",
        "textColor": null
      },
      "metadata": {
        "modHidden": false,
        "rankBased": [],
        "adminHidden": false
      },
      "reverseMask": false
    }
    ...,
  ]
}
```
{% endtab %}

{% tab title="400: Bad Request The following 400 errors may be sent in response:" %}
```javascript
INVALID API KEY
INVALID COMMUNITY ID
ROSTER NOT FOUND
```
{% endtab %}
{% endtabs %}

```json
{
    "id": "YOUR_COMMUNITY_ID",
    "key": "YOUR_API_KEY",
    "type": "GET_ROSTER_CONTENTS",
    "data": {
        "rosterId": NUMBER_ID,
        "skip": NUMBER_OF_ROWS_TO_SKIP,
        "limit": NUMBER_OF_ROWS_TO_FETCH, // Max. Limit 50
    }
}
```
