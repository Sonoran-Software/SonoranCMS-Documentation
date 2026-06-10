# Error Codes

## Error and Warning Codes

SonoranCMS FiveM uses structured `ERR-XX-###` and `WRN-XX-###` codes that point back to this document.

You can link directly to any code by appending it to the support URL. Example: `sonorancms.com/error/WRN-CORE-101`

Warnings use a `WRN-*` prefix. Errors use an `ERR-*` prefix.

### Core Errors

#### ERR-CORE-101

**Key:** `API_ERROR`

**What it means:** SonoranCMS could not retrieve the CMS API version during startup.

**How to fix it:** Verify the API URL, community ID, API key, and outbound connectivity, then restart the resource.

#### ERR-CORE-102

**Key:** `CONFIG_NEW_FOUND`

**What it means:** `config.NEW.lua` was found, which indicates the live config is outdated and needs manual review.

**How to fix it:** Merge the new config values into `config.lua`, then remove `config.NEW.lua`.

#### ERR-CORE-103

**Key:** `API_ENDPOINT_INVALID`

**What it means:** The configured CMS API endpoint resolved to an invalid backend path.

**How to fix it:** Check `Config.apiUrl`, registered endpoint mappings, and any custom API override values.

#### ERR-CORE-104

**Key:** `API_DISABLED_FATAL`

**What it means:** SonoranCMS disabled outbound API usage after a fatal configuration or authentication response.

**How to fix it:** Fix the reported invalid API key, community ID, or entitlement issue, then restart the resource.

#### ERR-CORE-105

**Key:** `API_SERVER_ERROR`

**What it means:** The CMS API returned a server-side error.

**How to fix it:** Check `status.sonoransoftware.com` and retry once the backend is healthy.

#### ERR-CORE-106

**Key:** `API_REQUEST_UNEXPECTED`

**What it means:** The CMS API returned an unexpected status or response body.

**How to fix it:** Enable debug logging, inspect the related request and response pair, and verify the endpoint and payload are valid.

#### ERR-CORE-107

**Key:** `API_REQUEST_BLOCKED`

**What it means:** SonoranCMS refused to send an API request because the resource is already in a critical error state.

**How to fix it:** Resolve the earlier fatal startup error first, then restart the resource.

#### ERR-CORE-108

**Key:** `PLAYER_IDENTIFIER_MISSING`

**What it means:** A helper attempted to read a player identifier that was not present on the player.

**How to fix it:** Confirm the configured identifier type exists for the player and that the framework or resource is passing the correct identifier type.

### Security Center Errors

#### ERR-SEC-101

**Key:** `SECURITY_CENTER_POST_FAILED`

**What it means:** Posting a Security Center event to SonoranCMS failed.

**How to fix it:** Verify the outbound API connection and inspect the backend response message included in the log.

### Activity Tracker Errors

#### ERR-AT-101

**Key:** `ACTIVITY_TRACKER_START_FAILED`

**What it means:** SonoranCMS could not create an activity tracker entry for a player join or start event.

**How to fix it:** Verify the outgoing payload and the API response for the affected player identifier.

#### ERR-AT-102

**Key:** `ACTIVITY_TRACKER_STOP_FAILED`

**What it means:** SonoranCMS could not stop an activity tracker entry for a player disconnect or stop event.

**How to fix it:** Check the API response payload and make sure the player identifier being sent is valid.

#### ERR-AT-103

**Key:** `ACTIVITY_TRACKER_RESET_FAILED`

**What it means:** SonoranCMS could not clear active activity tracker entries during startup recovery.

**How to fix it:** Check the API response details and verify the activity tracker endpoint is available.

### ACE Permission Errors

#### ERR-ACE-102

**Key:** `ACE_PERMISSIONS_FETCH_FAILED`

**What it means:** Fetching ACE permission data from SonoranCMS failed.

**How to fix it:** Verify the API key, community ID, and connectivity to the CMS API.

### JobSync Errors

#### ERR-JS-101

**Key:** `JOBSYNC_SET_RANKS_FAILED`

**What it means:** JobSync could not update account ranks in SonoranCMS.

**How to fix it:** Verify the player identifier, inspect the API response in the log, and confirm the configured rank mappings are valid.

#### ERR-JS-102

