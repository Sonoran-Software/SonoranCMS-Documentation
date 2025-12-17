---
description: An in-game way to utilize Sonoran CMS's clock in/out system.
---

# Clock In

This module is a in-game way of automatically\* clocking in/out of Sonoran CMS's system.

## Installation / Configuration

{% hint style="info" %}
With core version `v1.4.0` the Clock In resource was converted to a core module and no longer requires manual installation just configuration.
{% endhint %}

### 1. Configure Clock In Module

Locate the clockin module within your `[sonorancms]/sonorancms/server/modules` and open the `clockin_config.json` file

```json
{
    "enableCommand": true,
    "command": "clockin",
    "useAcePermissions": false,
    "qbcore": {
        "use": true,
        "autoClockInJobs": [
            "police",
            "ems",
            "fire"
        ]
    },
    "esx": {
        "use": false,
        "autoClockInJobs": [
            "police",
            "ambulance"
        ]
    },
    "cad": {
        "use": false,
        "note": "This will automatically clock in users when they enter a Police/EMS/Fire CAD panel. This will not correlate to the users actual in-game status, but will allow them to use the CAD without having to manually clock in."
    },
    "ranksWhileCadActive": [
        "00000000-0000-0000-0000-000000000000"
    ]
}
```

## Configuration

| Config Option          | Description                                                                                                                                                                                                                                                                                                                                           |
| ---------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| enableCommand          | Registers the specified `command` that allows you to toggle clock in/out.                                                                                                                                                                                                                                                                             |
| command                | If `enableCommand` is `true`, this will be the registered command to toggle clock in/out.                                                                                                                                                                                                                                                             |
| useAcePermissions      | If `enableCommand` is `true`, this will enable ace permissions for the specific command, must give `command.whateverTheCommandIs`                                                                                                                                                                                                                     |
| qbcore.use             | Enables qbcore integration                                                                                                                                                                                                                                                                                                                            |
| qbcore.autoClockInJobs | Will automatically clock in/out the player's Sonoran CMS account with they clock in/out of a job with the name in the array of `autoClockInJobs`                                                                                                                                                                                                      |
| esx.use                | Enables ESX integration                                                                                                                                                                                                                                                                                                                               |
| esx.autoClockInJobs    | Will automatically clock in/out the player's Sonoran CMS account with they clock in/out of a job with the name in the array of `autoClockInJobs`                                                                                                                                                                                                      |
| cad                    | When enabled, it will automatically clock the user in and out when logging into and out of Sonoran CAD.                                                                                                                                                                                                                                               |
| ranksWhileCadActive    | <p>A list of <a href="../../../../tutorials/user-management/creating-departments.md#copy-rank-ids">CMS rank IDs</a> that will be added when the user logs into Sonoran CAD and removes it when logging out of Sonoran CAD.<br>This is used for restricting access to things like Sonoran Radio to only be available to users actively in the CAD.</p> |

### 2. Add your API ID

Ensure all players have added their [API ID](../../../../developer-api-documentation/api-integration/getting-started/api-id-system.md) to the CMS!
