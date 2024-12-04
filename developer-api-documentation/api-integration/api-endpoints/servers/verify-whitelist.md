---
description: This endpoint allows you to verify the whitelist of a community account.
---

# Verify Whitelist

## Verify Whitelist

<mark style="color:green;">`POST`</mark> `https://api.sonorancms.com/servers/verify_whitelist`

Verifies the whitelist of a community account found given the accId or API ID.

#### Request Body

| Name | Type   | Description                    |
| ---- | ------ | ------------------------------ |
| id   | string | Community ID                   |
| key  | string | API Key                        |
| type | string | GET\_GAM&#x45;_\__&#x53;ERVERS |
| data | array  |                                |

{% tabs %}
{% tab title="200: OK The following text responses may be sent in response:" %}
```javascript
{{Sonoran CMS Account Username}}
BYPASSED WHITELIST - {{Sonoran CMS Account Username}}
```
{% endtab %}

{% tab title="400: Bad Request The following text responses may be sent in response:" %}
```json
{
    "status": 400,
    "message": "VALID BAD REQUEST REASON"
}
```
{% endtab %}

{% tab title="404: Not Found The following text responses may be sent in response:" %}
```javascript
NOT ALLOWED ON WHITELIST
```
{% endtab %}
{% endtabs %}

```json
{
    "id": "YOUR_COMMUNITY_ID",
    "key": "YOUR_API_KEY",
    "type": "VERIFY_WHITELIST",
    "data": [
        {
            // User Identification
            "apiId": "SOME_API_ID", // Optional - must have one
            "username": "SOMEUSERNAME", // Optional - must have one
            "accId": "SOMEACCID", // Optional - must have one
            "discord": "111122223333444455", // Optional - must have one
            "uniqueId": 1234 // Optional - must have one
            // Configuration
            "serverId": 2 // Optional - will check specific server whitelist if specified
        }
    ]
}
```