**Key:** `JOBSYNC_CONFIG_MISSING`

**What it means:** The JobSync configuration file could not be loaded.

**How to fix it:** Ensure `server/modules/jobsync/jobsync_config.json` exists and contains valid JSON.

### ClockIn Errors

#### ERR-CLK-101

**Key:** `CLOCKIN_PERMISSION_DENIED`

**What it means:** A player attempted to use ClockIn without the required permissions.

**How to fix it:** Verify the command permission model and the player's allowed access before retrying.

#### ERR-CLK-102

**Key:** `CLOCKIN_REQUEST_FAILED`

**What it means:** A ClockIn request failed while handling a player command.

**How to fix it:** Check the backend response text included in the log and verify the account can clock in or out through SonoranCMS.

#### ERR-CLK-103

**Key:** `CLOCKIN_EVENT_FAILED`

**What it means:** A server-side ClockIn event failed while processing a player state change.

**How to fix it:** Verify the player identifier and the current clock-in state being sent to the API.

#### ERR-CLK-104

**Key:** `CLOCKIN_CAD_RESOURCE_BAD_STATE`

**What it means:** ClockIn attempted to use SonoranCAD integration while the `sonorancad` resource was not started cleanly.

**How to fix it:** Start or repair the `sonorancad` resource, or disable the CAD integration in the ClockIn config.

#### ERR-CLK-105

**Key:** `CLOCKIN_CONFIG_MISSING`

**What it means:** ClockIn could not load its configuration from file or convars.

**How to fix it:** Ensure `server/modules/clockin/clockin_config.json` exists and that the expected convars are set.

### Whitelist Errors

#### ERR-WL-101

**Key:** `WHITELIST_ACTIVE_PLAYER_CACHE_FAILED`

**What it means:** Whitelist failed to cache an active player entry.

**How to fix it:** Inspect the related account lookup call and verify the response returned a usable account ID.

#### ERR-WL-102

**Key:** `WHITELIST_IDENTIFIER_MISSING`

**What it means:** Whitelist could not find the configured API identifier type for a player.

**How to fix it:** Confirm the configured identifier type matches the identifiers actually present on connecting players.

### Game Panel Errors

#### ERR-GP-201

**Key:** `GAME_PANEL_GARAGE_EXPORT_MISSING`

**What it means:** A supported garage integration resource is missing the export SonoranCMS expects.

**How to fix it:** Update the affected garage resource to a compatible version or switch to a supported garage integration.

### Plugin and Legacy Addon Errors

#### ERR-PLUG-101

**Key:** `LEGACY_RESOURCE_STOP_FAILED`

**What it means:** SonoranCMS detected an old standalone addon resource and could not stop it automatically.

**How to fix it:** Remove the old standalone resource from your startup config and filesystem so only the bundled module remains.

### Update Errors

#### ERR-UPD-101

**Key:** `UPDATE_DOWNLOAD_FAILED`

**What it means:** SonoranCMS downloaded an update flow result that failed during unzip or helper processing.

**How to fix it:** Inspect the bundled error payload in the log, verify filesystem permissions, and retry the update.

### Core Warnings

#### WRN-CORE-101

**Key:** `CMS_SERVERS_FETCH_FAILED`

**What it means:** SonoranCMS could not fetch the existing CMS server list.

**How to fix it:** Verify API connectivity and inspect the logged response for the failing request.

#### WRN-CORE-102

**Key:** `CMS_SERVERS_PARSE_FAILED`

**What it means:** The response to `GET_GAME_SERVERS` could not be parsed as expected.

**How to fix it:** Enable debug logging and inspect the raw response body for malformed JSON or an upstream HTML or error payload.

#### WRN-CORE-103

**Key:** `CMS_SERVERS_RESPONSE_INVALID`

**What it means:** The `GET_GAME_SERVERS` response was valid JSON but did not contain the expected `servers` table.

**How to fix it:** Verify the backend endpoint is the expected one and inspect the raw response payload.

#### WRN-CORE-104

**Key:** `CMS_SERVER_PORT_DEFAULTED`

**What it means:** SonoranCMS could not detect the server port and fell back to `30120` during registration.

**How to fix it:** Set `endpoint_add_tcp`, `endpoint_add_udp`, `sv_port`, or `netPort` correctly so the real port can be detected.

