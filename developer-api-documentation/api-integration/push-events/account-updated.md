---
description: This push event sends data when an account gets updated.
---

# Account Updated

### ACCOUNT\_UPDATED POST

```javascript
{
    "key": "YOUR_API_KEY", // Authenticate legitimate event traffic
    "type": "ACCOUNT_UPDATED",
    "data": {
        "discordId": "235947056630333440",
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
        ]
    }
}
```
