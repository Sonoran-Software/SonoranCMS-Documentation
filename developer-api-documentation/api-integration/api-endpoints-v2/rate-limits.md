---
description: Rate limits for the v2 API.
---

# V2 Rate Limits

The documented ceilings below are intentionally a little lower than the live gateway limits so normal integration bursts still have a safety buffer.

All limits are enforced per credential.

## General

| Endpoint | Safe Limit |
| --- | --- |
| [Get Community](general/get-community.md) | `13 requests/min` |
| [Get Sub Version](general/get-sub-version.md) | `13 requests/min` |
| [Lookup Community](general/lookup-community.md) | `13 requests/min` |
| [Get Departments](general/get-departments.md) | `13 requests/min` |
| [Get Profile Fields](general/get-profile-fields.md) | `13 requests/min` |
| [Get Clock In Types](general/get-clockin-types.md) | `13 requests/min` |
| [Get Custom Log Types](general/get-custom-log-types.md) | `13 requests/min` |
| [Get Promotion Flows](general/get-promotion-flows.md) | `13 requests/min` |
| [Trigger Promotion Flows](general/trigger-promotion-flows.md) | `13 requests/min` |
| [Undo Rank Change](general/undo-rank-change.md) | `13 requests/min` |
| [Create Short URL](general/create-short-url.md) | `13 requests/min` |

## Accounts

| Endpoint | Safe Limit |
| --- | --- |
| [Get Accounts](accounts/get-accounts.md) | `22 requests/min` |
| [Search Accounts](accounts/search-accounts.md) | `27 requests/min` |
| [Get Account](accounts/get-account.md) | `27 requests/min` |
| [Get Account Ranks](accounts/get-account-ranks.md) | `27 requests/min` |
| [Get Account Identifiers](accounts/get-account-identifiers.md) | `22 requests/min` |
| [Register Identifiers](accounts/register-identifiers.md) | `22 requests/min` |
| [Set Account Name](accounts/set-account-name.md) | `22 requests/min` |
| [Set Account Ranks](accounts/set-account-ranks.md) | `22 requests/min` |
| [Edit Profile Fields](accounts/edit-profile-fields.md) | `22 requests/min` |
| [Clock Account](accounts/clock-account.md) | `22 requests/min` |
| [Get Current Clock In](accounts/get-current-clock-in.md) | `27 requests/min` |
| [Get Latest Activity](accounts/get-latest-activity.md) | `27 requests/min` |
| [Force Sync](accounts/force-sync.md) | `27 requests/min` |

## Servers

| Endpoint | Safe Limit |
| --- | --- |
| [Get Servers](servers/get-servers.md) | `13 requests/min` |
| [Set Servers](servers/set-servers.md) | `9 requests/min` |
| [Add Servers](servers/add-servers.md) | `9 requests/min` |
| [Get ACE Config](servers/get-ace-config.md) | `27 requests/min` |
| [Set ACE Config](servers/set-ace-config.md) | `18 requests/min` |
| [Set Server Type](servers/set-server-type.md) | `18 requests/min` |
| [Verify Whitelist](servers/verify-whitelist.md) | `27 requests/min` |
| [Full Whitelist](servers/full-whitelist.md) | `13 requests/min` |
| [Activity Tracker](servers/activity-tracker.md) | `27 requests/min` |
| [Activity Tracker Server Start](servers/activity-tracker-server-start.md) | `27 requests/min` |

## Events

| Endpoint | Safe Limit |
| --- | --- |
| [RSVP](events/rsvp.md) | `27 requests/min` |

## Forms

| Endpoint | Safe Limit |
| --- | --- |
| [Change Form Stage](forms/change-stage.md) | `27 requests/min` |
| [Get Template Submissions](forms/get-template-submissions.md) | `13 requests/min` |
| [Get Form Lock Status](forms/get-lock-status.md) | `27 requests/min` |
| [Set Form Lock Status](forms/set-lock-status.md) | `18 requests/min` |
| [Get Submission](forms/get-submission.md) | `27 requests/min` |

## Rosters

| Endpoint | Safe Limit |
| --- | --- |
| [Get Roster Contents](rosters/get-roster-contents.md) | `9 requests/min` |

## Disciplinary

| Endpoint | Safe Limit |
| --- | --- |
| [Get Member Points](disciplinary/get-member-points.md) | `27 requests/min` |
| [Get Member Records](disciplinary/get-member-records.md) | `27 requests/min` |
| [Add Member Record](disciplinary/add-member-record.md) | `18 requests/min` |
| [Update Member Record Points](disciplinary/update-member-record-points.md) | `18 requests/min` |
| [Update Member Record Reason](disciplinary/update-member-record-reason.md) | `18 requests/min` |
| [Update Member Record Status](disciplinary/update-member-record-status.md) | `18 requests/min` |

## ERLC

| Endpoint | Safe Limit |
| --- | --- |
| [Get Online Players](erlc/get-online-players.md) | `27 requests/min` |
| [Get Player Queue](erlc/get-player-queue.md) | `27 requests/min` |
| [Add ERLC Record](erlc/add-record.md) | `18 requests/min` |
| [Execute Command](erlc/execute-command.md) | `18 requests/min` |
| [Lock Team](erlc/lock-team.md) | `18 requests/min` |
| [Unlock Team](erlc/unlock-team.md) | `18 requests/min` |

## Sessions

| Endpoint | Safe Limit |
| --- | --- |
| [Get Current Session](sessions/get-current-session.md) | `27 requests/min` |
| [Start Session](sessions/start-session.md) | `27 requests/min` |
| [Stop Session](sessions/stop-session.md) | `27 requests/min` |
| [Cancel Session](sessions/cancel-session.md) | `9 requests/min` |