#### WRN-CORE-105

**Key:** `CMS_SERVER_REGISTER_FAILED`

**What it means:** SonoranCMS could not create the configured CMS server entry.

**How to fix it:** Verify `serverId`, server metadata, and the backend response for the failed add request.

#### WRN-CORE-106

**Key:** `LEGACY_ADDONUPDATES_PERMISSION`

**What it means:** The deprecated `addonupdates` folder may exist, but SonoranCMS could not verify it because of a permission error.

**How to fix it:** Review the resource directory permissions and remove the legacy folder if it is no longer needed.

#### WRN-CORE-107

**Key:** `CONFIG_NEW_PERMISSION`

**What it means:** `config.NEW.lua` may exist, but a permission error prevented SonoranCMS from checking it.

**How to fix it:** Verify resource filesystem permissions and then rerun startup checks.

#### WRN-CORE-108

**Key:** `FXSERVER_OUTDATED`

**What it means:** The running FXServer build is older than the version SonoranCMS was tested against.

**How to fix it:** Update FXServer to at least the tested build shown in the log.

#### WRN-CORE-109

**Key:** `API_ENDPOINT_UNREGISTERED`

**What it means:** Code attempted to send an API request for an endpoint type that was never registered.

**How to fix it:** Register the endpoint type before calling `performApiRequest`, or correct the endpoint name.

#### WRN-CORE-110

**Key:** `API_BAD_REQUEST`

**What it means:** The CMS API rejected a request as invalid or malformed.

**How to fix it:** Enable debug logging and inspect the payload or body being sent to the API.

#### WRN-CORE-111

**Key:** `API_RATELIMITED`

**What it means:** The CMS API temporarily rate-limited one of the endpoints.

**How to fix it:** Reduce request frequency for the affected endpoint and check for duplicate or looping requests.

### Game Panel Warnings

#### WRN-GP-101

**Key:** `GAME_PANEL_INVENTORY_DEPENDENCY_MISSING`

**What it means:** Game Panel inventory data cannot be sent because no supported inventory resource is running.

**How to fix it:** Start a supported inventory resource or ignore this warning if the Game Panel feature is not used.

#### WRN-GP-102

**Key:** `GAME_PANEL_GARAGE_DEPENDENCY_MISSING`

**What it means:** Game Panel garage data will be empty because no supported garage resource is running.

**How to fix it:** Start a supported garage resource or ignore this warning if garage sync is not needed.

#### WRN-GP-103

**Key:** `GAME_PANEL_DATABASE_DEPENDENCY_MISSING`

**What it means:** Game Panel payloads cannot be built because no supported database resource is running.

**How to fix it:** Start `oxmysql`, `mysql-async`, or `ghmattimysql`, or ignore this warning if the Game Panel feature is not used.

#### WRN-GP-104

**Key:** `GAME_PANEL_PAYLOAD_BLOCKED`

**What it means:** Game Panel payload delivery was skipped because SonoranCMS is in a critical error state.

**How to fix it:** Resolve the earlier blocking error first, then restart the resource.

#### WRN-GP-105

**Key:** `GAME_PANEL_PAYLOAD_BLOCKED_DETAILS`

**What it means:** Additional details were logged for a skipped Game Panel payload.

**How to fix it:** Read the accompanying error list in the same log block and fix the first listed problem.

#### WRN-GP-106

**Key:** `RESOURCE_NAME_INVALID`

**What it means:** The resource is not named `sonorancms`, which breaks assumptions used by the integration.

**How to fix it:** Rename the resource folder or startup entry to `sonorancms`.

#### WRN-GP-107

**Key:** `LEGACY_RESOURCE_RUNNING`

**What it means:** A legacy standalone SonoranCMS addon is still running even though that functionality is now bundled into core.

**How to fix it:** Remove the old addon resource from startup and leave only the bundled SonoranCMS core resource enabled.

### ACE Permission Warnings

#### WRN-ACE-101

**Key:** `ACE_IDENTIFIER_MISSING`

**What it means:** A player was denied ACE-based sync because the configured identifier type was missing.

**How to fix it:** Confirm players have the configured identifier type and that `Config.apiIdType` matches it.

