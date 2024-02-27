# Set Account Ranks

{% swagger method="post" path="/general/set_account_ranks" baseUrl="https://api.sonorancms.com" summary="Set Account Ranks" %}
{% swagger-description %}
Get a Sonoran CMS community account's ranks by account ID, API ID, or username.
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
[
    "4298c76d-a1ee-46dc-b33c-8daf2e2280dd", // UUID of Rank
    ...
]
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
    "type": "SET_ACCOUNT_RANKS",
    "data": [
        {
            // User Identification
            "apiId": "SOME_API_ID", // Optional - must have one
            "username": "SOMEUSERNAME", // Optional - must have one
            "accId": "SOMEACCID", // Optional - must have one
            "discord": "111122223333444455", // Optional - must have one
            "uniqueId": 1234 // Optional - must have one
            // Rank Specification
            "set": ["RANK_UUID", "ANOTHER_RANK_UUID"], // Remove and set ONLY these ranks on account
            "add": ["RANK_UUID"], // Optional - Add rank(s)
            "remove": ["RANK_UUID"] // Optional - Remove rank(s)
        }
    ]
}
```

### Notes

`set` `add` and `remove` can all be used together. `remove` takes precedence over `add` (i.e. if both add and remove have the same rank, it is ultimately removed).

The rank UUID(s) can be copied from the [rank manager](../../../../tutorials/user-management/creating-departments.md) by clicking the `...` icon and selecting the `Copy Rank ID` button.