### JobSync Warnings

#### WRN-JS-101

**Key:** `JOBSYNC_IDENTIFIER_MISSING`

**What it means:** JobSync could not update ranks because the player did not have the configured identifier.

**How to fix it:** Confirm the identifier type configured for SonoranCMS is present on the affected players.

### Update Warnings

#### WRN-UPD-101

**Key:** `UPDATE_AUTORESTARTING`

**What it means:** An automatic update completed and SonoranCMS is about to restart helper resources.

**How to fix it:** No immediate action is required unless the restart loop repeats unexpectedly.

#### WRN-UPD-102

**Key:** `UPDATE_RELEASE_DOWNLOAD_FAILED`

**What it means:** Downloading an update archive from GitHub failed.

**How to fix it:** Check outbound network access to GitHub and verify the release URL or version exists.

#### WRN-UPD-103

**Key:** `UPDATE_VERSION_RESPONSE_INVALID`

**What it means:** The version metadata fetched for updates was not valid JSON or was otherwise unusable.

**How to fix it:** Check the raw version file response and retry once GitHub raw content is reachable.

#### WRN-UPD-104

**Key:** `UPDATE_NOT_CONFIGURED`

**What it means:** Automatic updating is available but `allowAutoUpdate` has not been configured.

**How to fix it:** Set `allowAutoUpdate` explicitly in `config.lua` to either enable or intentionally disable auto-updates.

#### WRN-UPD-105

**Key:** `UPDATE_RESTART_DELAYED`

**What it means:** An update was applied, but restart is delayed until the server is empty.

**How to fix it:** Wait for the server to empty or restart manually during a maintenance window.

### ClockIn Warnings

#### WRN-CLK-101

**Key:** `CLOCKIN_UNITLOGIN_MISSING_ACCID`

**What it means:** A SonoranCAD `UnitLogin` event did not include an account ID for ClockIn.

**How to fix it:** Verify the incoming push event payload contains `accId`.

#### WRN-CLK-102

**Key:** `CLOCKIN_UNITLOGOUT_MISSING_ACCID`

**What it means:** A SonoranCAD `UnitLogout` event did not include an account ID or unit reference for ClockIn.

**How to fix it:** Verify the event payload being emitted by the CAD integration.

#### WRN-CLK-103

**Key:** `CLOCKIN_UNITLOGOUT_UNIT_MISSING`

**What it means:** ClockIn could not resolve the CAD unit record for a logout event.

**How to fix it:** Check the SonoranCAD unit cache and make sure the unit ID is still valid when the event fires.

#### WRN-CLK-104

**Key:** `CLOCKIN_CAD_CLOCK_FAILED`

**What it means:** ClockIn could not complete a CAD-driven clock in or out request.

**How to fix it:** Review the player or account state and the related API response for the failed request.

#### WRN-CLK-105

**Key:** `CLOCKIN_RANK_LOGIN_ACCID_MISSING`

**What it means:** ClockIn could not add CMS ranks on CAD login because the account ID was missing.

**How to fix it:** Verify the incoming `UnitLogin` event payload includes `accId`.

#### WRN-CLK-106

**Key:** `CLOCKIN_RANK_ADD_FAILED`

**What it means:** ClockIn could not add the configured CMS ranks after a CAD login event.

**How to fix it:** Verify the configured rank IDs and the account ID being sent to SonoranCMS.

#### WRN-CLK-107

**Key:** `CLOCKIN_RANK_LOGOUT_ACCID_MISSING`

**What it means:** ClockIn could not remove CMS ranks on CAD logout because the account ID was missing.

**How to fix it:** Verify the logout event payload contains the expected unit or account reference.

#### WRN-CLK-108

**Key:** `CLOCKIN_RANK_LOGOUT_UNIT_MISSING`

**What it means:** ClockIn could not resolve the cached CAD unit while removing CMS ranks on logout.

**How to fix it:** Inspect the SonoranCAD unit cache and confirm the unit still exists when logout fires.

#### WRN-CLK-109

**Key:** `CLOCKIN_RANK_REMOVE_FAILED`

**What it means:** ClockIn could not remove the configured CMS ranks after a CAD logout event.

**How to fix it:** Verify the configured rank IDs and the account ID being sent to SonoranCMS.

