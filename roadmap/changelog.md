---
description: View the latest changes to Sonoran CMS!
---

# 📋 Changelog

## Roadmap

[View our upcoming roadmap!](https://roadmap.sonorancms.com/)

## Changelog

### 1.1.28 05/06/2025

{% tabs %}
{% tab title="Fixed" %}
\#28514 - Pending Forms

* Fixed an issue causing "Anyone Can Submit" forms showing twice for pending users.

Mobile: Rosters Search Overlap

* Fixed an issue causing the roster search box to overlap the roster title on mobile.

Mobile: Profile Page Improvements

* General improvements to the community profile page on mobile.

Mobile: Tab Permission Updates

* Improve reconnection handling to ensure community navigation tab permissions load.

i18n: Edit Account

* Fixed a missing i18n label in the general account profile tab.

Notification Center: Centering

* Improvements to icon centering and padding in the notification center.

Integrations: Icon Spacing

* Improvements to icon spacing in the integrations portal.

Discovery Text Overflow

* Fixed a text overflow issue in the community discovery spotlight section.

Form Selection Redirect

* Fixed an issue causing form editor selections to navigate back without showing a permissions error.

Disciplinary Point Duplicate Actions

* Fixed an issue causing multiple disciplinary actions to fire at once, instead of only the threshold meeting action.
{% endtab %}
{% endtabs %}

### 1.1.27 05/01/2025

{% tabs %}
{% tab title="New" %}
Forms: Local Save Progress

* Filling out a form saves locally to resume progress if the page is exited, reloaded, or navigated away from.

Security Center: Mass-Dismiss

* Added the ability to mass-select security center flags to dismiss or reactivate.
{% endtab %}

{% tab title="Fixed" %}
HF: Page Editor SQL

* Fixed an issue causing the wrong page to load in the website page editor in rare cases.

Form Selection Cards: Gear Menu Improvements

* Fixed an issue with the form selection gear menu sometimes disappearing when clicking.

\#28318 - Website Card URLs

* Fixed an issue causing website card URLs to not properly navigate.

Fix: Private Webpages

* Fixed an issue causing webpages to all show as private.
{% endtab %}
{% endtabs %}

### 1.1.26 04/23/2025

{% tabs %}
{% tab title="New" %}
Disciplinary API

* Added API endpoints to get records, get points, add records, and modify records.

Drive: Admin Nav Bar

* When navigating to the Drive via Admin panel, the nav bar on the left will persist.
{% endtab %}

{% tab title="Fixed" %}
JS Cache Busting

* Improved JS file cache busting to resolve issues when updates are pushed.
{% endtab %}
{% endtabs %}

### 1.1.25 04/15/2025

{% tabs %}
{% tab title="New" %}
Webpage animations

* Added webpage animations for page elements.

Private Comments - UI Improvements

* Improved the UI for private form submission comments by moving the toggle directly in the input and highlighting the background as red when in private mode.

WYS Editor - Placeholder Text

* Added small placeholder text in the upgraded text editor for the form submission comments.
{% endtab %}

{% tab title="Fixed" %}
\#28030 - Form Folders & Templates

* Fixed an issue causing new form folders and templates to not appear.

Toolbar Editor - Giant Security Flag Badge

* Fixed an issue in the toolbar editor showing the user flag chip as giant.
{% endtab %}
{% endtabs %}

### 1.1.24 04/07/2025

{% tabs %}
{% tab title="New" %}
Form Comments - Private Messages

* Added new per-form permissions to send private comments on submissions.

IFrame Viewer

* Added a new iframe website viewer component.

Website Cards - Preview Image

* Added preview images to the website cards after saving the page.

Video Element - Additional Support

* Added the ability to link TikTok videos or upload your own file to the video viewer website element.

Form Unit Number Field Label Change

* Updated the form "Unit Number" field label to "Primary Identifier".
{% endtab %}

{% tab title="Fixed" %}
\#27889 Roster Search

* Fixed an issue causing the roster to refresh and show all default results when first changing the search type.

Name Format Customization

* Fixed missing i18n labels in the name format customization area.

Form Submit Permissions

* Forms set to "anyone can submit" now work for non-pending users with ranks instead of only pending users.

Growth Description Auto-Save

* Fixed an issue where updating the community description in the growth panel would not trigger an auto-save.

Member Select Drop-Downs

* Fixed an issue causing form member selector dropdowns to be empty.
{% endtab %}
{% endtabs %}

### 1.1.23 03/24/2025

{% tabs %}
{% tab title="New" %}
WYSIWYG (Quill) Editor for Form Comments + Auto-Reply

* Added a full WYS editor to form comments and the auto-reply action

Form Editor: Type Selection

* Improved the form type selection settings in the editor to be more clear

\#27655 - Get Clock Status API

* Added an API endpoint to get a user's current clock-in status
{% endtab %}

{% tab title="Fixed" %}
\#27568 - Calendar Perms

* Fixed an issue causing calendar permissions to not display in the rank manager

CMS Resource Linux Detection

* Fixed an issue causing the CMS resource to detect the platform as Linux on some versions of Windows

Time Log Popup

* Fixed an issue causing the time log modal to not properly display in rosters
{% endtab %}
{% endtabs %}

### 1.1.22 03/18/2025

{% tabs %}
{% tab title="New" %}
Qbox Panel

* Added a Qbox management panel for FiveM management

Per-Form Edit Permission

* Added per-form edit permissions in the event that a community does not want to grant the system permission to edit all forms

Discord Mapping Terms

* Updated terminology in the Discord mapping configurator, along with popup help images
{% endtab %}

{% tab title="Fixed" %}
Job Sync: Framework Safety Disable

* Added a safety to the job sync to automatically disable if framework is set to none

\#27462 Electron Window Maximize

* Fixed an issue causing an error popup when maximizing the CMS desktop application

Disciplinary Point Action Labels

* Fixed an issue causing disciplinary actions to have missing labels
{% endtab %}
{% endtabs %}

### 1.1.21 03/11/2025

{% tabs %}
{% tab title="New" %}
Form Stages - Conditional Firing

* Added conditional options to only trigger form stage actions in certain cases
{% endtab %}

{% tab title="Fixed" %}
HF: ACE Perm API Failure

* Fixed an issue causing the ACE perm configuration to be temporarily wiped on resource stop until the game panel was loaded

HF: CAD Sync

* Fixed an issue causing CAD sync to fail in certain edge cases

Garage Script Spam

* Reduced error spam when a server does not have a compatible garage script installed for the game panel

HF: Section Checkbox Conditionals

* Added a safety to ignore label fields that were marked as a required question before being changed to a label field

Form Question Variable Select

* Fixed an issue on form question variable select (for custom submission labels) where question options in the drop-down wouldn't update if changed

\#27463 Dropdown Target Select

* Fixed an issue causing the inability to select which specific form or roster a dropdown button item navigated to

Discord Mapping: Missing CMS Logo

* Fixed an issue causing the CMS logo to be missing in the Discord mapping configuration
{% endtab %}
{% endtabs %}

### 1.1.20 02/18/2025

{% tabs %}
{% tab title="New" %}
Nav Bar Dropdown Items: Drag-and-Drop Reorder

* Added the ability to drag-and-drop dropdown items in the navigation bar editor to reorder them.

Form Stage Editor Variables: Dropdown

* Improved the variables modal for form stages to include a dropdown to select the form field (instead of manually clicking and copying a field ID).

Form Board: Tree Width Expansion

* Improved the width rendering in the form submission board's tree expansion.

Backend Outage Endpoint

* Improved internal monitoring to more quickly detect unhealthy nodes in the event of a service outage.
{% endtab %}

{% tab title="Fixed" %}
\#27249 Profile Image

* Fixed an issue causing the root /account page to not display the proper account avatar.

\#27277 Discord ID Profile Field

* Fixed an issue causing the Discord ID profile field to not properly load.

Verify Token Reauth 2x WSS

* Improved reauthentication checks to help prevent an endless load on refreshes.

HF: Mobile Discord Login

* Fixed an issue causing the mobile app login with Discord to not process correctly.

Form Submit: Prior Required Field

* Fixed an issue preventing submisssions if a required field was changed to a label, thus no longer displaying the option to no longer be required.
{% endtab %}
{% endtabs %}

### 1.1.18 02/11/2025

{% tabs %}
{% tab title="New" %}
Form Viewer: Mobile Improvements

* Improved form submission board UI layout for better density with the stage add and reorder buttons.

Clockin: Live Reactivity

* Clocking in externally via API (in-game) now live updates on your CMS screen if open.

Available Forms: Live Permission Update

* Adding or removing a rank from a user will now live update/reload their available forms page if viewing it.
{% endtab %}

{% tab title="Fixed" %}
Dev Mode Banner Race Condition

* Fixed an internal display issue with the banner on the development version site

\#27105 Delete Community

* Fixed an issue causing the redirect after deleting a CMS community to cause an endless loading screen on the main menu.

i18n Fix

* Fixed a missing "Kicked Members" label in the account menu.

Mobile App Login Redirect

* Fixed an issue with the mobile app causing the SSO login screen to keep the app in-browser instead of reopening the CMS app.
{% endtab %}
{% endtabs %}

### 1.1.17 02/05/2025

{% tabs %}
{% tab title="New" %}
Form Submission Board: Tree View

* Form submission board now has expandable tree nodes for form selection, allowing for better organization with folders.

Actions: Variable Modal Component

* Form stage and disciplinary actions now use the new variable component for easier copy/paste of dynamic variables instead of visual typing in the descriptions.

Form SEO Metadata

* Improved social embeds for new forms and form submission links.

Forms: Dependency Select

* Improved the dependency selection in the form editor to have a drop-down select for applicable form types instead of always requiring a comma separated string.
{% endtab %}

{% tab title="Fixed" %}
\#26930 Roster Rank Display Order

* Fixed an issue causing rosters with specificly ordered ranks to load the ranks in reverse order.

\#26903 Share Submission Link

* Fixed an issue causing admin form submission share URLs to not automatically open the form submission.
{% endtab %}
{% endtabs %}

### 1.1.16 01/29/2025

{% tabs %}
{% tab title="New" %}
Website Element: Account Card

* Added a new website element to display a selected user with their name, avatar, highest rank, and more.

Form Submission: Title Customization

* Added new submission title customizations, complete with variables, to customize how submissions show in the submitted form board.

Form Submission Limits: Blacklisted Ranks

* Added a new blacklisted permission that can restrict a user's ability to submit specific forms regardless of other ranks.

Push Notification: Community Icon

* Added custom community icon/logo support to push notifications for desktop and mobile apps.
{% endtab %}

{% tab title="Fixed" %}
\#26780 Form Editor Element Delete

* Fixed an issue breaking the form editor when deleting the last question in a section.

Mobile & Desktop - Freeze

* Fixed an issue causing the mobile and desktop apps to freeze on new logins.
{% endtab %}
{% endtabs %}

### 1.1.15 01/21/2025

{% tabs %}
{% tab title="New" %}
URL Shortener Search Expansion

* Updated the URL shortener search bar to include words/phrases from the URLs themselves and not just the description

Disciplinary Actions: Auto-Save

* Disciplinary panel actions now auto-save

Account Filter: Fixes and Improvements

* Improved labels and refresh handling in the account search filter
{% endtab %}

{% tab title="Fixed" %}
CAD Sync Change: Mass Resync

* Fixed an issue causing the CAD permission mapping to not properly mass-resync after updating the configuration

\#26629 Discord Roster Load

* Fixed an issue causing Discord username fields in rosters to not properly load/display

\#25800 - Page Load Redirect

* Fixed an issue causing a slow loading page to redirect back if navigating to a second page while waiting for the load to finish

HF: API Get FiveM Download

* Added a new API endpoint to get the pre-configured FiveM download
{% endtab %}
{% endtabs %}

### 1.1.14 01/14/2025

{% tabs %}
{% tab title="New" %}
Drive Audio File Player

* Added an in-Drive audio file player

ACE Perm Config - CMS Backup

* The QBCore/vMenu panel now stores the ACE permission config on the CMS side, rather than the community's server. This ensures communities deploying via GIT do not have their configuration files wiped out

URL Shortener Metrics Small Fixes/Improvements

* Added automatic loading when scrolling to the bottom of the URL shortener metrics tabs
* Fixed an issue causing URL shortener metrics to not update after changing the date selection

API Critical UI Notices

* Added new critical notice banners to display at the top of a community page for critical errors (such as a Discord bot configuration)

Short URL Root Subdomain Load Optimization

* Optimized the URL shortener configuration to load the short URL table faster

goodToProcess Handling Overhaul

* Overhauled logic for how pages reload and sign the user back in for a smoother experience
{% endtab %}

{% tab title="Fixed" %}
Available Forms Icon Fixes

* Fixed small issues with form icons being aligned
* Added small horizontal padding to available form titles and descriptions

Image Component - Bad Source Handling

* Fixed an issue where uploading a corrupt image would fail to display the image and fail to allow the user to hover over, click, and update the image

HF: Form Webhooks

* Resolved minor issues causing some form submission webhooks to fail

HF: Form View

* Resolved minor issues causing some communities to see a form submission from another community

Calendar Event Notification

* Resolved an issue causing some communities to get a calendar event notification from another community

FiveM Download: Remove "Dist"

* Fixed an issue with the FiveM download where "dist" was not automatically removed from the whitelist configuration file name

Drive Unzip Folder Handling

* Fixed an issue causing Google Drive ZIP file extractions (when migrating) to place files in the wrong directory

Webpage Navigation Display Issues

* Resolved an issue causing toolbar menu options to sometimes display incorrectly on mobile vs desktop

Form Clone Element ID

* Fixed an issue where cloning a form element would not generate a different unique field ID, causing dependency selections to conflict
{% endtab %}
{% endtabs %}

### 1.1.13 01/07/2025

{% tabs %}
{% tab title="New" %}
Short URL: subpaths

* Short URLs now support subpaths (ex: url.com/one/two/three)

Form Elements: Discord ID

* Added a new automatic Discord ID field to forms

Logging Center Usability Improvements

* Hid spammed internal logs used for syncs
* Added additional logs for form status changes
* Added additional logs for short URL changes
* Updated date ranges to reflect local timezone

CAD & Radio Integration: Auto-Save only if needed

* Improved the CAD and radio integrations to only auto-save when needed

On-Join Actions: Auto-Save

* On-join actions now auto-save instead of requiring a manual save button

Roster Member Add Filter

* On manual rosters, added a type-to-filter option to the member selection drop-down
{% endtab %}

{% tab title="Fixed" %}
Security Center: Flag Pagination

* Fixed an issue causing only 20 security center flags to load at once

Roster Search Overflows Title

* Fixed an issue on mobile where the roster search bar would fall behind the roster name

Integration Panel Hyperlinks

* Fixed an issue with integration panel hyperlinks being hard to click

Form Icon Duplicate Tooltip

* Removed a duplicate tooltip on the admin form editor viewer

HF: Form Webhooks: Checkbox Emoji

* Updated the checkbox status emojis in Discord webhook to be more clear on the checked vs unchecked state

HF: Form Webhooks: Number Field

* Fixed an issue where number fields in discord webhooks for forms would display as empty

HF: Discord Stage Change User

* Fixed an issue causing the "stage changed by" user to be incorrect when a form stage was changed via Discord embed
{% endtab %}
{% endtabs %}

### 1.1.12 12/23/2024

{% tabs %}
{% tab title="New" %}
URL Shortener: Perm Breakout

* Expanded URL shortener permissions to separate view, add, edit, remove, and manage domains

URL Shortener Subdomain Root Path

* Added support for short URLs to the root subdomain (ex: subdomain.example.com -> some url)

URL Shortener Metrics

* Added URL shortener metrics in the community growth panel

Drive: Upload Images

* Added image upload support in the Drive complete with thumbnails and a previewer

CAD Login Add/Remove Ranks

* Added a new `ranksWhileCadActive` config option to automatically add and remove ranks (for things like radio access) based on being in the CAD or not
{% endtab %}

{% tab title="Fixed" %}
Drive: Only Show Assets Folder in Root

* Fixed an issue causing the community assets folder to sometimes also appear in sub-folders

Form Icon/Image Fixes

* Fixed an issue causing form icons to display tiny in the available forms section
* Added icon support inside of the form editor instead of only image uploads

HF: Ranks Add Auto-Active Status

* Fixed an issue causing automated rank changes to not update a user's account status from pending to active

Form Name Confirmation

* Fixed an issue causing the form name to display incorrectly in the delete confirmation popup

Discord Webhook: Length Failure

* Fixed an issue with general discord webhooks (not from custom actions) where fields were not being trimmed to size resulting in a failed embed

HF: Short URL Path Conflicts

* Fixed an issue causing short URL paths on a subdomain to conflict with the main domain

External Nav Links Duplicate Tabs

* Fixed an issue where external navigation links would open in two new tabs instead of one if popups were enabled

Roster Discord Guild Selector

* Fixed an issue in the roster editor causing the Discord guild selector to not display
{% endtab %}
{% endtabs %}

### 1.1.11 12/11/2024

{% tabs %}
{% tab title="New" %}
Rosters - Username Search

* Added a new search bar in rosters to find a specific user by username, UID, Discord, or TS3 ID.

Status Action: Remove Pending and Active

* Updated the community status action item to only contain kick, ban, and archive as pending and active are automated based on whether the user has one or more ranks.

URL Shortener: Path Subtext

* Added full path subtext while creating a new short URL for better context.

CAD Integration: UI Improvements

* Improved horizontal scrolling in the CAD permission mapping integration window.
{% endtab %}

{% tab title="Fixed" %}
HF: Guild Selection

* Fixed an issue causing the form stage execute webhook to not display all linked Discord Guilds

HF: CAD Sync

* Fixed an issue causing new Sonoran CAD permission sync mappings to fail

Nav Bar

* Fixed an issue causing new drop-down items to not appear until after a refresh

Page Editor

* Fixed an issue with the settings cog where the page options hint would not hide, partially covering the homepage button
* Fixed an issue with an error improperly displaying after setting a new homepage
* Fixed an issue with new sections containing a blank element that couldn't be edited

Drive: List Images

* Fixed an issue causing drive images to not display when in list mode

HF: #25966 - Archived Users

* Fixed an issue causing archived users to not show up

HF: URL Shortener Redirect

* Fixed an issue where adding a subdomain based URL on a protected path - would cause the protected path to also go to the shortened URL

\#25944 - Form Limits

* Fixed an issue with new form submissions being blocked when the limits were set to ignore

\#25799 - Discovery Save

* Fixed issues with the Growth tab's Discovery settings not properly auto-saving

Footer Version

* Fixed an issue with the footer version displaying as undefined

Missing i18n Key

* Fixed an issue with a missing i18n key on the user accounts unban button
{% endtab %}
{% endtabs %}

### 1.1.9 11/27/2024

{% tabs %}
{% tab title="New" %}
URL Shortener: UI and Functionality Improvements

* Greatly improved the URL Shortener UI for more simplicity
* Updated functionality so that all Short URLs are unque to the specific subdomain

CAD Integration: UI Update

* Updated the CAD integration UI to match the newer style that the Radio integration has
{% endtab %}

{% tab title="Fixed" %}
\#25553 - Roster Rank Alignment

* Fixed an issue causing cell alignment to not apply to roster rank columns

\#25837: Short URL Save

* Fixed an issue causing new short URLs to sometimes not generate/save

Calendar Notification

* Added additional logging in the event of a calendar event notification from a different community getting fired

HF: Stage Webhook

* Fixed an issue causing some Discord stage webhooks to not be sent if certain properties were null.

HF: #25753 - Push Notifications

* Fixed an issue with template strings not properly being formatted in mobile push notifications
{% endtab %}
{% endtabs %}

### 1.1.8 11/18/2024

{% tabs %}
{% tab title="New" %}
QB Job Sync - CMS Permissions

* Overhauled the QB job sync functionality to automatically add or remove CMS ranks based on their in-game job. Ex: Only allow CAD/Radio access while in-game in an LEO job

Auto Clock-in/out Via CAD

* Added an auto clockin/out feature based on Sonoran CAD, for non QB/ESX severs

Kicked/Banned UID Changes

* Added the ability to customize a user's UID even if they're kicked or banned

Website Element Copy/Paste

* Added the ability to right-click and copy/paste website elements

Profile Activity Time - Add/Edit/Remove

* Added the ability to open a user's profile activity time block to view, add, edit, and remove time logs

API - Roster Endpoint

* Added an API endpoint to get roster data
{% endtab %}

{% tab title="Fixed" %}
\#25397 - Custom Domain Login Join Community

* Fixed an issue causing custom domain logins to display the join community banner, even though the user was auto-joined

Custom Domain Join - Link Discord Banner

* Fixed an issue causing users newly joining a community via custom domain login to not have the Discord link banner displayed until after a refresh

\#256623 - QB Nav Item

* Fixed a permissions issue causing a custom toolbar link to the QB game panel to not display

Core Download - Hash Check

* Added additional checks to the FiveM core download to ensure all files are present

Stage Actions - Status Breaks Rank Add

* Fixed an issue where setting a user's status in a custom form stage action while also setting ranks would cause the ranks to be wiped

i18n Update - Kick Sync

* Updated the Discord kick sync description in the settings panel to better reflect the functionality
{% endtab %}
{% endtabs %}

### 1.1.7 10/31/2024

{% tabs %}
{% tab title="New" %}
Short URLs - Subdomain

* Initial overhaul of the short URL system with the additional support of custom subdomain redirects. Ex: forms.community.com -> community.com/forms/new/123

Profile Field - Activity Time

* Added a new profile field type to show server activity time

Homepage - Radio Promo

* Added a new homepage promo to highlight the CMS x Radio permissions management
{% endtab %}

{% tab title="Fixed" %}
\#25234 - TeamSpeak Resync

* Adjusted TS3 sync handling in the event that a community changes their TS3 server IP address.
* Added additional handling to re-sync TS3 permissions in the user's manual re-sync tab in their community settings.

Roster N/A Rows

* Fixed an issue causing roster name and community ID rows to display as N/A when editing
{% endtab %}
{% endtabs %}

### 1.1.6 10/16/2024

{% tabs %}
{% tab title="New" %}
On-Join Actions

* Added customizable on-join actions to modify a user's ranks, send an email, send a Discord DM/webhook, and more

Live Reactivity

* Added live updates for user permissions, toolbar items, webpage content, and account status

Website Section Copy

* Added the ability to copy and paste a website page section via right-click
{% endtab %}

{% tab title="Fixed" %}
\#25011 - Integration Images

* Fixed an issue causing the desktop application's integration card images to not display

\#24884 - Radio Integration UI

* Fixed an issue causing the Sonoran Radio integration permission modal to display off screen in certain screen sizes

\#25010 - CAD Integration Keys

* Fixed an issue causing the Sonoran CAD integration community ID/key boxes to clear when initially setting values

\#24980 - Form Limits

* Fixed an issue causing form limits to apply incorrectly in some cases

Backend Log Cleanup

* Improved and cleaned up general backend logging process
{% endtab %}
{% endtabs %}

### 1.1.5 10/09/2024

{% tabs %}
{% tab title="New" %}
Discord -> CMS Name Sync

* Added the ability to sync names from Discord to the CMS, instead of only CMS to Discord. These name syncs also apply to the Sonoran Radio integration.

Roster - Activity Time Options

* Added the option for roster activity time columns to be set to the current week, month, quarter, and year

Roster Webpage Embed

* Added the ability to embed a roster inside of a custom webpage

Community Settings - Improvements

* Small UI improvements to the user's community settings modal, along with a change to a "global" or system-wide re-sync instead of only Sonoran CAD

Mobile App - Prompt to Review

* Mobile app now prompts the user if they would like to leave a review on the app store
{% endtab %}

{% tab title="Fixed" %}
QB Inventory Bug

* Fixed an issue where adding an item to a player's inventory wouldn't save

Bot - Strip Unmapped

* Removed the depreciated and no-longer needed role strip unmapped feature

\#24954 - Webpage Font

* Fixed an issue causing webpage font selection to not save or display

Forms not showing on Profile View

* Fixed an issue causing some forms to not display on the profile view that were submitted by the profile's user

Pagination on Short URLs

* Fixed an issue causing the URL shortnener to not paginate more than 10 items at a time.

Notification Cleanup

* General fixes, improvements, and cleanup for mobile push notifications

Discord Ban - Rank Clear

* Fixed an issue where banning a user via Discord would not clear their CMS ranks on unban.

Roster - Discord Nickname Fetch Timeout

* Fixed an issue with Discord nickname fetching on rosters causing timeouts and failures
{% endtab %}
{% endtabs %}

### 1.1.4 10/01/2024

{% tabs %}
{% tab title="New" %}
Temporary Bans

* Added temporary bans to the user accounts portal

Form Stages - Temporary Bans

* Added temporary bans to form stage actions

Disciplinary Points - Temporary Bans

* Added temporary bans to disciplinary point thresholds

Sonoran Radio Private Channel Sync

* Added private channel permission sync to the Sonoran Radio Integration

Sonoran Radio Name Sync

* Added display name sync to the Sonoran Radio integration

Sonoran Radio Talkover Override

* Added an option to enable the talkover override permission in Sonoran Radio (not yet released)

User Account Search Filters

* Added search filters username, Discord, TeamSpeak, and UID in the admin accounts panel

Name Customization Permission

* Removed the toggle for the community-wide ability for users to update their display name and made it a separate per-user permission

Growth Metrics Mobile Improvements

* Added small mobile UI improvements to the metrics panel graphs
{% endtab %}

{% tab title="Fixed" %}
\#24841 - Radio Sync Toggles

* Fixed an issue with radio sync toggles in the radio integration panel
{% endtab %}
{% endtabs %}

### 1.1.2 09/06/2024

{% tabs %}
{% tab title="New" %}
Disciplinary Action Variables

* Added new point\_reason and discord\_ping variables for automated actions in the disciplinary panel

Radio Integration Perm Breakout

* Added a separate Sonoran Radio panel access permission instead of relying on the Sonoran CAD panel permission

Radio Integration UI Improvements

* Large improvements to the Radio integration panel's rank mapping UI
{% endtab %}

{% tab title="Fixed" %}
\#24250 Form Clone + Stage Internal Fix

* Fixed an issue causing cloned forms to break after cloning and directly navigating to the available forms section without a refresh
* Overhauled internal logic for form stages from a previous migration

\#24371 Form Attachments

* Fixed an issue causing form images to not be saved in the form editor

Fix CMS icon in Discord mapping

* Fixed an issue causing the CMS logo to not display in the mobile and desktop applications in the Discord mapping panel
{% endtab %}
{% endtabs %}

### 1.1.1 08/23/2024

{% tabs %}
{% tab title="New" %}
Growth Panel - Custom Dashboard

* Added a new favorites tab to the growth metrics panel, allow you to toggle, drag-and-drop, and see your favorite metrics at a glance

Form Perm Separation

* Separated the permissions needed to change a form stage and the ability to edit form stage actions

Grant Ranks w/Higher Power

* Separated the permissions needed to grant ranks on a user and grant ranks to a user that have a higher rank power than yours

Avatar - Flag and Point Consolidation

* For user avatars displayed in small areas, the badge for security center flags and disciplinary points has been consolidated to not cover the avatar as much
{% endtab %}

{% tab title="Fixed" %}
\#24134 - Security Flag Nav Badge

* Fixed an issue causing the admin security center navigation button to display the full number of community flags regardless of the new preference settings

Discord Guild Error

* Fixed an issue causing the Discord integration panel to give an un-needed warning in the event that the bot was kicked from a linked guild

\#24263 - Change Name Wrong Endpoint

* Fixed an issue preventing some users from being unable to change their own community name

\#24347 - Stage Actions - Fix Rank Modify

* Fixed an issue causing the rank modifier action on form stage changes to not save
{% endtab %}
{% endtabs %}



### 1.1.0 08/15/2024

{% tabs %}
{% tab title="New" %}
Disciplinary Panel

* An all new panel allowing communities to configure disciplinary points, their expiration time, and point thresholds at which automated actions will occur.

Forms Disciplinary Point Action

* Added a new form stage action to add or remove disciplinary points from a user.

Forms Number Element

* Added a new number form element which can be optionally selected on the forms disciplinary stage action to specify the number of points.

Sonoran Radio Standalone Integration

* Added the ability to configure a Sonoran Radio standalone community for auto-join, kick, and permission sync (requires Radio Standalone Beta v2.5.0)

Webpage Clone

* Added the ability to clone an existing webpage.

Notify Swap to Progress

* Updated several notification popups for basic actions like save confirmations to instead show the orange loading/progress bar at the top for a less-invasive experience.

Discovery Spotlight Description

* Updated the discovery spotlight to display the community's discovery description instead of the tagline.
{% endtab %}

{% tab title="Fixed" %}
\#23965 - Roster Date Range

* Fixed an issue causing the roster date range selector on specific fields to not properly set.

Drive Removal Paths

* Finalized a perminant fix for a previous issue causing Drive files with unusual names to not be removable.
{% endtab %}
{% endtabs %}

### 1.0.2 08/06/2024

{% tabs %}
{% tab title="New" %}
Security Center - Preferences

* Added two new customizable security center preferences (enabled by default) to hide VPN flags on non-pending users and hide alt account flags on accounts not yet in the community

Form Folders - Icon/Image

* Added the ability to customize an icon or image on form folders

Form Types - Consolidation

* Consolidated all existing form types to the new member application (allows pending users to submit) and general form types

Manual Roster - New Row Modal UI Improvements

* Improved the popup modal to configure a new row on a manual roster

Forms Auto-Reply Avatar

* When a form stage adds an automatic reply, the avatar will be the CMS logo or the community logo with [branding removal](../pricing/pricing-faq/branding-removal.md)

Forms Editor - Improvements

* Toggling the dependency on a section in the form editor will no longer cause it to also collapse/expand
* Removed the dependency toggle if the section is the highest in order

Drive UI Improvements

* Added icons on the triple dot menu for existing items
* Moved and adjusted the import from Google Drive button

User Permissions - Translations

* Added missing translation keys for user permission title and descriptions
{% endtab %}

{% tab title="Fixed" %}
New Webpage Name

* Fixed an issue where setting the webpage name on a brand new webpage would result in both duplication and an error

Account UID - Cutoff

* Improved UID cutoff handling in the user accounts panel for users with a long UID value

\#23889 - Drive Issues

* Fixed an issue causing file uploads to not appear until after a refresh
{% endtab %}
{% endtabs %}

### 1.0.1 07/26/2024

{% tabs %}
{% tab title="New" %}
Discovery - AI Approval

* Added a new AI based approval system to approve communities for the discovery page

Drive - Increase Storage Purchase

* Added a new subscription option/addon to purchase additional Drive storage space

Join Community - UI Refresh

* Updated and improved the UI on the community selection screen when searching for a community to join
{% endtab %}

{% tab title="Fixed" %}
\#23476 - Allow Replies

* Fixed an issue allowing submitters to still comment on form submissions after replies were locked

Growth - Mobile Tab Improvements

* Improved the growth panel metric tabs on mobile to have consistent margins and prevent scrolling from changing tabs

\#23824 - Forum Post Overflow

* Fixed an issue causing long forum posts to overflow the page

\#23834 - Delete Assets

* Fixed an issue causing the inability to delete drive files with unconventional names
{% endtab %}
{% endtabs %}



### 1.0.0 (Full Release) 07/17/2024

{% tabs %}
{% tab title="New" %}
Translation Overhaul

* The completion of the full translation overhaul, allowing communities to fully translate the CMS into any language

Forms - Apply Action to Selected User

* Form stage actions can now be applied to user(s) on a member-select field instead of only the form submitter

Form Submission Limits - UI Improvements

* Overhauled the form submissions limits UI

Rosters - Primary vs Secondary

* Removed all references of the old primary and secondary roster rows

Community Discovery

* Improved loading with "skeleton" animation placeholders for a less jarring experience
{% endtab %}

{% tab title="Fixed" %}
Logged Out - Forums Loading

* Fixed an issue preventing forums from fully loading while the user is logged out

Logged Out - Profile Loading

* Fixed an issue preventing user profile pages from fully loading while the user is logged out

Roster Editor

* Fixed a small UI issue displaying an unused grey bar at the bottom of certain column type editors

Spotlight - Fastest Growing

* Fixed an issue causing some communities outside of the 50-250 member range to still be eligible for the fastest growing spotlight category
{% endtab %}
{% endtabs %}

### 0.6.4 (Beta) 07/03/2024

{% tabs %}
{% tab title="New" %}
UID Data Type Restriction

* Increased the numerical size of member UIDs to allow for Roblox identifiers

Discord Mapping - Updates

* Added the ability to update existing Discord mappings of any type

Roster Permissions - Consolidate

* Removed the separate roster add/edit/remove permissions for primary and secondary, and merged into a single permission each

URL Shortner IPs and Ports

* Added the ability to redirect a short URL to an IP address and the ability to add a port number

Webhook Attachment URLs

* Added a hyperlinked content section to all webhooks for any attachment fields in a form

Forms - Section Drag-and-Drop

* Improved the forms editor UI to collapse sections when clicking on the header, and drag-and-drop capability to each header
{% endtab %}

{% tab title="Fixed" %}
Notification Cross-Community

* Improved handling to resolve edge cases causing notifications to go to additional users outside of the intended community

Roster Loading

* Improved handling to resolve edge cases causing roster pagination (changing pages) to load a different community's roster

\#23175 - Forum Bullet Sanitization

* Improved sanitization and UI rendering to ensure forum posts and replies are the same as the post and reply editor
{% endtab %}
{% endtabs %}

### 0.6.3 (Beta) 06/26/2024

{% tabs %}
{% tab title="New" %}
Vanity & Custom Domain - Auto Join on Login

* Users now automatically join your CMS when they login on your custom domain or vanity URL

Discovery Panel - UI Updates

* Updated the UI for community discovery configuration in the admin growth panel

Discord Mapping - UI Improvements

* Overhauled this discord mapping UI to reflect more of an if/then style for more clarity
{% endtab %}

{% tab title="Fixed" %}
\#23042 - Delete Manual Roster Rows

* Re-added the ability to delete rows in custom rosters via right-click

Webhooks - Character Limits

* Added handling to ensure webhooks don't fail due to going over the text length limit

\#22911 - Typo

* Fixed small typos

Mobile - View Submissions

* Fixed an issue on mobile causing the submission type tabs to be oversized
{% endtab %}
{% endtabs %}

### 0.6.2 (Beta) 06/20/2024

{% tabs %}
{% tab title="New" %}
Navbar - Dropdown Icons

* Added customizable dropdown item icons/images

Custom Domain - Login Preservation

* Added new handling to redirect and preserve a community's custom domain when a user logs in via Discord or Apple

Main Menu - Spotlight

* Added spotlight communities to the main community selection menu

Main Menu - UI Refresh

* Refreshed and improved the community selection menu

Homepage - URL Shortener Promo

* Added a promotional slide for the URL shortener to the homepage

Discovery Page - Metrics Tracking

* Added new metrics to see community views and clicks from the discovery page

Improved Spotlight Selection

* Limited the fastest growing communities spotlight category (by percentage) to communities between 50 and 250 members

Form Submission Viewer - Search and Scroll

* Added a search bar to filer form names in the submission viewer
* Added vertical scroll support for desktop in the submission viewer for communities with large amount of forms
{% endtab %}

{% tab title="Changed" %}
Discovery Settings

* Community discovery settings have been migrated to the growth panel's discovery section
{% endtab %}

{% tab title="Fixed" %}
Website Cards - Image Tweaks

* Fixed an issue where setting an image instead of an icon on a website card element would stretch the entire image across the card

Available Page Cards - Add Button Mobile

* Fixed a mobile sizing issue with the website overview new page button

Form Submission Loading

* Fixed a bug causing submissions to not load in rare cases

Roster Loading

* Fixed a big causing rosters to not load in rare cases
{% endtab %}
{% endtabs %}



### 0.6.1 (Beta) 06/12/2024

{% tabs %}
{% tab title="New" %}
Discovery Panel

* Added the start of the redesigned community discovery panel, complete with spotlight and featured communities. Spotlight communities will soon be featured in the main menu of the CAD, CMS, and radio portals.

Enable/Disable Submissions

* Individual forms can now be locked or unlocked to easily open and close applications

Limits Panel

* Revamped the UI on the limits panel, fixed multiple issues, and added the new feature promos for the URL shortener and metrics panel

Metrics - Tooltips

* Added tooltips to every metric in the growth panel better explaining what is being visualized

Discord Integration - Optimization

* Internal UI component optimization with the Discord webhook config panel
{% endtab %}

{% tab title="Fixed" %}
Security Flags - Mobile

* Fixed an issue causing the flag number to not show on the admin navigation bar in mobile

Metrics - Negative

* Changed the lost members stat to red if an increase in value and green if a decrease in value

\#22815 - Roster Editor

* Fixed an issue in live-editing rosters where using the date picker on the date column would fail to auto-save

\#22815 - Form Duplication

* Fixed an issue causing form submissions to appear duplicated on the user profile

\#22927 - Metric Graphs

* Fixed an issue causing metric graphs in the growth panel to only visualize up to the number one each day

Forms

* Fixed a logic issue causing per-section submissions to be disabled if the conditional values were greater than one
* Disabled the required toggle for label type questions
{% endtab %}
{% endtabs %}



### 0.6.0 (Beta) 06/05/2024

{% tabs %}
{% tab title="New" %}
Growth Panel - Additional Metrics

* Added additional community metrics for every custom form and webpage.

URL Shortener

* Added an all-new URL shortener, allowing communities to create URL redirects with their custom domain or vanity URL.

\#22435 - Image Aspect Ratio

* Added a way to unlock the aspect ratio on website images, allowing the user to stretch images.

Discord Mapping - Dependency

* Added a new Discord mapping type "dependency" to grant a more "global" Discord role if the user has one of the listed CMS ranks.\
  Ex: The Discord "Staff" role is dependent on the CMS `Moderator`, `Admin`, or `Owner` ranks. If the user has any of those, the Discord `Staff` role will be applied. Granting the `Staff` Discord role will not grant any other CMS ranks or have any further impact.

Homepage - Security Center Promo

* Updated the CMS homepage with additional feature promos.
{% endtab %}

{% tab title="Fixed" %}
Account Username Ellipsis

* Improved account username overflow handling in the user accounts panel.
{% endtab %}
{% endtabs %}

### 0.5.93 (Beta) 05/30/2024

{% tabs %}
{% tab title="New" %}
Growth Panel

* Added the initial start to the admin growth panel, offering community metrics and performance graphs.

CAD Integration - Permission

* Added a separate permission to access the CAD integration panel.

Rosters - Manual Override

* Added a way to manually set roster cell values on items that rely on conditional formatting. Ex: Setting a staff member's status column to Active manually, even if conditional formatting sets it based on an activity hours column.

Security Center - Log Type Filter

* Added a type to filter system to the security center log types search.

User Profile - Third Party Icon

* Added a third party icon to user profiles in their "submission" columns to show what forms they have submitted but on someone else.

User Profile - Submission Status

* Updated the submission status column on the user profile to show the custom stage/status color and icon.

User Profile - Account Buttons

* Updated the user profile page to use three new improved, icon-based buttons for their Sonoran Account, Community Settings, and account deletion.

Forms - UI Improvements

* Updated the forms editor UI to allow section up/down reordering.
* Updated the new form submission UI to navigate the user through each section individually.

Security Center - Flag Notes

* Added a notes system in the security center for account flags, allowing historic informational/context messages to be saved.

User Profile - URL Improvements

* User profiles are now formatted as community.com/u/id with the ID being the user's numerical unique ID.
{% endtab %}

{% tab title="Fixed" %}
Bot - Form Status Change

* Removed an error message when updating a CMS form stage via Discord embed.

Desktop Apps

* Fixed an issue with local storage and security center device IDs preventing the desktop apps from properly launching.

Mobile Apps

* Fixed an issue with security center device IDs preventing the mobile apps from properly launching.
{% endtab %}
{% endtabs %}

### 0.5.92 (Beta) 05/21/2024

{% tabs %}
{% tab title="New" %}
Security Center - Reactivate Flag

* Added a flag reactivation event if a (alt) user that was not in your community had their flag dismissed, it will re-activate when they later join the community.

Security Center - In-Game Identifiers

* Added new alt account detection methods for in-game identifiers like CFX license, Xbox live, Steam, hardware identifiers, etc.

Security Center - VPN Detection Flag

* Added a new flag type to detect users logging in with a VPN running, potentially trying to evade an IP ban.
{% endtab %}

{% tab title="Fixed" %}
Backend - Startup Without Logging DB

* Fixed an issue preventing the CMS backend from starting if there was a logging database outage.

\#22436 - Drive Permissions

* Fixed an issue with users getting an error when trying to access authorized documents but without the modify all documents permission.
* Fixed an issue with users who do not have the modify all documents permission being unable to edit documents on a rank-specific file.

HF: Logging DB History Clear

* Fixed an issue with system logs being stored longer than 30 days.

\#22434 - Image Popup Size Constraints

* Fixed an issue where the image displays in the website gallery and image editor popups were too large.

Forms Panel - CSS Tweaks

* Fixed minor style inconsistencies on the admin forms panel.

\#22453 - Roster Editor Widths

* Added handling to set a roster column's minimum width when editing it.

\#22450 - Discord Webhook Action

* Fixed an issue where Discord webhooks with an invalid author URL would cause a failure.

\#22452 - Calendar Flag Redirect

* Fixed an issue where clicking on a user's avatar in the calendar event menu wouldn't navigate to their community profile.
{% endtab %}
{% endtabs %}

### 0.5.91 (Beta) 05/15/2024

{% tabs %}
{% tab title="New" %}
Forms - Third Party Sub. Permission

* Added a new permission to restrict which users can submit specific forms as a third party

Forms - Audio Upload

* Added a new form element allowing users to record and upload audio submissions

Forms - Checkbox Section Dependency

* Form sections can now have a dependency based on checkbox select values

Account Avatar - View Profile

* Clicking on a user's account avatar will now automatically redirect to their community profile

Discord Role Import - Filter

* Added a filter search box in the rank manager when importing existing Discord roles

Photo Gallery - Image Uploader

* Updated the image upload component in the website builder's photo gallery element
{% endtab %}

{% tab title="Fixed" %}
\#22313 - Discord Roster Bug

* Fixed an issue causing rosters to not load if they contained a single Discord username column, and no other Discord type columns

\#22312 - Roster Row Editor

* Fixed an issue where Discord and TeamSpeak type roster columns would appear to be editable when selecting the row in the roster viewer

\#22203 - Calendar Event Image

* Fixed an issue causing the calendar event images to not be properly set or edited

(HF) Roster Formatting - Hours over 23

* Fixed an issue causing conditional formatting to break on a roster when relying on a time log or activity hours column that had 24 or more total hours

(HF) Kick and Ban - Remove TS Ranks

* Fixed a vulnerability where kicking or banning a CMS user would not also remove their mapped TeamSpeak ranks.

(HF) CMS Kick - Remove Discord Roles

* Fixed a vulnerability where kicking a CMS user would not remove their mapped Discord roles.
{% endtab %}
{% endtabs %}

### 0.5.90 (Beta) 05/08/2024

{% tabs %}
{% tab title="New" %}
[Security Center - Account Flags](../tutorials/administrative/security-center/account-flags.md)

* Added the base release of the new account flags system for alt account detection.

Rosters - Toolbox Consolidation

* Migrated the side toolbox elements for the roster editor into groups to better consolidate and save space.

Website Builder - Toolbox Consolidation

* Migrated the side toolbox elements for the website builder into groups to better consolidate and save space.

Website Pages - Cards

* Updated the available website pages UI to reflect a similar "card" style like rosters and forms have.

API - Teamspeak ID

* Added `teamspeakId` property to both `get_com_account` and `get_account` endpoints
{% endtab %}

{% tab title="Fixed" %}
\#22294 - Drive Duplication

* Fixed an issue causing Drive documents to show as duplicated.

TS Link/Unlink - Wipe Other Existing Maps

* Patched a vulnerability and added handling to remove all existing/mapped TeamSpeak roles from a user when they unlink their TeamSpeak account, or when a second account links the same TeamSpeak account (resulting in the link being removed from the first account).

Discord Link/Unlink - Wipe Other Existing Maps

* Patched a vulnerability and added handling to remove all existing/mapped Discord roles from a user when they unlink their Discord account, or when a second account links the same Discord account (resulting in the link being removed from the first account).
{% endtab %}
{% endtabs %}

### 0.5.89 (Beta) 04/30/2024

{% tabs %}
{% tab title="New" %}
Rosters - Edit Row UI

* Removed the popup cell/row editor in the roster view and added in-line auto-save editing.

Image Uploads - Drive Storage

* Removed image and file uploading limits throughout the CMS and added this storage to the community Drive. The free plan has been increased from 10MB to 100MB.

Security Center

* Added the start of new internal logging and tracking for the security center, with visible functionalities coming soon...

Logging Center

* Automatically removed logs older than 30 days.
{% endtab %}

{% tab title="Fixed" %}
TeamSpeak Sync

* Fixed issue causing the TeamSpeak sync to not fully remove server groups in some cases.

Nav Bar Dropdown Display

* Fixed a permissions issue causing some dropdown items to not properly display, or display when the user didn't have navigation permissions.

\#21526 - Photo Gallery Fixes

* Resolved multiple bugs with the website builder's photo gallery element

\#21942 - New Form Stages

* Fixed an issue causing new forms to not automatically come with the three default stage options.

\#22005 - Dropdown Item Delete

* Fixed an issue with the nav bar editor's dropdown items not containing a delete button.

\#21099 - Form Stage Actions

* Fixed an issue with older form stage actions being unable to open/expand to configure.

TS Bad Credential Cooldown

* Added a cooldown for bad TeamSpeak credentials to prevent requests from being blocked.

Missing Page Loading

* Fixed an issue where pages that no longer existed in the CMS would cause a long load an an error. Now, it simply kicks the user back to the previous page.

\#21502 - Forms Auto Reply

* Fixed an issue where form stage auto replies would not show in the form submission viewer until a refresh after triggering a stage change.
{% endtab %}
{% endtabs %}

### v0.5.88 (Beta) 04/17/2024

{% tabs %}
{% tab title="New" %}
Activity Tracker

* Easily track member activity in your game server with an automated stopwatch system starting on server join and stopping on server exit

Activity Roster Column

* View member activity time in the last X days with the activity roster column

Last Active Roster Column

* See when your members were last in-game with the last active roster column

Discord Panel Settings

* Adjust all of Sonoran Bot's settings via the CMS UI instead of Discord commands

Website Builder - Forums Category UI

* Overhauled the forums category UI dialog in the website editor

User Profile - Form Submission UI

* Overhauled the forms submission UI in the user profile page

Website Builder - Favicon

* Paid communities now include a custom favicon on CMS website tabs utilizing their community icon
{% endtab %}

{% tab title="Changed" %}
Roster Status Column

* Removed the "status" type roster column and migrated all existing instances to a standard select/dropdown element. Conditional formatting has been automatically added to migrate the status colors.

New Communities - Name Format

* Adjusted the default name format for new communities from {name} | {identifier} to {uniqueUd} | {name}
{% endtab %}

{% tab title="Fixed" %}
\#20752 - TeamSpeak 3 Permissions

* Fixed an issue causing TeamSpeak rank sync to override previously added roles when syncing

\#21695 - Forum Webhooks

* Fixed an issue causing forums webhooks from being configured and sent properly
{% endtab %}
{% endtabs %}

### v0.5.87 (Beta) 04/09/2024

{% tabs %}
{% tab title="New" %}
Security Center - Logging

* Added a new logging section in the security center, allowing user actions to be searched

Forms - Auto Member Unique ID

* Added a new forms element type to automatically fill a user's unique ID

Bot - Improved Permission Errors

* Improved permission errors on Sonoran Bot to be more clear

Bot - Name Sync on Join

* Added handling to process a name sync when a new user joins a guild


{% endtab %}

{% tab title="Fixed" %}
\#21372 - Nav Bar Permissions

* Fixed an issue causing navigation bar items to display even if the user had no page permissions for the item

Community Discord Re-sync

* Fixed an issue causing performance issues when larger communities did a full Discord resymc

\#21351 - QB No Servers

* Fixed an issue where a community having no servers setup in the API panel would cause the wrong error message to be displayed

\#21392 - Forum Loading + Permissions

* Fixed an issue with forum posts being visible when private and an issue with forums loading without permissions causing a black screen

\#21536 - Roster Manual Row Fixes

* Multiple fixes added for manually added roster rows

\#21425 - Form Notifications

* Fixed an issue where certain notification links wouldn't open the specific form if you were already on the forms page

\#21537 - Rosters Date Field YY

* Fixed an issue with date formatting in rosters

\#21403 - Rank Manager Fixes

* Fixed several minor issues in the rank manager

\#21614 - Web Builder - Background Change

* Fixed an issue with being unable to set the webpage background back to non once it was set to image or color

\#21528 - Form Specific Webhooks

* Fixed an issue with custom form webhooks not working

\#21518 - Form Stage Change Webhook

* Fixed an issue with the interactive form stage change embed not working

\#21490 - Time Log Safety Check

* &#x20;Added a safety check to ensure users do not submit forms with negative timesheet values

\#21390 - Remove "Custom Pages" option

* Removed the un-used "Custom Pages" option for nav bar items

87 - Forums Sub-Category UI

* Fixed issues with editing and creating forum sub-categories

\#21768 - Page Backgrounds

* Fixed an issue with uploading images in the website builder
{% endtab %}
{% endtabs %}



### v0.5.86 (Beta) 03/26/2024

{% tabs %}
{% tab title="New" %}
Forms - DM Stage Action

* Added a new forms stage action to DM the submitter on Discord

Discord Webhooks - Bot Handling

* Overhauled how Discord webhooks are stored and processed, with all new webhook configurations being handled by bot posted embeds.

Forms - Stage Discord Ping

* Added the option in forms stages to ping the submitter in Discord.

Forms - Stage Webhooks

* Updated the webhook selector in the forms stages to be channel based instead of raw webhook URLs.

\#21213 - Notification Text View

* Added an icon to view the full notification text in the notification center if the text was cut off.
{% endtab %}

{% tab title="Fixed" %}
\#21103 Discord Mapping Mobile UI

* Fixed an issue causing Discord mappings on the mobile UI to not properly display.

\#21205 - Forms Auto Reply

* Fixed an issue causing forms auto reply messages to not hold the same format that they have in the stage editor.

\#21206 - Notification Events

* Fixed an issue where notifications, specifically in form stage updates, wouldn't appear in the user's notification center until a refresh.

\#21276 - Form Delete

* Fixed an issue preventing a user with permissions to delete their form submission from the available applications panel.

\#21275 - QB Character Link

* Fixed an issue with QB character links.

Sonoran Bot - Single Guild Removal

* Fixed an issue with guild removal.
{% endtab %}
{% endtabs %}

### v0.5.85 (Beta) 03/20/2024

{% tabs %}
{% tab title="New" %}
Forums - UI Improvements

* Improved UI design for creating topics and posts, private topic rank selection, and an all-new image uploader with drop support.

Forums - Website Section Handling

* Migrated new forums elements to a dedicated "section" in the website builder. This ensures forums elements can expand dynamically and push content down instead of overlapping or scrolling.

Forms - File Against User

* Forms can now be submitted on a user via third party for cases like ban requests or disciplinary action. These submissions then appear on the user's profile.
{% endtab %}

{% tab title="Fixed" %}
\#21106 - QB Panel Vehicles

* Fixed an issue in the QB panel preventing the vehicle information dialog from showing.

\#21165 - Desktop Close/Open Error

* Fixed an issue with an error pop-up when opening the CMS desktop app. Additionally, fixed a performance issue spawning duplicate CMS processes in the background and added a new tray icon for Windows.

\#20876 - Form Submission from Profile

* Fixed an issue where submitting a form from a user's profile would cause the same form type to always display.

\#21058 - Drive Sensitivity Save

* Fixed an issue causing the drive sensitivity toggle to not save.

\#20872 - QB Allow/Deny

* Fixed an issue causing the QB Core whitelist allow/deny lists from mirroring the same selection.

Discord Role Import

* Fixed an issue causing Discord role imports on the rank manager to load in the order of selection instead of the order in the selection table.

\#21195 - Deleted Ranks

* Fixed an issue causing rank deletions to still show on user profiles as an "Unknown Rank"
{% endtab %}
{% endtabs %}

### v0.5.84 (Beta) 03/12/2024

{% tabs %}
{% tab title="New" %}
Forums - UI Improvements

* Initial UI improvements for forums, including proper breadcrumb navigation back to the custom webpage, sub-category enforcement, and more.

Rosters - New Column Types

* Added Discord nickname, Discord ID, and TeamSpeak ID columns.

Discord Integration - Loading Animations

* Added new loading animations with live descriptions for the Discord panel. This improves user experience and understanding for larger Discord servers with multiple hundred channels and roles.

Form Stage Variables

* Added a `user_submission_link` (URL for the user that submitted the form to view) and `submission_link` variable (URL for an admin to view the submitted form) in replacement of the older `form_link` variable.
{% endtab %}

{% tab title="Changed" %}
Community Customization - On-Join Rank Selector

* Updated the on-join rank selector component.
{% endtab %}

{% tab title="Fixed" %}
\#20951 - Community ID Change

* Fixed an issue preventing community IDs from being changeable.

\#20898 - Menu Panel Data Requests

* Fixed an issue causing the vMenu panel from requesting QB specific data, resulting in console errors.

Discord Guild Assignment

* Fixed an issue with webhook configurations causing all roles and channels as belonging to the most recently linked guild.

Limits - CSS Tweaks

* Fixed minor placement issues with the community limits panel, and removed the upgrade button for communities already on pro.

QB Character - Metadata

* Fixed an issue causing character metadata in the QB core panel from displaying.

\#21180 - Notification Typo

* Corrected a small typo in the notifications center.
{% endtab %}
{% endtabs %}

### v0.5.83 (Beta) 3/04/2024

{% tabs %}
{% tab title="New" %}
Rosters - Conditional Formatting on Other Cells

* Added the ability to conditionally format both styles and values on a roster cell/column based on the value of another column.

Rank Manager - Search

* Added the ability to search and filter permissions in the rank manager for an easier configuration experience.

Auto Clock-In ESX

* Added ESX job support to the in-game auto clock-in system.

Forms - Submission Button

* Added a "view submissions" button in the available forms section for users that have permissions. This negates the need for the user to have access to the admin forms editor panel just to see the navigation button.

\#20905 - View Profile in Grid Mode

* Added the ability to right-click on a user account card to access their profile, mimicking function of the user accounts panel in list mode.
{% endtab %}

{% tab title="Fixed" %}
\#20795 - Forms Reply Data

* Fixed an issue causing forum threads to show some of the creator's info on replies.

\#20791 - Multi-Account Change Webhook

* Fixed an issue with webhooks not firing on multi/mass-account changes in the user panel.

\#20798 - User Kick

* Fixed an issue causing user kicks to seemingly do nothing

\#20812 - API Unique ID

* Fixed an issue causing the user account unique ID to not be returned in the GET\_COM\_ACCOUNT endpoint.

_Additional bugs have been resolved via live hot-fix and are not listed with this module._
{% endtab %}
{% endtabs %}

### v0.5.82 (Beta) 2/27/2024

{% tabs %}
{% tab title="New" %}
Community Account ID - Modify

* Community administrators can now manually customize a member's UID in the user accounts tab.

\#20479 - Clear All Notifications

* Users can now clear all notifications on their CMS at once.

Community Customization - UI Improvements

* The community customization panel has been overhauled and simplified for a better user interface experience.

Limits Panel - UI Improvements

* The community limits panel has been updated for an improved user interface.

\#20746 - Form Question Descriptions

* Form questions can now have subtext added below the element type.

\#20757 - Form Submission Removal

* Added new delete buttons on the submission card and submission viewer to remove form submissions instead of having to right-click.

\#20766 - Form Stage Email Branding

* Updated the custom form stage emails to include custom community branding in the subject line and included email logo.

\#20767 - Community Member UID Column

* Added the community member UID column to the list view in the user accounts panel.

\#20745 - Stage Customization in Submitter UI

* Added proper stage customization display (icon and color) to the stage listed on the submitter UI section.

\#20762 - Direct Link Stage Response

* Added a new {form\_link} variable in custom form stages to send a direct link to the submitted form.

Custom Emails - Sanitization

* Added additional HTML and script sanitization on custom stage action emails.

\#20754 - Event Redesigned

* Redesigned the UI on the community event viewer and migrated to a dialog popup instead of a full page.

New Form Scroll Height

* Improved the form height scroll calculation for new form submissions, maximizing the user's screen space.

Forms Label - New WYS Editor

* Label elements on the form editor now include the updated WYS editor for better control.

Website Editor - Width Preview

* Improved the width handling on the website editor to show the true width of the page breakpoint being edited. Also added new ctrl + scroll handling to quickly zoom in and out of the editor preview.

API Endpoints - User Variables

* Added the following consistent user variable options:
  * `accId`
  * `apiId`
  * `uniqueId`
  * `discord`
  * `username`
* To the following endpoints:
  * `GET_COM_ACCOUNT`
  * `GET_ACCOUNT_RANKS`
  * `SET_ACCOUNT_RANKS`
  * `CLOCK_IN_OUT`
  * `KICK_ACCOUNT`
  * `BAN_ACCOUNT`
  * `EDIT_ACC_PROFLIE_FIELDS`
  * `VERIFY_WHITELIST`&#x20;
  * `RSVP`
{% endtab %}

{% tab title="Fixed" %}
\#20744 - External URLs

* Fixed an issue causing external URLs in the navbar to not properly open.

\#20749 - Roster Hours

* Fixed an issue with roster time hours showing as invalid.
* Fixed an issue with manually added roster rows not displaying on initial save.

\#20748 - Roster Ranks

* Fixed an issue causing rosters with specific rank selections to load in reverse order.

\#20742 - Clock-In Time

* Fixed an issue causing the total time for click-in import not displaying the amount.

\#20730 - Discord Webhook Selector

* Fixed an issue causing the Discord webhook channel selector to display a webhook URL instead of the selected channel name.

\#20692 - Advertise Encoding

* Fixed an issue causing image URLs to not be fully encoded for special characters in the Sonoran Discord's #advertise-here channel

\#20756 - Calendar Perm Checks

* Fixed an issue allowing users without the create event permission to still create events.

\#20761 - Form Action Template String

* Fixed an issue causing {form\_name} and {stage\_name} variables from not properly displaying in custom stage action text.

Department Name Ellipsis

* Fixed an issue causing departments names in the rank manager from getting cut off instead of showing an ellipsis.

Page Templates - Text Format Update

* Updated the default community pages to have the newly formatted text markup for the improved WYS editor.

\#20863 - Navbar Button Editor

* Fixed multiple issues with the navbar button and dropdown editor, added additional style handling to prevent color clashes.

\#20840 - Initial Discord Sync

* Fixed an issue causing users already in a CMS community that newly linked their Discord account to not receive associated CMS ranks from their existing Discord roles.

_More than several additional bugs have been resolved via live hot-fix and are not listed with this module._
{% endtab %}
{% endtabs %}



### v0.5.81 (Beta) 2/19/2024

{% tabs %}
{% tab title="New" %}
**Rank Editor**\
&#xNAN;_&#x44;iscord Role Import_\
Creating departments and ranks within the editor is now much easier, you can now import any role from a linked guild directly into your community. It'll import name, color, and icon automatically, just select which roles you want imported and moments later they'll be created within your community.

**API Endpoint**\
&#xNAN;_&#x47;et Accounts_\
Fetch all accounts within your community, with filters and paginated. This will return all basic information for returned members.

**WYSIWYG Text Editor**\
The newly added WYSIWYG editor has been reworked to utilize a more feature rich editor, allowing for more control and customization.
{% endtab %}

{% tab title="Fixed" %}
**Accounts - Multi-Actions**

* Changing or setting ranks via multi-actions will now properly process and apply

**Community Profile**

* Viewing your own profile and updating your community name will now update the UI upon successful change

**Website Builder**

* Buttons that target to fill out a form will now properly navigate

**Form Management**

* While viewing a form submission, you can now properly change stages via the dropdown button / options

**Rosters**

* Custom fonts and alignment will now properly display on the viewer side
{% endtab %}
{% endtabs %}

### v0.5.80 (Beta) 2/14/2024

{% tabs %}
{% tab title="New" %}
**Search Engine Optimization**\
Custom pages now have customizable SEO information, you can now set the image and description for the page SEO. This type of information will show within the link embeds in applications such as Discord. Additionally, forms will now have SEO information regarding the form name, description and image.

**Form Management** - **Stages**\
Stages have been completely reworked to be per form rather than globally created individually, primarily for future easier development.\
As well, drag and drop support was added for rearranging the order of stages.

**New Common UI**\
We've created a unified common WYSIWYG text editor to be used throughout the application, allowing the same control through. This is seen within the Website Builder, Forums, etc.
{% endtab %}

{% tab title="Fixed" %}
**Permissions**

* Proper permission evaluation was corrected and validated for viewing any page within the Administrative Panel
{% endtab %}
{% endtabs %}

### v0.5.79 (Beta) 2/6/2024

{% tabs %}
{% tab title="New" %}
**Discord Integration**

We've completely reworked how Discord guild data is fetched for a more efficient and effective method. Configuring your Discord Integration should be populating much faster as data is now concurrently fetched by key, reducing the overall data that is transferred.

Additionally, we've made the following changes:

* Remove Guilds\
  &#xNAN;_&#x52;emove linked guilds directly within the Discord Integration panel, allowing you to unlink guilds you no longer wish to be included in sync events_
* Join Rank Check\
  &#xNAN;_&#x4E;ew members that join your CMS community when a guild is linked will check whether they have any roles in guild(s) for mapped ranks that they should have, automatically applying the ranks on join_

**Website Builder - MAJOR OVERHAUL**

The website builder has seen a massive overhaul, now with the ability for more customization and control over your page designs. Create stunning pages with our new placement system, easily drag and drop elements wherever you want on the page, no longer limited by just column sizing.

As well, when creating new pages you're now able to create from templates or just a blank canvas.

**Navigation Bar**

Bar items now have the ability to have more styles & customization applied to the item. Choose from several different styling options to fit your design needs. As well, the individual item editor was reworked for much better UI/UX.

**Community Settings**

A new data template key was added to the Community Naming format, `{uniqueId}` will now provide their automatically generated unique integer ID.

**Admin Panel**

`Drive` access button was added to the Administrative Panel side navigation, no longer requiring a navigation item to navigate through
{% endtab %}

{% tab title="Fixed" %}
**Website Builder**

* Page background image would not save, it would default back to the color option
* Image uploader options for page background would often display under the image

**User Accounts**

* Rank icon / name badge will now show properly instead of empty space
* Accounts should no longer have Unknown Rank in their rank list, audit functions were added&#x20;

**Discord Integration - Role Mapping**

* Removing / adding a role directly within the role list wouldn't actually save on the backend&#x20;

**Rank Manager**

* Roster & form ALL permission toggles will now properly add / remove all
{% endtab %}
{% endtabs %}



### v0.5.77 (Beta) 1/31/2024

{% tabs %}
{% tab title="New" %}
**Form Management**

Managing forms will now properly paginate based on what's in your current view, the further you scroll down the more submitted forms will populate.

**Game Panel**

Game state fetching was optimized to be more efficient and only needed when requested. Game state data will now manually be fetched from CMS -> Game Server instead of a the Game Server sending a periodic (every 1 minute) update to the CMS to store even if not currently used.\
Data will now be more up-to-date and fluid throughout, as well these optimizations _should_ alleviate some of the _hitch_ warnings seen.
{% endtab %}

{% tab title="Changed" %}
**Discord Integration**

Mobile optimizations have been made to make it easier and more fluid while configuring Discord integration capabilities.

**User Accounts**

Multi-select and filtering have seen several improvements for a better UI/UX
{% endtab %}

{% tab title="Fixed" %}
**Rosters**

* Column colors are now consistent

**User Accounts**

* Join date will now properly show instead of a _random_ date/time

**Forms**

* Conditional sections will now properly be evaluated and populated

**iOS**

* An issue regarding a black/blank screen was addressed, the fix is not guaranteed
{% endtab %}
{% endtabs %}

### v0.5.76 (Beta) 1/15/2024

{% tabs %}
{% tab title="New" %}
**iOS Notch Support**

The iOS finally now has support for the _notch_ that was introduced with iPhone X+, there is now proper spacing for elements that would originally be within the notch area.

**Rosters**

_Discord Guild Nickname Column_\
New column type was added allowing for Discord guild nicknames to be referenced within rosters, this will pull the nickname for the user if they're in the specified guild for the column. Each column can reference a different linked Discord guild to be the source of the nicknames.

_Timeclock Column_\
Several new improvements and additions were introduced. Now allowing for several different timeclock time parameters, allowing to fetch hours within the last amount of days, between two dates or simply from a specific date. These time parameters are set directly on the column within the Roster editor.
{% endtab %}

{% tab title="Changed" %}
**Rosters**

_Timeclock Column_\
While viewing a roster, that has a timeclock column, you can now specify the date range which you are referencing the hours from. Allowing for much easier viewing of hours without the need of modify the roster! Simply modify the date range while viewing the roster and you'll fetch the hours instantly!

_Column Permissions_\
To follow suit with several other aspects of the CMS we've removed the _Mod_ and _Admin_ specific permissions from roster restricting. Columns will now be able to simply specify which ranks have viewable access, no longer requiring to manually grant individual permission to view restricted columns.\
If no ranks are specified the column will be viewable by all members that can view the roster.

**Profile Fields**

Drag and drop support, with the new system, has been introduced for profile fields within the editor. Now reorder profile fields with ease via drag and drop.

**Website Builder**

The _Card_ and _Button_ element editors have been reworked from the ground up, now allowing for much easier editing with instant visual changes. Editing these elements should feel more native and overall easier to use.
{% endtab %}

{% tab title="Fixed" %}
**Rosters**

* Pagination would only allow for a maximum of 100 rows to be fetched, any additional rows would be unable to be accessed

**Branding**

* Branding footer would appear above the Forms Editor

**Common**

* Image preview component wouldn't allow removal of the current image
{% endtab %}
{% endtabs %}

### v0.5.75 (Beta) 1/8/2024

{% tabs %}
{% tab title="New" %}
**Rosters**

_Member ID Column_\
Rosters now have the ability to display member's unique ID as a column type now, this will grab the member's unique ID

_Rank Based Rosters_\
Rosters will now be able to be specified from specific ranks rather than whole department's or utilizing a custom roster. You can now specify what ranks and order that a member must have in-order to be displayed on the roster.

_Cosmetic Styling_\
All roster columns now have the ability to be styled to have more customization over your rosters. Additionally you can set conditions to when a column row cell is a specific styling, allowing greater control on how rosters are displayed.\
\
As well, Rosters can now have a header image displayed above the roster table.
{% endtab %}

{% tab title="Fixed" %}
**Forms**

* Duplicating a form would not duplicate the form stages resulting in a shared stage group with the form you just duplicated from

**Community Customization**

* On Join Settings would not be accounted for when a new member joins, in certain circumstances

**TeamSpeak Integration**

* Several issues regarding timeouts, rate limits, and connection issues were addressed and improved
{% endtab %}
{% endtabs %}

### v0.5.74 (Beta) 1/4/2024

{% tabs %}
{% tab title="New" %}
**Discord Integration**

_Role Mapping_\
CMS bi-directional Discord role sync has been implemented natively within the Sonoran CMS UI. A more visual and easy to use UI in comparison to the existing bot embed setup.

_Ban Sync_\
Bans will now sync across all linked guilds ensuring proper handling of members upon exit.

**Forms**

_Form Editor_\
Drag and drop supported added to form questions, you can now easily re-order questions within a form.

_Submissions_\
On larger screens the form replies will now be on the right side, allowing to view the form response and the replies at the same time.
{% endtab %}

{% tab title="Changed" %}
**Limits**

Drive limits have been increased to the following:\
&#xNAN;_&#x53;tandard:_ 50MB -> 500MB\
&#xNAN;_&#x50;ro:_ 100MB -> 1GB

Uploader max file size has been increased to 200MB to allow for larger documents to be imported into the Drive system.

**Forms**

Stage actions have been updated to our standard components with rank selecting, as well as improvements to the Discord Webhook editor.
{% endtab %}

{% tab title="Fixed" %}
**Webhooks**

Reply settings updates will now show properly for the newly changed reply settings structure.

**Drive**

Sizing with files was improved to no longer appear squeezed on certain resolutions.

Viewing PDFs within the Drive will now properly show instead of kicking back to the main Drive UI.

**TeamSpeak Integration**

Backend functionality was reworked to avoid rate-limits associated with syncing full communities frequently, syncs are now queued and only processed once per minute.

**Forms**

Several issues regarding sizing of question elements was addressed, mostly pertaining to viewing a submission.
{% endtab %}
{% endtabs %}

### v0.5.73 (Beta) 12/18/2023

{% tabs %}
{% tab title="New" %}
**Forms Management**

Form submissions can now be drag-and-dropped to change stages for much easier form submission management, this can be done within the Form Submissions viewer.

**Permission Descriptions**

Permission selectors now display individual descriptions for each permission type, explaining what the permission grants.

**Form Editor**

Permissions for individual form templates can now be modified directly through settings while editing a form
{% endtab %}

{% tab title="Changed" %}
**Custom Domains**

Handling has been improved for failed domains and when communities becoming ineligible for using a set up domain

**Available Forms**

Viewing your own form submissions within your Available Forms page will now utilize the new UI shown within Form Management

**Community Settings**

The UI on smaller / mobile devices has been improved upon for ease-of-use
{% endtab %}
{% endtabs %}

### v0.5.72 (Beta) 12/13/2023

{% tabs %}
{% tab title="New" %}
**Form Builder**

Our custom form builder has seen a complete user-interface rework, now allowing for easier and clearer form building. The new UI was focused on providing a more streamlined and efficient workflow for creating the custom forms needed for communities!

**Discord Bot Integration**

We've implemented Form stage changing directly from Discord form webhooks, form webhooks from CMS are now routed to the Sonoran Bot to provide additional features; form webhooks will now provide a drop-down menu allowing you to select what stage you want the form changed to. When updated the existing webhook embed will be updated for ease-of-use.
{% endtab %}

{% tab title="Changed" %}
**Rank Manager**

We've updated the UI to allow for much better spacing on Desktop and re-introduced mass permission toggles, allowing you to toggle all of one permission section instead of each individual permission.

**Community Settings**

The mobile UI has been updated for much easier use while viewing on the smaller screen.
{% endtab %}

{% tab title="Fixed" %}
**Forms**

* Creating a new form template within a folder will now create the form in the folder instead of the root
* Filter by form type within Available Forms will now properly filter

**Community Profile**

* While opening the Community Settings directly from your Community Profile would utilize the now deprecated settings UI
* While viewing a profile and navigating to your own profile or someone else's directly from that profile would not update the UI with the new profile

**Custom Pages**

* Buttons that linked to a custom form would not navigate to the form for submitting
* Image carousel would not properly display the images set for the carousel

**Identifiers**

* Identifiers were not able to be seen throughout the application, would show in some areas but majority wouldn't show
* Identifiers can now have a default set which will show as your identifier throughout unless otherwise specified in the rosters
{% endtab %}
{% endtabs %}

### v0.5.71 (Beta) 12/5/2023

{% tabs %}
{% tab title="New" %}
**Mobile - Push Notifications**

Android and iOS apps for Sonoran CMS now offer push notifications for all previously supported notification events. Now receive notifications to your mobile device when events start, form status change, and much more!

**Forms - Stage Editor**

Stages editor has continued rework from last update now with more seamless editing and managing.

New forms will now have three (3) default stages for quick form creation!
{% endtab %}

{% tab title="Changed" %}
**Community Menu**

Mobile UI has been improved for a better user-experience.

**Drive**

Sizing of drive items was improved for better viewing of multiple items within the drive item viewer.

**Rank Manager**

Permission editing modal sizing was improved on mobile for easier management.
{% endtab %}

{% tab title="Fixed" %}
**Forms Builder**

Mobile optimization and overall functionality improvements were made as it was difficult to create and edit forms

**Forums**

Usernames now ellipsis when too long, no longer expanding the UI
{% endtab %}
{% endtabs %}

### v0.5.70 (Beta) _v0.5.69 Re-Release w/ Breaking Hotfix_

### v0.5.69 (Beta) 11/20/2023

{% tabs %}
{% tab title="New" %}
**Form Management**

Form submissions are now easier to manage with the reworked UI, now easily move forms through stages with ease with the all new stage tab UI. Forms will now be in a list beneath their respective stage, allowing for easier distinction and visualization of where your community's forms are!

Form Submissions are now accessible via Administrative Panel > Forms > View Submissions button.

Submissions viewed in the new tabbed UI will now show the new submission popup modal with a more informational and condensed view.

**Drive**

File viewer UI has been reworked for a more user-friendly and informative experience. Folders are now displayed separately from any files in the parent folder in the grid view, in the list view folders are sorted above any files in the parent folder.

Additionally, the view and edit drive file UI was updated to be more consistent.
{% endtab %}

{% tab title="Changed" %}
**Default Community Data**

* New community default data was updated with modified pages.

**Rank Manager**

* Several aspects of the rank manager were improved for mobile sizes.
* Primary & Secondary Only options are no longer used

**Drive**

* Ranks with Access Permissions now uses the newer rank selector component

**Website Builder**

* Mobile improvements were made to page, section, and element setting modals
* Border show/hide is now only one button

**Consistency Changes**

* Website Pages
  * A standard/common card style was applied to select, delete and add more

**Misc.**

* All notify button icons were changed to a bell icon
* Add status button on mobile has better size handling within rosters

**Branding**

* Footer branding was condensed to just Sonoran CMS
* Free communities can now change the icon in the toolbar within the customization settings
{% endtab %}

{% tab title="Fixed" %}
**CMS API**

* Add button is now the proper size while viewing on a larger screen

**iOS Application**

* Top community toolbar no longer is cut off by the notch

**Community Profile**

* Community name no longer overflows off the screen on mobile

**Drive**

* Drive UI no longer turns blank after closing share settings
* Changes to the general access settings will now consistently persist
* General access drop down should no longer display nothing or "Unknown"
* General access settings now show on PDFs
* Clicking the _Cancel_ button on the Share Settings modal will now cancel any changes instead of auto-saving
* Auto-save notification is now grammatically correct
* Changes to ranks viewer/editor permission will now consistently persist
* Clicking and losing focus on the document name input will no longer error out
{% endtab %}
{% endtabs %}

### v0.5.68 (Beta) 11/10/2023

{% tabs %}
{% tab title="New" %}
**Website Builder**

_Element Offsets_

Element offsets now allow for further customization of spacing and position of elements throughout your custom pages built through the Website Builder.

_Element Image Support_

Elements can now have images set on them similar to setting a page background but solely on an element.

**Discord Integration**

Improvements to the mobile aspect of the UI have been added specifically to the setup process, making it easier to follow the instructions and get set up faster!
{% endtab %}

{% tab title="Changed" %}
**Help Modal**

Several UI/UX improvements have been introduced.

**Integrations - CMS API / Sonoran CAD / TS3**

Mobile improvements have been made and other small UI tweaks to make the UX better.

**Account Viewer**

There's no longer a _Primary Identifier_ column as that was deprecated for the new identifier system recently
{% endtab %}
{% endtabs %}

### v0.5.67 (Beta) 11/8/2023

{% tabs %}
{% tab title="New" %}
**Toolbar Editor**

You can now drag and drop the order of toolbar items to easily create the toolbar you desire.

**Profile Fields Editor**

Drag and drop of profile fields will now display a red line to signify where the profile field will be dropped.

**Discord Bot**

Improved handling has been introduced into the bot to make the setup and manage process easier when configuring the Discord bot.

**Page Meta**

All informational and administrative pages now have unique meta associated with them, allowing for easier differentiating of pages.
{% endtab %}

{% tab title="Changed" %}
**Forms**

* Multi-member & member selector inputs now allow for input to filter specific members without the need to scroll and manually find the member
* Patrol Log has been rebranded to Time Log
* Default icons have been introduced to default form types
* Submission Replies
  * Submission replies have been completely reworked and simplified, reply settings are no longer locked to: "Basic", "Mod", and "Admin".
  * Reply settings are now based on if the replies are locked, if the submitter can reply when locked and what ranks can reply
* Stage Action: Community Status
  * UI has been improved for a more clear and concise UX
* Clock In/Out has been moved to the element list as opposed to being a section
  * Though it is still a section, just more visible within the UI
* Auto Member Elements will now default to the Form Submitter as the reference
{% endtab %}
{% endtabs %}

### v0.5.66 (Beta) 10/27/2023

{% tabs %}
{% tab title="New" %}
**Desktop Notifications**

We've now introduced Desktop notifications as our first step to push notifications everywhere! Now receive desktop notifications, where configured, when you receive new form submissions, new calendar event, and much more! Manage your notification preferences directly within your Community Settings similar to API ID. Receive Desktop notifications upon each trigger WHEN you have the Sonoran CMS Desktop application running on your device.

[**QBCore Game Panel**](broken-reference)

**Job Sync** has been reworked into the core resource and implemented natively within the QBCore Game Panel, easily manage your server's jobs with automatic job sync!

**Rank Manager**

Drag and drop line previews are now present when managing your ranks, easily see where your organizing your ranks in real-time.

**Toolbar Editor**

Toolbar editing is now supported through auto-save functions, never worry about losing work toolbar customization!
{% endtab %}

{% tab title="Changed" %}
**Template**

Default community template has been updated for a more generic gaming community focus

**User Accounts**

* Mass Account Actions: Rank manipulation is now utilizing the standard component for selecting ranks
* Individual Account Actions: Rank manipulation is now utilizing the standard component for selecting ranks
* User Filter
  * Rank selection is now utilizing the standard component
{% endtab %}

{% tab title="Fixed" %}
**Community Discovery**

* Community banner image URLs that contained spaces would not be URL encoded to be properly loaded when sent through Discord

**Form Management**

* When viewing a submitted form you don't have access to it would provide a blank page instead of notifying user

**Form Management**

* Form Settings button would overlap Form Stage Settings dialog
* Drag and drop would not work in certain instances, overall improved functionality
{% endtab %}
{% endtabs %}

### v0.5.65 (Beta) 10/24/2023

{% tabs %}
{% tab title="New" %}
[**vMenu Game Panel**](broken-reference)

**Weather** and **Time Management** is now available within the vMenu Game Panel, easily change and manage vMenu Weather & Time directly from your Sonoran CMS!

**Homepage**

We've reworked out homepage to be more modern and information forward!
{% endtab %}

{% tab title="Changed" %}
**Website Builder**

* Information block items can now be dragged and dropped to be reordered
* Gallery - Create Category & Forums - Create Category now uses the standardized component for managing permissions
{% endtab %}

{% tab title="Fixed" %}
**Forms Editor**

* Unable to change the Form Type as the selector would provide blank labels
* Re-organizing forms/folder within the selector would overwrite some forms within folders
* Drag and dropping a new element into the blank area where no section is will now properly create a section for the new element instead of doing nothing

**Website Builder**

* Drag and dropping a new element into the blank area where no section is will now properly create a section for the new element instead of doing nothing
{% endtab %}
{% endtabs %}

### v0.5.64 (Beta) 10/16/2023

{% tabs %}
{% tab title="New" %}
**Mobile Improvements**

* Color styling is now more consistent in the Forms Editor
* Form Settings are now a popup modal instead of a drop-down button
* New element selection has been reworked for an improved UI/UX
* Accounts Viewer has been improved for easier mobile UI/UX
* **Rosters** now mimic the Forms Editor styling and functionality with reworked UI/UX
* QBCore Game Panel navigation is now easier to use with more consistent styling
{% endtab %}

{% tab title="Changed" %}
**Website Builder**

* Section and element backgrounds support transparency now
* Text elements support hyperlinks

**Form Management**

* Filtering is now persistent, once you change filtering it will be locally saved upon the next visit to the page.
{% endtab %}

{% tab title="Fixed" %}
**Website Builder**

* Section backgrounds would only display on the editor and not on the viewable page
* Button styles wouldn't save on the editor and wouldn't display on the viewable page
* Text elements when created when have alignment issues with the builder vs the viewable page

**Discord Integration**

* Invite Sonoran Bot button will now properly let you invite the Discord bot
* Admin - General webhooks would unreliably trigger

**Ranks Editor**

* Editing a department would unreliably save
{% endtab %}
{% endtabs %}

### v0.5.63 (Beta) 10/11/2023

{% tabs %}
{% tab title="New" %}
[**Sonoran Bot Integration**](../integration-capabilities/discord-bot-integration.md)

Name Sync now takes in account the name format set within Community Customization!

**vMenu** **Game Panel**

Now introducing the _vMenu_ Game Panel, similar to the QBCore Game Panel we've implemented a user-friendly way to manage your _vMenu_ server(s). Manage whitelisting and ace permissions directly within your Sonoran CMS community without the need to mess with config files.

* Whitelisting & Ace Permission Sync configuration now integrated within the UI&#x20;
{% endtab %}

{% tab title="Changed" %}
**Rosters & Forms Editor**

Several aspects of both UI's have been improved for a better UI/UX, specifically with varying sizes.

**Website Builder**

Several aspects of the website builder have been improved upon and corrected for any inconsistencies and irregularities with sizing. As well, improvements to newly created elements with default data.
{% endtab %}

{% tab title="Fixed" %}
**Website Builder**

* Page permission selector would show blank/missing in some cases

**Profile Fields**

* Select type profile fields wouldn't be able to be selected

**Community Events**

* Public shared event links would unreliably load with varying conditions
{% endtab %}
{% endtabs %}

### v0.5.62 (Beta) 10/2/2023

{% tabs %}
{% tab title="New" %}
**Profile Fields**

* Permission management is now reworked and easier with direct permission management within the Profile Fields editor

**Website Builder**

* Drag and drop previews for when creating unique and custom web pages
{% endtab %}

{% tab title="Changed" %}
**Mobile Improvements**

* API Panel now allows scrolling instead of swapping tabs
* Community Settings tabs are now on top for easier recognition
* _Discord Webhooks_ are now much easier to navigate and use from a smaller device
{% endtab %}

{% tab title="Fixed" %}
**Community Menu**

* If a community didn't have a description it would show the card as blank when hovering over it

**Rosters**

* Patrol logs columns should now accurately show proper hours for Custom rosters
* Identifier columns are now able to be utilized with the new identifier system, now select an identifier to show for that row
* Switching between rosters from direct toolbar buttons is now possible without the need of refreshing
* Selecting a source form for patrol log hour columns will now properly display the label of the form

**Form Management**

* If you delete a form template you can now delete a submitted version of that form template

**Website Builder**

* Video elements are now able to be edited to show a different YouTube video
{% endtab %}
{% endtabs %}

### v0.5.61 (Beta) 9/25/2023

{% tabs %}
{% tab title="New" %}
**User Accounts**

* _Discord_ and _TeamSpeak_ IDs are now on user accounts and can be easily copied in the Accounts viewer
* Unique IDs is now able to be copied on forum replies

**Sonoran CMS API Panel**

* Entire API panel has been reworked for a better UI/UX

**Rank Selector**

* UI improvements have been introduced for easier rank recognition
* Component has been standardized for use within the Account Viewer
{% endtab %}
{% endtabs %}

### v0.5.60 (Beta) 9/16/2023

{% tabs %}
{% tab title="New" %}
**Accounts - Unique ID**

* You can now easily click to copy unique IDs that are displayed

**Discord Bot**

* CMS Name Sync have been added to the initial setup process

**Website Builder**

* Permissions for private pages are now directly within the Website Builder UI, allowing for easier page management without the need to modify ranks

**Forums**

* Forum Topics and Replies can now have text color & highlight
{% endtab %}

{% tab title="Changed" %}
**Community Menu**

* Community creation UI has been improved for better sizing and readability between screen sizes
* Community cards are now larger and have better handling for content

**Community Settings**

* Several aspects have been improved upon for a better UI/UX

**Website Builder**

* Several aspects have been improved upon for a better UI/UX specifically for mobile
{% endtab %}

{% tab title="Fixed" %}
**Discord Webhooks**

* Specific webhooks logs wouldn't send but general/all webhooks would send
* Account Updated webhook embed now properly shows ranks instead of `[object Object]`

**Discord Integration**

* Upon initial load of the panel you would be greeted with an error if you haven't set the bot up already

**Accounts - Identifiers**

* Some communities wouldn't be able to add idenfitiers to accounts

**Custom Forms**

* Editing the header of a section wouldn't be able to be focused to edit

**TeamSpeak Integration**

* TeamSpeak Server Groups select wouldn't filter dispite being able to type

**Custom Pages**

* Tutorial help icon would show when viewing a page with a gallery component
{% endtab %}
{% endtabs %}



### v0.5.59 (Beta) 9/8/2023

{% tabs %}
{% tab title="New" %}
**Account Viewer**

_Multi-Account Actions_

Now you can easily manage groups of accounts instead of individually updating them. You can now set ranks, kick or even ban a group of accounts all at once, allows for easier and a more streamlined user management.

_Rank Filtering_

Filtering and searching for the Accounts viewer has been improved, you can now filter by individual ranks and search for users by their _new_ Unique ID.

[**QBCore Game Panel**](broken-reference)

* Job Management is now achievable within Sonoran CMS, you can now edit/change the job and grades for individual accounts.
* Search vehicle plates via the Vehicles table

[**Discord Bot**](../integration-capabilities/discord-bot-integration.md)

* Sonoran CMS community names are now able to be synced to your Discord guild(s)
{% endtab %}

{% tab title="Changed" %}
**UI Consistency**

Several aspects of the platform have been reworked for a better UI/UX while improving our overall styling consistency

* Calendar UI
* Website Builder - Modals
* API Integrations
{% endtab %}
{% endtabs %}

### v0.5.58 (Beta) 9/2/2023

{% tabs %}
{% tab title="New" %}
**Rosters**

Rosters no longer require a member to be assigned to a row for Custom Rosters, you can now create rosters more than for tracking members!

* Several aspects of the Rosters Editor has been improved upon for a better UI/UX

[**Discord Webhooks**](../integration-capabilities/discord-webhooks.md)

You can now select what roles you want to get mentioned with each Discord Webhook log, just select what ranks (supplied by Sonoran Bot) you want mentioned and they'll be sent along with each log!

* Additionally, Minor UI/UX Improvements

[**TeamSpeak Integration**](../integration-capabilities/teamspeak-3-role-sync/)

You can now select TeamSpeak groups instead of having to manually input UIDs for each one during the role sync setup!

**GTA Integration - Core**

* Project Sloth Inventory Support Added
{% endtab %}

{% tab title="Changed" %}
**Forms Editor**

* Several aspects have been improved upon for a better UI/UX

**Calendar**

* RSVP Limit is now straight forward by selecting unlimited or inputting a desired amount
* Several aspects have been improved upon for a better UI/UX

**Toolbar Editor**

* Drag-and-drop previews are now shown when moving items around your toolbar editor

**User Accounts**

Ranks are no longer separated by _Primary_ and _Secondary_, all ranks are now seen as the same type but are evaluated by power. You no longer need to mark ranks as a specific type and you can now easily assign ranks to users without the confusion of what type each rank is. Additionally this will ease the process with Sonoran Bot setup!

Additionally, account identifiers have been combined into one group instead of separating by Primary & Secondary.

[**QBCore Game Panel**](broken-reference)

* Several aspects have been improved upon for a better UI/UX, specifically with mobile handling
{% endtab %}
{% endtabs %}

### v0.5.57 (Beta) Non-Web Version Release 8/29/2023

There was a hotfix version bump release that was sent to Web, MacOS, and Windows platforms to fix a new forms reordering issue.

### v0.5.56 (Beta) 8/29/2023

{% tabs %}
{% tab title="New" %}
[**Discord Webhooks**](../integration-capabilities/discord-webhooks.md)

The input system for webhooks has been completely reworked and streamlined for a easier setup and management. Now you can select channels pulled from all Discord guilds the Sonoran Bot is setup for with your community.

* Auto-save functionality is now smoother and more efficient
* Setup process is now outlined within the UI

[**QBCore Game Panel**](broken-reference)

Several aspects of the game panel have been improved upon for a better UI/UX.

* More consistent styling throughout pages
* Viewing a character now shows owned vehicles
* Viewing characters on the Players page will now show basic information
  * Cash & Bank Balances&#x20;
  * Jobs&#x20;
* Resources page now supports folders&#x20;

**Community Account Unique IDs**

All users within communities are now automatically assigned a unique numerical ID upon join, existing communities automatically assigned IDs. Easily track users within your community with a much easier identifier to track that NEVER changes.

* Unique IDs are shown on the Community Profile, Forums, Account Viewer, Submitted Forms, etc.
{% endtab %}

{% tab title="Changed" %}
[**Sonoran CAD Integration**](../integration-capabilities/sonoran-cad-sync.md)

* Overall page has been reworked for a better UI/UX
* Setup process have been reworked to follow standardized stepper

**Calendar - Categories**

* Mobile UI functionality has been added
{% endtab %}

{% tab title="Fixed" %}
**Information Blocks**

* Blocks linked for total members of a department would only count users that have the rank as a secondary, not counting primary users.
{% endtab %}
{% endtabs %}

### v0.5.55 (Beta) 8/18/2023

{% tabs %}
{% tab title="New" %}
[**Rosters Editor**](../tutorials/user-management/creating-custom-rosters.md)

* UI was completely reworked to be more interactive and user-friendly
* Community Statuses has been moved to the Roster Editor and rebranded to Roster Statuses

[**QBCore Game Panel**](broken-reference)

* Vehicle management dialogs with user/character information is now hyperlinked to manage the character that the vehicle belongs to

**Toolbar**

* You can now set a button destination to _QBCore Game Panel_
{% endtab %}

{% tab title="Changed" %}
**Footer**

* Now forced to the bottom of the screen when there's not enough content on the page

[**Forms**](../tutorials/forms/creating-custom-forms.md)

* You can now reorder forms in and out of folders by simply dragging and dropping to the desired position

**Toolbar**

* Drop downs on mobile will no longer show if there's no options in the dropdown

[**Website Builder - Gallery**](../tutorials/community-website/gallery-system.md)

* New gallery categories will now automatically have one image created with it
{% endtab %}

{% tab title="Fixed" %}
[**Drive**](../tutorials/your-drive-and-documents.md)

* Preview images were not getting generated upon saves
* Manually saving (Ctrl + S) a document, slideshow, etc. would throw an error despite successfully saving

[**Clock In/Out**](../tutorials/forms/clock-in-out-system.md)

* Adding a clock in/out note after clocking in would add the note to the clock in/out previously created

[**Profile - Change Name**](../tutorials/user-management/viewing-a-community-profile.md)

* Despite having the _Allow Members to Customize Name_ users wouldn't be able to change their name

**Calendar**

* RSVPing for an event wouldn't do anything when clicking the button
* _Irregular_ - Calendar event times would be initially incorrect after creation&#x20;
{% endtab %}
{% endtabs %}

### v0.5.54 (Beta) 8/15/2023

{% tabs %}
{% tab title="New" %}
[**QBCore Game Panel**](broken-reference)

* Vehicle management inputs that require a Citizen ID will now provide users with a select input to select a character from rather than a raw Citizen ID
* Permissions
  * QBCore Game Panel permissions have been moved from the Servers tab to their own category/section.
  * _Existing permissions have been migrated to the new permission structure for Game Panel(s)._

**Help/Tutorial Modals**

* 25+ help and tutorial modal's have been implemented throughout the entire platform
* View documentation and tutorials associated with pages by clicking the red help button located on the bottom-right of pages
{% endtab %}

{% tab title="Changed" %}
**Profile Fields**

* Verified profile fields will now visually show which are verified or not with the Sonoran CMS orange checkmark
{% endtab %}
{% endtabs %}

### v0.5.53 (Beta) 8/3/2023

{% tabs %}
{% tab title="New" %}
[**QBCore Game Panel**](broken-reference)

* Initial Setup
  * The setup process for the panel has been placed directly into the panel with direct and easy steps to get it running.
* Inventory
  * Inventory items now are draggable, you can now drag and drop items within inventories with ease.
* Inter Panel Links
  * Any dialog popup that lists data is now linkable, while having the dialog open the URL is modified to include the proper ID which can be directly opened to.
* Characters
  * Metadata
    * You can now view character metadata within the Character dialog
  * Jobs
    * You can now view character job data within the Character dialog

[**Integrations**](broken-reference)

* [GTA RP - CMS Core](../integration-capabilities/in-game-integration-resources/core/core-submodules/)
  * You can now download the GTA RP CMS Core directly from the Integrations Portal, it will be downloaded with your community credentials already inputted into your config.
{% endtab %}

{% tab title="Changed" %}
[**Custom Domain**](../tutorials/customization/custom-domain.md)

* Custom domains now go through a more thorough DNS record check to ensure domains are assigned to the proper communities.

[**Drive**](../tutorials/your-drive-and-documents.md)

* Several aspects of the Drive UI have been improved for a better UI/UX.
* Several actions on the Drive UI have been reworked to handle auto-saving instead of manual saves.

[**API Integration**](../developer-api-documentation/api-integration/)

* Servers managing has been reworked to handle auto-saving instead of manual saving.
{% endtab %}

{% tab title="Fixed" %}
**Custom Forms**

* An issue where conditional sections would cause problems when determining form completion
{% endtab %}
{% endtabs %}

### v0.5.52 (Beta) 8/2/2023

{% tabs %}
{% tab title="New" %}
[**QBCore Game Panel**](broken-reference)

* Characters
  * View and manage character inventories directly within the panel
    * Mimicked UI from popular slot based inventory systems
* Items
  * View and manage all in-game items directly within the panel
    * Directly upload item images from Sonoran CMS to your game server
* Vehicles
  * You can now select from all preconfigured garages to set a character's vehicle current garage at instead of having to provide the garage ID
{% endtab %}

{% tab title="Changed" %}
**Profile Fields Editor**

Several aspects of the Profile Fields Editor have been reworked in favor for a better UI/UX

**Drive**

Several aspects of the Drive system have been reworked in favor for a better UI/UX, as well as some QOL changes for a smoother transition within pages and actions.
{% endtab %}

{% tab title="Fixed" %}
**Calendar**

* Clicking the event removal button wouldn't actually do anything and would only fail no matter the conditions
{% endtab %}
{% endtabs %}

### v0.5.51 (Beta) 7/21/2023

{% tabs %}
{% tab title="New" %}
[**QBCore Game Panel**](broken-reference)

* Gangs
  * View and manage QBCore framework gangs
  * Add and remove what grades each gang has
* Jobs
  * View and manage QBCore framework jobs
  * Add and remove what grades each job has

**Sonoran Shield Integration**

You can now link and manage your Sonoran Shield configurations directly within Sonoran CMS! You can also grant individuals permission to help manage your shield as well!
{% endtab %}

{% tab title="Changed" %}
**Custom Domain**

The entire verification process as well as UI have been completely reworked to have a better UI/UX.

**Community Selection**

The community selection menu has been reworked for a better UI/UX.
{% endtab %}
{% endtabs %}

### v0.5.50 (Beta) Non-Web Version Release 7/15/2023

There was a hotfix version bump release that was sent to all non-web version platforms to fix a new login issue.

### v0.5.49 (Beta) 7/14/2023

{% tabs %}
{% tab title="New" %}
[**QBCore Game Panel**](broken-reference)

* Characters
  * View online & offline characters
  * Edit online & offline characters
* Vehicles
  * View online & offline vehicles
  * Edit online & offline vehicles
* Permission Enforcement
  * Pages within the game panel are now permission enforced therefore you must have permission to view pages.
{% endtab %}

{% tab title="Changed" %}
[**Discord Integration** - **Webhooks**](../integration-capabilities/discord-webhooks.md)

Discord Webhook Notification editor UI has been completely reworked for a better UI/UX, editing should now auto-save instead of requiring a manual save.

[**API Integration**](../developer-api-documentation/api-integration/)

Servers editor for API Integration has been completely reworked for a clearer and better UI/UX.
{% endtab %}

{% tab title="Fixed" %}
[**Rank Editor**](broken-reference)

* Auto-save has been optimized to not trigger when no changes have been made.
* Duplicating rank wouldn't trigger a auto-save.
* Delete a rank wouldn't give a clear indicator whether it's been processed or not.

[**Website Builder**](../tutorials/community-website/website-builder.md)

* Changing a `image` component will not properly change the image instead of applying it as a background to the existing placeholder image.
{% endtab %}
{% endtabs %}

### v0.5.48 (Beta) 7/6/2023

{% tabs %}
{% tab title="New" %}
**Discord Integration**

Form Stage changes will now trigger the Sonoran Bot to notify the submitter of the form that it's been updated! With Discord Sync enabled and form notifications properly configured you can now receive a Discord notification via DM, text channel or both.

[**QBCore Game Panel**](broken-reference)

* Server Logs
  * View and search the last 1,000 logs generated by your server directly within your Sonoran CMS community!
* Resource Management
  * Easily start/stop all your server's resources directly within your Sonoran CMS community!
{% endtab %}

{% tab title="Changed" %}
**Image Uploading**

All applicable image uploaders have been replaced with our newly created component for ease of use!

**Forms Editor**

The same handling and editing from the Website Builder have been carried over to the Forms Editor, now you'll click an element field to edit.

**Limits & Integrations**

Several aspects of the UI have been improved upon for a clearer UI/UX.
{% endtab %}
{% endtabs %}

### v0.5.47 (Beta) 6/30/2023

{% tabs %}
{% tab title="New" %}
[**Calendar Consolidation**](broken-reference)

All aspects of the calendar system has been consolidated to the main calendar view, editing and adding event categories can now be edited and managed within there. You can now easily manage permissions specifically for the calendars you're editing. The event creation UI has also been improved for a better UI/UX.

[**QB Core Game Panel**](broken-reference)

* Warn Player
* Characters
  * Display Character Info
  * Adjust Money
{% endtab %}

{% tab title="Changed" %}
**Rank Manager**

Rank Manager UI has been improved for a more seamless and interactive experience, rank data now auto-saves as you edit.

**Community Member Name Change**

Now enabled by default for new communities.

**Website Builder**

* Many aspects of the website builder has been improved.
* Pages within page overview are in alphabetical order.
* Mobile UI has been improved.

**Toolbar Editor**

General UI/UX improvements have been made.

**Connection Interruption Banner**

Connection banner will now take longer to appear to allow for reconnections and brief connection drops.

**Admin Accounts**

Rank labels no longer overflow the UI.

**Forums**

Category labels will no longer overflow the UI, they'll now ellipsis.

Rank titles within forum posts will no longer overflow the UI, they now ellipsis.
{% endtab %}

{% tab title="Fixed" %}
**Available Forms**

* Form titles with a very large amount of characters will no longer overflow UI and will now ellipsis.

**Forms Editor**

* Form titles with a very large amount of characters will no longer overflow UI and will now ellipsis.

**Website Builder**

* HTML & Image component editor will now have the proper inputs for editing.

**Admin Panel Navigation**

* Navigation button will now not show above popup/dialogs.

**Toolbar Editor**

* Adding a dropdown toolbar item will now properly add the item instead of removing all other items.
{% endtab %}
{% endtabs %}

### v0.5.46 (Beta) 6/23/2023

{% tabs %}
{% tab title="New" %}
[**QB Core Management Panel**](broken-reference)

The first update to our official QB Core management panel for GTARP!

New functionality includes:

* Permissions
  * Ranks can now be granted permissions to access/use various features of the panel.
* Players
  * Kick
* Vehicles
  * Repair
  * Despawn
* Money
  * Edit Account Balances (Wallet, Bank, Crypto, etc)
{% endtab %}

{% tab title="Changed" %}
**Admin Panel**

* Dragging the admin navigation show/hide button up and above the toolbar will no longer be possible, it will restrict just below the toolbar.

**Toolbar**

* Direct URL destination buttons will now open links in a new tab instead of taking over the current CMS tab.

**Form Management**

* The old route `forms/mgmt` is now deprecated and now transfers you to the main forms hub, button destinations for Form Management now have additional handling to direct to the manage tab.

**Custom Pages / Website Builder**

* Custom page slugs are no longer case sensitive.
* Buttons will now open links in a new tab instead of taking over the current CMS tab.
* Saving a custom page will no longer kick you back to the page selector.
* Improved border UI to differentiate the screen size.
* Many improvements to various components for the website builder.
{% endtab %}

{% tab title="Fixed" %}
**Drive**

* Long document names would overflow the UI card, they should be truncated now.

**Community Profile**

* Attempting to _Sync CAD_ through the Settings dialog within the community profile would error out and not complete.

**Rosters**

* Editing a roster row that contains a date field would not allow you to select dates via the date picker.

**Admin Panel**

* **Mobile:** Touching the admin navigation show/hide button would not always work due to conflicting events getting fired, it should be draggable without issue.

**Toolbar**

* Dragging/reordering handling for toolbar items has been improved/fixed.
  * Previously unable to drag one to the very most right, it would only allow on very last item.
{% endtab %}
{% endtabs %}

### v0.5.45 (Beta) 6/19/2023

{% tabs %}
{% tab title="New" %}
**QB Core Management Panel**

The initial release of our official QB Core management panel for GTARP is here!

Initial functionality includes:

* Players
  * View and Kick
* Player Vehicles
  * Repair, Delete and Despawn
* Player Bank Accounts
  * View, Add Money, Remove Money

More functionality is planned for weekly releases! The CMS QB Core management panel will soon be your single management point for your QB server!

[**Community Creation**](../tutorials/getting-started/registering-your-community.md)

The Community Creation UI has been completely reworked, now walking new users through a guided process to upload and customize logos, descriptions, and more.

**Form Manager Consolidation**

The form manager and available forms sections have been combined into a single panel. This requires less overall navigation and also includes a tab for admins to quickly access the forms editor.

**Admin Navigation Bar**

The admin side navigation bar's toggle button is now condensed into a vertical button with dynamic opacity when collapsed to reduce screen footprint. Additionally, users can now click and drag the toggle button vertically up or down the screen.

**Integrations**

A new Integrations Portal has been introduced, this portal houses all integrations that Sonoran CMS offers. From official integrations to community driven integrations this is the one place to manage it all. With more comprehensive integrations planned in the very near future.
{% endtab %}

{% tab title="Changed" %}
**Default Template**

The default website template for new communities has been reworked. This includes improved and condensed navigation, breaks feature elements into dedicated pages, and more.

**Toolbar Spacing**

Increased spacing between toolbar items for more clear separation.
{% endtab %}
{% endtabs %}



### v0.5.44 (Beta) 6/8/2023

{% tabs %}
{% tab title="New" %}
[**Community Customization**](../tutorials/customization/)

The entire Community Customization UI has been completely reworked from the ground up, focused on an improved UI/UX.

**Administrative Panel Navigation**

Administrative panel navigation has been completely reworked from the ground up similar to Community Customization. This new navigation allows for more screen real estate, improved UX, and overall and easier navigation experience.

**Limits**

The limits page has been completely reworked to clearly layout what limits apply to your community and overall a refresh to the existing UI.

**Integrations**

A new Integrations Portal has been introduced, this portal houses all integrations that Sonoran CMS offers. From official integrations to community driven integrations this is the one place to manage it all. With more comprehensive integrations planned in the very near future.
{% endtab %}

{% tab title="Fixed" %}
**Community Profile**

* Unable to view user profiles if you're not logged in or apart of the community

**Website Pages**

* Privatized pages would not actually handle like they're privatized, essentially would behave as a public page

**Rosters**

* Some communities may have seen JSON data within their roster rows
{% endtab %}
{% endtabs %}

### v0.5.43 (Beta) 6/1/2023

{% tabs %}
{% tab title="New" %}
[**Website Builder** - **New Elements**](../tutorials/community-website/website-builder.md)

_Static Image Carousel_

Similar to the gallery element however members cannot upload or remove images through the UI, this element is set for the page.

_Card_

The card element can display various information and can be customized to your exact liking!

_Circular Progress (Info Block Style)_

Circular progress has been added as a style type for the **Info Block** element type, this provides a circular progress bar that can be customized to a specific value or based on total community or department members.

_HTML Embed_

HTML Embed allows more in-depth customization to your website pages, easily embed popular embeds from other sites such as TrackyServer!

[**Rank Manager**](broken-reference)

The ability to copy and paste permissions between ranks/departments has been re-implemented from being removed in the last update.

[**Toolbar**](../tutorials/community-website/website-builder.md#toolbar)

_Drive Document_

A new destination type has been added to the toolbar item options, you can now select a specific file in your CMS Drive to directly link to without the need of grabbing the physical URL to the file!
{% endtab %}

{% tab title="Changed" %}
[**Website Builder**](../tutorials/community-website/website-builder.md)

* Editing an element's sizing will change the current preview size shown within the editor.
* Removed excess spacing on the sides while viewing on a mobile sized screen.
* Pop-up editing of elements have been reworked and improved for a better user experience.

[**Forms Editor**](../tutorials/forms/creating-custom-forms.md)

* Utility Toolbar has been reworked and improved for a better user experience.

**Footer**

* Footer was updated to have more spacing and less cramming

**Pricing**

* The Sonoran CAD button now has the correct hyperlink destination

[**Direct Form URLs**](../tutorials/forms/)

When linking an individual a direct apply link to a form it would it just take them to the Available Forms and not display anything. Now it'll notify they must be signed in and will easily direct them to login and take them back to the same page once signed in.

[**Forums**](../tutorials/community-website/forum-system.md)

Forums no longer require individuals to be signed in to just view a category and forums element.
{% endtab %}

{% tab title="Fixed" %}
**Gallery**

* Gallery elements would not show/load properly if the individual is not signed in, the sign in requirement is now removed.
{% endtab %}
{% endtabs %}

### v0.5.42 (Beta) 5/25/2023

{% tabs %}
{% tab title="New" %}
[**Community Template**](broken-reference)

The Community Template feature has been removed for the time being, we've reworked the default template to be fully customized to easily see the full capabilities of the system and an easier customization transition. Newly created communities will now come with departments, rosters, pages, etc. fully customized to be used out of the box or customized further to fit your needs.

[**Forms Editor**](../tutorials/forms/creating-custom-forms.md)

The Forms Editor has been reworked to take after the ease of use and customization the Website Builder brings. The entire UI has been reworked and now includes the majority of customization capabilities of the Website Builder for forms.

[**Department Manager -> Rank Manager**](broken-reference)

The Department Manager has been reworked and renamed to Rank Manager. This rework has provided an easier and smoother experience when editing and managing ranks. From creating a department to managing rank permissions, the whole experience has been simplified and improved.&#x20;
{% endtab %}

{% tab title="Fixed" %}
**Community Discovery**

* Fixed an issue where the images would appear very small compared to the actual size that should have been shown.

**Custom Forms**

* Member selectors would not have any options to select from despite having members that should be populated.

**Ranks**

* Inherited permissions from the parent department would not be accounted for.

**Desktop Application**

* Top toolbar would overlap with the top window bar.

**Website Builder**

* New page elements wouldn't be able to dragged and dropped into an empty area, they would only appear if dropped onto an existing section.
{% endtab %}
{% endtabs %}

### v0.5.41 (Beta) 5/17/2023

{% tabs %}
{% tab title="New" %}
[**Pricing & Subscriptions**](broken-reference)

We're making Sonoran CMS more accessible than ever before, with all functionality for **FREE**!

View our [notice](broken-reference) for more information.

[**Website Builder**](../tutorials/community-website/website-builder.md)

Background images now have different handling to better allow more customization on how they view, you can now change how the image shows across the background.
{% endtab %}

{% tab title="Changed" %}
[**Website Builder**](../tutorials/community-website/website-builder.md)

Side toolbar is now scrollable

Page slug input no longer shows the preview and is replaced with a copy button

Grid lines in the previewer are no longer there

**Account Management**

When editing an individual account there will no longer be an option to change between active & pending, setting an individual to no ranks will place them in pending and setting them with any ranks will place them in active.
{% endtab %}
{% endtabs %}

### v0.5.40 (Beta) 5/15/2023

{% tabs %}
{% tab title="New" %}
[**Custom Forms**](../tutorials/forms/creating-custom-forms.md)

Custom Forms now have new element type, uploader. This accepts images and PDFs but is configurable per element. Easily have your users upload images or PDFs to be viewable directly within the submission.

[**Profile Fields**](../tutorials/customization/community-profile-fields.md)

Two new profile field types have been added, Discord and TeamSpeak. These two types are apart of the new _verified_ profile types. These will be automatically grabbed from the account without any user interaction or input.

[**Toolbar Editing**](../tutorials/community-website/website-builder.md#toolbar)

The toolbar editor has been moved from Customization to the Website Builder.

Additionally the toolbar now supports background color, individual font and text-color customization, and easy drag and drop support. You can now rearrange your toolbar including the community image easily to how you desire.&#x20;

[**TeamSpeak 3 Sync**](../integration-capabilities/teamspeak-3-role-sync/)

You can now sync your Sonoran CMS ranks directly to your TeamSpeak 3 server's groups! This will automatically add/remove TS server groups from individuals that are configured to be set with their associated ranks.
{% endtab %}

{% tab title="Changed" %}
**Custom Page Backgrounds**

Custom page backgrounds now extend to the entire body of the page instead of the custom page container.
{% endtab %}
{% endtabs %}

### v0.5.39 (Beta) 5/4/2023

{% tabs %}
{% tab title="New" %}
[**Website Builder**](../tutorials/community-website/website-builder.md)

The existing Custom Page Editor has been rebranded to the Website Builder.

Background image and color is now able to be applied to the entire page as well as the existing section and element background options.

Side left toolbox was added to larger screen sizes to easily drag and drop elements onto the page, as well modify page background options.

Button elements have been expanded to include further customization such as text color, image icon, and several edge stylings.

Content elements can now modify the color and font of the content in the WYSIWYG editor.

**Discord Clock In/Out**

You can now clock in/out directly through Discord with the addition of the following commands:

* `/clockincms`
* `/clockoutcms`
{% endtab %}

{% tab title="Changed" %}
**Icon / Image Selector**

All areas where an icon would be expected to be supplied it has been reworked to allow for icon & image with the icon selector allowing to be searched within the field.
{% endtab %}
{% endtabs %}

### v0.5.38 (Beta) 4/28/2023

{% tabs %}
{% tab title="New" %}
[**Custom Page Editor**](../tutorials/community-website/website-builder.md)

The Custom Page Editor has been thoroughly reworked to allow for more styling specifically to sections and elements within sections. With this rework we've revamped the structures of pages and all existing pages have been migrated over to the new page system. Pages are now constructed of individual sections which house elements. All existing pages were updated to move all pre-existing sections into one section and converted to elements. Now customize the padding, margin, alignment, etc. of sections, we've also included background color and images to sections and elements!

[**Discovery Page UI**](broken-reference)

The Community Discovery Page UI has been reworked to better advertise and showcase the communities that use Sonoran CMS!
{% endtab %}

{% tab title="Changed" %}
**Account Dropdown**

Items within the Account dropdown have been reordered to categorize where needed.

**Community Image (Top Left in Toolbar)**

Clicking the top left community image will now redirect to the Dashboard instead of leaving the community and navigating to _My Communities_.
{% endtab %}

{% tab title="Fixed" %}
**Custom Forms**

Forms could not be submitted from _Available Forms_ or directly linked, this issue was resolved on web shortly after v0.5.37 release.
{% endtab %}
{% endtabs %}

### v0.5.37 (Beta) 4/21/2023

{% tabs %}
{% tab title="New" %}
[**Department Editor**](../tutorials/user-management/creating-departments.md#4.-customize-rank-cosmetic-styling)

The customization workflow for Department Rank's has been improved, you can now directly upload an image or choose from thousands of icons for your rank cosmetic icon.

[**Community Transfers**](../tutorials/administrative/delete-community.md#how-to-transferring-a-community)

Community Owner's can now transfer their community to anyone that's currently active within the community, the owner must complete a confirmation before the transfer is complete.

[**Custom Page Editor - UI**](../tutorials/community-website/website-builder.md)

The entire Custom Page Editor UI has been reworked to become more of a _website editor_ than a custom form editor. This new UI allows for easy sorting of sections by dragging and dropping and an overall better user experience. This new UI is one of many improvements we plan on bringing to Custom Pages.

[**Direct Form Submission Links**](../tutorials/forms/creating-custom-forms.md#sharing-direct-submission-access)

You can now share a direct link to a Custom Form to be submitted from, this should help with recruitment as it will take them straight to filling out the form. This URL can be found in the Custom Forms area prior to selecting a form to edit.

[**Discord Sync**](../integration-capabilities/discord-bot-integration.md)

Discord Sync has now been made available to all Free communities using Sonoran CMS, regardless of Sonoran CMS community premium status.
{% endtab %}

{% tab title="Fixed" %}
**Form Management**

The top header would be oddly positioned and would have text be misaligned.
{% endtab %}
{% endtabs %}

### v0.5.36 (Beta) 4/17/2023

{% tabs %}
{% tab title="New" %}
[**Toolbar**](../tutorials/customization/community-branding-and-settings.md#toolbar)\
The existing side-menu that was positioned to the left of the Community pages was removed and migrated to the top toolbar. Now all navigation goes through the top navigation bar, allowing full customization for how your navigation is designed and organized.

* **Clock In/Out** is now located between the Admin cog (if enabled & viewable) and the Notification Center icon located on the right side of the toolbar.
* All existing communities have been migrated with side-menu options being recreated for each community to allow for an easier transition into the new navigation system.
  * Drive, Available Forms, Form Management, etc. are now toolbar options for all existing communities from this update. Feel free to update your toolbar to remove these options if not desired.
* **Community Settings** to edit your API IDs, refresh CAD Sync, etc. has been moved to the top-right dropdown menu where you can navigate to Community Discovery, My Communities, etc.

[**CAD Sync**](../integration-capabilities/sonoran-cad-sync.md)\
CAD Sync has now been made available to all Free communities using Sonoran CMS, regardless of Sonoran CAD community premium status. Use the full capabilities of CAD Sync without needing a premium subscription.
{% endtab %}

{% tab title="Changed" %}
**Accounts Viewer**\
While viewing accounts through the Administrative Panel the accounts will now load more efficiently through the use of server-side pagination.

**Accounts Editing**\
The UI for editing accounts has been improved for a better UI/UX.

**Community Side Menu**\
Has been completely removed in favor for the toolbar navigation system.
{% endtab %}

{% tab title="Fixed" %}
**Discord Webhooks**\
Forum Topic Creation - Not sending with properly formatted webhook embed description.

**Managing Permissions**\
Editing a user's secondary ranks, either to add, remove, or edit would cause errors to throw invalidating any request to save.

**Gallery**\
Gallery permissions were not evaluated for the gallery uploading capabilities.

**Available Forms**\
Forms with the type of New Member Application were not showing for new members of communities.

**Form Management**\
Specific Form's would not all show in the Form Management filtering selector.
{% endtab %}
{% endtabs %}

### v0.5.35 (Beta) 4/7/2023

{% tabs %}
{% tab title="New" %}
[**Calendar** RSVP Limits](../tutorials/community-events.md#regarding-rsvp-limit)

Calendar events can now be RSVP limited, you can now set how many members can RSVP to an individual event.

**API Endpoints**

[**Event RSVP**](../developer-api-documentation/api-integration/api-endpoints/events/rsvp.md)

[**Drive** Downloads](../tutorials/your-drive-and-documents.md#drive-downloads)

Additional file types can now be uploaded and downloaded directly from the Sonoran CMS Drive. Any **.rpf**, **.wav**, **.mp3**, **.zip**, and **.pdf** are accepted. They aren't "viewable" but are able to be downloaded easily. Additionally there's now a download URL that can be copied for the _downloadable_ file types as described above.

[**Community Gallery**](../tutorials/community-website/gallery-system.md)

A new **Custom Page Element** has been added for additional customization and content. We've added the first of many elements apart of the new Gallery system. This system is designed heavily after the Forum system, as far as handling. Each element requires it to be associated to a _Gallery category_, with further customization and elements coming in later updates. This new element will show your images in a larger slide show with also listing all the gallery posts associated to the category. These gallery categories can be restricted as far as who can upload.
{% endtab %}

{% tab title="Changed" %}
**Member Join**

All new users that joined communities would have their community name set to "NOT SET" upon initial join, this however has been changed to set their community name as their Sonoran account username.

**Community Profile**

The community profile now shows all ranks that the user has associated.

**Several UI Improvements**

Mobile UI/UX has been improved in several areas to better adapt to smaller screens.
{% endtab %}
{% endtabs %}

### v0.5.34 (Beta) 3/24/2023

{% tabs %}
{% tab title="New" %}
[**Archive Community Member**](../tutorials/administrative/archive-community-member.md)

Community member's can now be archived, this is _kick_ from the community but sets the member in a archived state where their profile and information is still accessible. This should allow communities to better organize member's that have left and will allow you to easily see their information by viewing their profile even after they're gone.

* When an account is archived it will display a banner on their profile showing they're archived.
  * Additionally if they're banned it will also display a banner.
* When an account is archived it will display a small banner on their brief profile information when viewing a Forum Topic.

**Custom Profile Fields**

[_Text Array Profile Field Type_](../tutorials/customization/community-profile-fields.md#text-array-profile-field-editing)\
A new profile field type has been added; Text Array. This new field type allows you to store several entries of information on one specific field.

**API Endpoints**

[**Get Profile Fields Endpoint**](../developer-api-documentation/api-integration/api-endpoints/general/get-departments-1.md)

[**Edit Account Profile Fields Endpoint**](../developer-api-documentation/api-integration/api-endpoints/general/ban-account-1.md)
{% endtab %}

{% tab title="Changed" %}
**Roster**

When viewing a roster and clicking on a row it will now not immediately edit the row, it will now give you the option to edit the row or to view their community profile.

**Community Profile**

Several UI elements of the Community Profile have been changed to improve the overall UI/UX.
{% endtab %}

{% tab title="Fixed" %}
**Community Profile**

Clicking on a user profile's name text will warn about not being able to edit it.

**Mobile UI**

_Hamburger Menu_

The hamburger menu would keep state from a previous community and not refresh upon loading a new community.

**Custom Page Editor**

The default page button would be clickable even if the page is already set to default.

**Custom Form Editor**

Adding new fields could randomly be placed in a different section than the intended one.
{% endtab %}
{% endtabs %}

### v0.5.33 (Beta) 3/17/2023

{% tabs %}
{% tab title="New" %}
**Mobile UI**\
&#xNAN;_&#x53;ide Menu & Hamburger Menu while Signed into a Community_\
The hamburger menu when shown on mobile has been reworked to introduce the existing menu that listed all community area such as Administrative Panel, Form Management, etc. The main side menu will now longer show on mobile view and will be included in the hamburger menu.

_Forum Topic Page_\
When viewing a forum topic on a smaller screen the replies and user information will no longer become disoriented and unviewable.

**Forum Topics**

Replies on forum topics now allow you to include attachments with the reply similar to creating a topic.

**Form Stages**

Form stages have now two labels. The _Stage Label_ should be seen as a public name for the label, this will be shown in Available Forms, Form Management, and when referenced in stage actions (when they execute). The _Internal Label_ should be seen as a _nickname_ for the stage, this will be shown in any area it's referenced in the Administrative Panel area.

**Community Profile**

_Community Bio_\
A community bio option has been added to the community profile page. Members can now set a customizable bio for themselves directly in their profile.

_Name Changing_

Individuals viewing another member's profile and having permission to edit them within the Account Viewer will be able to change the member's name directly in the profile.

_Account Avatar_

Individuals viewing their own community profile will be able to change their account avatar by simply clicking on their avatar in the profile page.

_Global Account Actions_\
Several account action buttons have been added to the community profile page, these will only show when viewing your own profile. This is in place due to the change with how the top-right dropdown menu is handled and the options that are now displayed there.
{% endtab %}

{% tab title="Changed" %}
**Account / Top Account Dropdown**

The non-community account page is now no longer accessible by the top dropdown when viewing a community. This will now direct you to your Community Profile which also provides the same global account action buttons that are in the non-community account page. The dropdown item _Account_ was renamed to _Profile_ to adapt to this change.
{% endtab %}

{% tab title="Fixed" %}
**Department Editor**

After adding a calendar category and going to the department editor it would not show up until a refresh or a relog into the community.

**Account Viewer**

When editing an account and removing the primary rank it would not remove the primary department shown in the account viewer table.

**Stage Actions**

After creating a stage with a _Change Submitter's Department/Rank_ action, the action would not provide all department ranks after editing it upon creation.

**Integration - Whitelist**

Several bugs have been pushed to address issues related to the whitelist system.

**Custom Form Editor**

Premade form sections were removed during the rework of the Custom Forms & Stages. They've been reimplemented with no additional sections added, just the Patrol Start/End.
{% endtab %}
{% endtabs %}

### v0.5.32 (Beta) 3/9/2023

{% tabs %}
{% tab title="New" %}
**Expiring Ranks**

Ranks can now be applied to [individuals manually](../tutorials/user-management/modify-users-permissions-and-information.md#granting-expiring-ranks) or through [stage actions](../tutorials/forms/creating-custom-forms.md#action-explanation-change-submitters-department-rank) to set a rank to expire, the rank will automatically be removed upon the next check (every fetch for the account) if found expired. Ranks can be set to expire after X amount of hours/days or by a exact time/day that you set.

**Account Avatars**

Customizable account avatars have now been implemented, all areas within the Sonoran CMS should now support the customizable avatar. You can now set your avatar [here](https://account.sonoransoftware.com/).

[**Discord Webhooks**](../integration-capabilities/discord-webhooks.md)

A new webhook event has been added, **Member Join**. This webhook will fire when a member joins your Sonoran CMS community.

**Forum Topic's**

Forum topic attachments now support opening in a image viewer instead of downloading the image. Zoom, pan, etc.

**Account Editing**

Account editing UI has been slightly reworked to adapt to the new Expiring Ranks. Users will no longer need to select a department prior to assigning a rank.
{% endtab %}

{% tab title="Fixed" %}
**Available Forms**

* Share link would appear on non-submitted forms
* Form ID "#" would appear on non-submitted forms
* Able to view all and any forms regardless of permission
* State would not update with newly edited/created forms

**Rosters**

* Automatic Department Rosters would unreliably get backend generated rows
* Rows be able to be initially edited without proper permission
  * Request to edit the row would not process through without valid permissions

**Discord Webhooks**

* Forms submitted directly onto a profile would not send a logging webhook
{% endtab %}
{% endtabs %}

### v0.5.31 (Beta) 3/2/2023

{% tabs %}
{% tab title="New" %}
[**Custom Page Paths**](../tutorials/community-website/website-builder.md#custom-page-paths)

Custom pages can now have a custom path slug to further customize your pages. These path slugs will replace the number ID that is given by default for all custom pages. These paths support custom domains, example: `lspd/sop` would append to a custom domain such as `cms.sonoranrp.com/lspd/sop`.

[**Custom Form Folders**](../tutorials/forms/creating-custom-forms.md#custom-form-folders)

Custom Forms can now be organized within folders, folders are simply for organizational purposes and serve no additional purposes.

**Home Page**

Our home page has been reworked to provide a more user-friendly and informational landing page.

**API Endpoints**

[**Kick Endpoint**](../developer-api-documentation/api-integration/api-endpoints/general/kick-account.md)

[**Ban Endpoint**](../developer-api-documentation/api-integration/api-endpoints/general/ban-account.md)

**API Integration**

Copy buttons have been added to the `Community ID` and `API Key` fields.

**Discord Webhooks**

Custom Form webhooks have been updated to hyperlink the forms share link to the embed's URL.
{% endtab %}

{% tab title="Changed" %}
**Rosters**

Automatic Department Roster's have been reworked to improve reliability and performance regarding row generation and response.
{% endtab %}
{% endtabs %}

### v0.5.30 (Beta) 2/23/2023

{% tabs %}
{% tab title="New" %}
[**Automatic Rosters**](../tutorials/user-management/creating-custom-rosters.md#department-automatic)

Rosters have been reworked to add additional functionality and purpose. All existing rosters have been moved to the type of "Custom", this type is considered for all rosters that will allow you to add and remove rows as you please. With this change the previous _Department_ and _Sub-Department_ type have been deprecated.\
\
A new roster type, Department, was added to replace the previous _Department_ roster type. This new roster type is considered automatic meaning rows will be dynamically created based on all members that hold a rank within the specified department. Members will be sorted in the order which their rank within the department is shown, as well as alphabetically.
{% endtab %}

{% tab title="Fixed" %}
**Form Management**

Filtering forms to show only **Deleted Forms** would show no forms despite fetching all deleted forms.

[**Custom Forms**](../tutorials/forms/creating-custom-forms.md)

An internal ID was not setting correctly upon save which would make the form no longer editable or usable.

**Menu Items**

Menu items would not correctly evaluate permissions.
{% endtab %}
{% endtabs %}

### v0.5.29 (Beta) 2/17/2023

{% tabs %}
{% tab title="New" %}
[**Form Submission Limits**](../tutorials/forms/creating-custom-forms.md#limiting-form-submissions)

Custom Form Templates now have limit settings, these settings will allow you to customize how your forms are being submitted. This allows for submissions to be limited to a certain amount per user, within the last X days, and even with a cooldown between submissions.

* Limit Total Submissions from each User
  * Ignore submissions that are set to a stage with the type of "Archived"
* Submission Cooldown
* Limit Within Last X Days

[**Department Rank Cosmetic Customization**](../tutorials/user-management/creating-departments.md#4.-customize-rank-cosmetic-styling)

Department ranks now have cosmetic styling, this cosmetic addition is only shown when viewing Forum Topic's but will be expanded upon as UI is needed. This customization allows you to change the background color and icon associated with it.

**Custom Form & Stage Editors**

Custom Form, Custom Stage and Custom Stage Group editor's have all been centralized into one page and one editor. Create stages directly within forms without the hassle of creating groups to then go back and fourth within editors.

**Additional Form Management Filters**

Several new form management filters have been added to better find submissions within your community. Now you're able to use the following filters when managing forms:

* Community Member
* Form Type
  * Was already implemented prior but was improved/fixed as well
* Custom Form
  * Search for submissions that were all created from the same custom form template
    * Additionally you can specify whether you want to filter the custom form submissions by their current stage as well
{% endtab %}

{% tab title="Fixed" %}
Custom Page Editor

* When enabling sorting for page sections you'll only be displayed with a maximum of 5 sections even if you have more.

Account Info

* Saving an edited account would fail and not provide an error.
{% endtab %}
{% endtabs %}

### v0.5.28 (Beta) 2/9/2023

{% tabs %}
{% tab title="New" %}
[Forum System](../tutorials/community-website/forum-system.md)

The user interface for the Forum System has been completely revamped, improving the individual topic viewing and forum categories pages.

* Quote Replying
  * There's now an option under a topic or a topic reply will have an option to quote the content of that, this will add the content to your reply editor to allow you to easily quote an individual's post.
{% endtab %}

{% tab title="Fixed" %}
Community Discovery

* "Load More" button located on the Community Discovery page would not load additional communities

Community Profile

* When viewing a profile that's now your own the name of the profile would display "ERROR"

Rosters

* Saving a roster row without changing the user's status would cause their status to remove and go back to unset/errored
* Websocket Disconnections
  * Permissions checks when gathering all rows would cause a WS disconnection due to a failure in the check

Account Viewer Table

* Sorting accounts by the table column labels would not sort properly, they would be randomly sorted and not with the correct sort applied
{% endtab %}
{% endtabs %}

### v0.5.27 (Beta) 2/2/2023

{% tabs %}
{% tab title="New" %}
[Custom Login Page](../tutorials/customization/custom-domain.md#custom-login-page)

The custom login page has been completely revamped, the old login page has been deprecated and have been moved to the top toolbar & community dashboards.

* When using a Custom Domain it'll automatically load the community's dashboard page.
* If you're not signed in or not apart of the community you'll be put in a "Preview" mode for the community while you view their dashboard and custom pages.
* Deprecated login page may still be seen as there's some actions that require a login page to direct to.
{% endtab %}

{% tab title="Fixed" %}
[Discord Webhooks](../integration-capabilities/discord-webhooks.md)

* Account Updated webhook would not show the correct ranks/departments the account is associated with.
* Event webhooks would include raw HTML within the event description.
* Tutorial button on Discord Webhook page now directs you to the guide.
* Event webhooks would not include any specified content and would always be content-less with the embed.
{% endtab %}
{% endtabs %}

### v0.5.26 (Beta) 1/26/2023

{% tabs %}
{% tab title="New" %}
[Dashboard](../tutorials/community-website/website-builder.md#default-dashboard-page)

The community Dashboard / Landing page has been completely reworked, this now allows for the full customization of the Custom Page Editor. Set any existing custom page as your community's dashboard page.

[Custom Page Editor](../tutorials/community-website/website-builder.md#page-editing)

* New Page Section Type
  * Information Block
    * This allows for multiple blocks of information to be added to your page, each block allows for two customizable text options. This also allows you to dynamically populate the block with "Total Community Members" or "Total Department Members".
* UI Improvements
  * Several aspects of the Custom Page Editor UI was reworked and improved.
* Page Reordering
  * Page reordering is now handled through drag and drops actions instead of direction buttons.
* Page Section Reordering
  * Page section reordering is now handled through drag and drops actions instead of direction buttons.
* Default / Landing Page Toggle
  * Set a Custom Page as the community's Dashboard / Landing Page.
{% endtab %}

{% tab title="Fixed" %}
Network

* Handling for WS communication was changed to fix edge-cases with random disconnects.

Admin Routes

* Accounts table within the Administrative Panel would populate despite having permission to view any admin pages.
{% endtab %}
{% endtabs %}



### v0.5.25 (Beta) 1/24/2023

{% tabs %}
{% tab title="New" %}
[Sonoran CAD Integration](../integration-capabilities/sonoran-cad-sync.md#feature-overview)

* **Multi-Setup Sync**

Sync your single Sonoran CMS community to multiple Sonoran CAD communities!

[Navigation Button Visibility](../tutorials/community-website/navigation-sidebar.md)

Navigation items on the sidebar can now be dynamically shown based upon permissions. Documentation explains how each navigation item is permission evaluated.

[Privatized Pages](../tutorials/community-website/website-builder.md#privatized-pages)

Pages can now be privatized and require permissions to view, this view type can be changed in the page editor.

[Available Forms UI](https://cdn.discordapp.com/attachments/859199158568615986/1065772905251737610/8tf7hUj.png)

The _Available Forms_ area is now in a grid UI.
{% endtab %}

{% tab title="Fixed" %}
[Whitelist API](../developer-api-documentation/api-integration/api-endpoints/servers/verify-whitelist.md)

Reponses have been fixed to be consistent and adjusted to provide reliablity to the in-game resource(s).
{% endtab %}

{% tab title="Changed" %}
[Sonoran CAD Integration](../integration-capabilities/sonoran-cad-sync.md#feature-overview)

* Individual Manual Sync
  * CAD Sync button located in the Account Settings dialog

Member's can now manually sync their Sonoran CMS account with the linked Sonoran CAD community, this will now sync all aspects of the account besides just permissions.
{% endtab %}
{% endtabs %}

### v0.5.24 (Beta) 1/12/2023

{% tabs %}
{% tab title="New" %}
[Sonoran CAD Integration](../integration-capabilities/sonoran-cad-sync.md#feature-overview)

* **API ID Sync**

Sync member's API IDs to the same user from your Sonoran CAD community, if they have a Discord account linked to their account it will sync that ID as well.

* **Auto Join CAD**

All new members that join your community automatically join your Sonoran CAD community under the same user ID.

[Member Join Customization](../tutorials/customization/community-branding-and-settings.md#member-on-join-settings)

Through the newly added "Member On Join Settings" you can customize whether members join with "ACTIVE" status, if "ACTIVE" is selected you can customize a rank which they'll be automatically granted.
{% endtab %}

{% tab title="Fixed" %}
[Custom Forms](../tutorials/forms/creating-custom-forms.md)

* Forms submitted would not be able to be replied to by the author of the form
* Forms would not be able to be submitted at all

Department Permissions

* Secondary rank permissions would not be evaluated correctly with roster related permission checks
{% endtab %}
{% endtabs %}

### v0.5.23 (Beta) 1/9/2023

{% tabs %}
{% tab title="New" %}
[Discord Webhooks](../integration-capabilities/discord-webhooks.md)

* A new webhook option was added for when submitted forms get their stage changed, a new webhook option is added solely for this event.

[Page Re-ordering](../tutorials/community-website/website-builder.md#sorting-pages)

* The ability to sort the position of the pages in which they appear in lists.

[Form Re-ordering](../tutorials/forms/creating-custom-forms.md#sorting-forms)

* The ability to sort the position of the forms in which they appear in Available Forms.

[Conditional Custom Form Sections](../tutorials/forms/creating-custom-forms.md#conditional-sections)

* Dynamically show sections within your custom forms based upon conditions set that require to be met with the specified field.

[Member Customization](../tutorials/customization/community-branding-and-settings.md#community-name-customization)

* Allow members to customize their community name's, this setting is community wide.
{% endtab %}

{% tab title="Fixed" %}
User Management

* Users would not be able to unban any individual within their community's ban list.

Rosters

* Patrol log hours would miscalculate based on the forms that were submitted on-behalf of the account, on-behalf of another account, and regular submissions.
{% endtab %}
{% endtabs %}

### v0.5.22 (Beta) 1/3/2023

{% tabs %}
{% tab title="Fixed" %}
[Discord Webhooks](../integration-capabilities/discord-webhooks.md)

* Webhook preference would appear to not be "saved" when switching pages, data was not updated locally upon backend change.

Rosters

* When adding a roster row the previous chosen sort power would be brought to the next row you create.
* Unable to view rosters after attempting to navigate from side smaller UI.

Forums

* Creating a public forum topic would cause errors.

Permission Evaluation

* Permission evaluation would not be completely considered upon specific page loads (Admin, Form Management, etc.)

Stage Actions

* Email stage actions would show the button included in the email as "{button}"
{% endtab %}

{% tab title="Changed" %}
Forms

* When submitting a form under another individual's profile it will warn you regarding the form being submitted by the submitter and not the profile it's being submitted under.
{% endtab %}
{% endtabs %}

### v0.5.21 (Beta) 12/21/2022

{% tabs %}
{% tab title="New" %}
[Forum System](../tutorials/community-website/forum-system.md)

Several new changes have been added to the forum system;

* [Sub-Categories](../tutorials/community-website/forum-system.md#creating-forum-sub-categories)
* [Topic Attachments](../tutorials/community-website/forum-system.md#topic-creation-forum-topic-attachments)
* [Private Topics](../tutorials/community-website/forum-system.md#creating-private-topics)
* Discord Webhooks
  * A new section has been added to the Discord Logging Webhook editor, Forums. This allows webhooks to be executed on Topic Creation & Reply Creation.

Migration System

A new database and system migration system has been implemented to ease any updates to the entire system or the database, this will allow usage of the platform when updates are in progress. If a community has not yet been migrated from an update the community will be unusable until the community has completed it's migration.
{% endtab %}

{% tab title="Fixed" %}
Community Creation

* Creating a community would be unreliable and not create the community

Discord Webhook Logging Editor

* Fixed the reliability of Discord Webhook logging data to be consistent to what the data standard is

Community Toolbar

* Header links with the community toolbar would only show on the "Dashboard" page
{% endtab %}
{% endtabs %}

### v0.5.20 (Beta) 12/12/2022

{% tabs %}
{% tab title="New" %}
[Forum System](../tutorials/community-website/forum-system.md)

Several new changes have been added to the forum system;

* [Dedicated Forum Category Page](../tutorials/community-website/forum-system.md#dedicated-forum-category-page)
* [Topic Pinning & Locking](../tutorials/community-website/forum-system.md#topic-actions-pin-and-lock)
* Improved UI
  * Forum Category Topics Table
  * Usernames within the Forum System will show with community name and identifier format as well as their primary rank if assigned
  * Several other UI improvements
* Topic Reply Editing
  * You can now edit your own topic replies
{% endtab %}

{% tab title="Fixed" %}
Discord Webhooks

* Webhook settings would not save depending on various authentication variables

Department Editor

* Department Default Permissions would cause the editor to be unusable and causing data to not be saved if certain conditions were met

Custom Forms

* Saving a edited submitted form would not complete and would just cause the client to hang without any notification or error
{% endtab %}

{% tab title="Changed" %}
[Forum System](../tutorials/community-website/forum-system.md)

**Delete Topics** permission section for forum category's has been moved to **Manage Topics** allowing that same permission section to handle topic deletion, pinning and locking.\
**Delete Topics -> Manage Topics**
{% endtab %}
{% endtabs %}

### v0.5.19 (Beta) 12/6/2022

{% tabs %}
{% tab title="New" %}
[Forum System](../tutorials/community-website/forum-system.md)

A new Forum System has been implemented; allows communities to create categories that can be used across multiple or individual custom pages in the form of a custom page section. Each category can have topics created within them, each topic can be removed and replied to. Permissions to create and manage topics/replies is handled by the forum category.
{% endtab %}

{% tab title="Fixed" %}
Form Stage Actions

* Using both the "Modify Submitter's Community Status" and "Change Submitter's Department/Rank" stage actions on the same stage would cause data to be overwritten when each of them would execute.

Drive

* Permissions viewing drive files would cause the data returned to be inconsistent with the data that should be returned.

Community Creation with Templates

* Creating a community from a template that's data would cause the community to be over limits would cause none of the template to apply.

Rosters

* Viewing a roster would cause none of the roster data rows to populate.

Accounts Viewer

* When viewing all of the user accounts in the community and changing the status filter to **BANNED** would not populate the user accounts table with the correct users.
{% endtab %}
{% endtabs %}

### v0.5.18 (Beta) 11/17/2022

{% tabs %}
{% tab title="New" %}
[Community Customization](../tutorials/customization/community-branding-and-settings.md)

* Cosmetic
  * You can now add a community "banner" image, currently this banner image only displays with the notification message sent with bumping your community for discovery.

[Community Discovery](broken-reference)

* Bumping
  * Bumping your community will now include your community's banner image upon bump. If no banner image is set it won't include any image.

[Custom Pages](../tutorials/community-website/website-builder.md)

* Page Elements
  * Two new page elements have been added, `Button` and `Button Group`. Both these elements can be added to any custom page. Each button's functionality and style can be configured to fit your needs. Buttons can target to a external website, custom form and custom page.
{% endtab %}

{% tab title="Fixed" %}
[Community Discovery](broken-reference)

* Clicking community cards to open up the community modal would not be possible unless you click the image or text on the card. The whole card should be clickable.
* Clicking a community card would display a modal with additional community information and options to join, this would not include the image.
{% endtab %}

{% tab title="Changed" %}
[Department Manager](broken-reference)

* Performance
  * Several improvements have been implemented to decrease any issues with performance regarding permission management of departments.
{% endtab %}
{% endtabs %}

### v0.5.17 (Beta) 11/14/2022

{% tabs %}
{% tab title="Fixed" %}
[Community Drive](../tutorials/your-drive-and-documents.md)

* Editing Files
  * An issue which would cause files to not be edited within the member editing page but would still allow edits through the public-sided edit file page.

[Discord Webhook Logging](../integration-capabilities/discord-webhooks.md)

* Editor
  * An issue which would cause the webhook input editor to not load fully or at all.
* Webhooks Executing
  * An issue which would causing the Calendar Creation webhook to not execute at all.

[Community Discovery](broken-reference)

* Bump System
  * An issue which would cause the Discord advertisement webhook message to include various programmatic types within the message such as '\[object Object]' & 'undefined'.

[Community Member Profile](../tutorials/customization/community-profile-fields.md)

* Forms
  * An issue which would cause individuals to be unable to submit forms directly onto another user's profile to attach it to their profile.

[Rosters](../tutorials/user-management/creating-custom-rosters.md)

* Column Types
  * Community Identifier row columns would not populate with a user's primary identifier properly unless the conditions which very specific.

[Custom Stage Form Actions](broken-reference)

* Status Modifier
  * An issue which would cause the stage action to change community status to not execute properly unless the individual was active within the community from the start.
{% endtab %}

{% tab title="Changed" %}
[Community Discovery](broken-reference)

* User Interface
  * Equal sizing has been applied to all community discovery cards
  * Each community has been moved to a dedicated modal upon click to provide additional information prior to the community

Application User Interface

* Various aspects of the Sonoran CMS has seen UI improvements
{% endtab %}
{% endtabs %}

### v0.5.16 (Beta) 11/7/2022

{% tabs %}
{% tab title="New" %}
[Community Discovery](broken-reference)

* [Bump System](broken-reference)
  * Allows your community to be bumped to the top of the Community Discovery list.
    * &#x20;Every **20 hours**!
    * Bumping will automatically advertise your community to the thousands of users in the Sonoran Software Systems LLC's Official Discord!
* Tags Categorization
  * Categorization your community with up to **5** predefined tags!
    * Select up to **3** tags with Sonoran CMS Free - Plus
    * Select up to **5** tags with Sonoran CMS Pro / Sonoran One
{% endtab %}
{% endtabs %}

### v0.5.15 (Beta) 11/3/2022

{% tabs %}
{% tab title="New" %}
[Community Discovery](broken-reference)

The Community Discovery Portal brings more members to communities by streamlining the joining process for your community. Joining a community through the discovery portal will automatically prompt them with the community's new member application. Advertise your community to the thousands of users using Sonoran CMS!

[Default Department Permissions](broken-reference)

Default Department Permissions applies the same set of permissions to all ranks within the department to easily manage permissions.

[Admin Form Delete](broken-reference)

Easily remove form submissions from y our community with the newly added "Admin Form Delete". This will remove the form from any data selection, this will now be accounted for when calculating patrol log hours, submissions, etc.
{% endtab %}

{% tab title="Fixed" %}
Community Deletion

* Communities were unable to be deleted, they will now process the deletion request properly.
{% endtab %}
{% endtabs %}

### v0.5.14 (Beta) 10/26/2022

{% tabs %}
{% tab title="New" %}
[Community Profile Fields](../tutorials/customization/community-profile-fields.md)

Profile Fields allow communities to put direct information onto member's profiles that can be restricted to certain viewers, editors, etc. with rank permissions. Profile Fields are dynamically on profiles depending on what ranks the profile you're viewing holds.
{% endtab %}

{% tab title="Fixed" %}
Department Editor

* Duplicating departments would not regenerate the IDs associated with the ranks in the new department which would cause the same ID to be associated by more than one rank.

Community Profile

* Submitting forms directly onto a member's profile would cause nothing to happen, it now will process through and allow you to let the profile "owner" to be able to see the form on their profile.
{% endtab %}
{% endtabs %}

### v0.5.13 (Beta) 10/17/2022

{% tabs %}
{% tab title="New" %}
[Drive](../tutorials/your-drive-and-documents.md#folders)

* [Publicly Accessible Files](../tutorials/your-drive-and-documents.md#publicly-accessible-files)
  * Files can now be accessible by anyone on the internet by a share link.
  * A new "General Access" option has been added, "Anyone with this link".
  * This will allow anyone to view and/or edit the file through the link given from the "Copy Link" button on the Share Settings dialog.

[Custom Form Stages](broken-reference)

* Custom Action: Modify Submitter's Community Status
  * This new action will do any of the following upon a form changing to a stage with this action:
    * Set Submitter to Pending
    * Set Submitter to Active
    * Kick Submitter from Community
    * Ban Submitter from Community
{% endtab %}

{% tab title="Fixed" %}
Billing

* Fixed an issue that would cause subscriptions to not update on the backend.

Rosters

* Fixed an issue where editing a secondary row would cause ranks to not populate in the dropdowns properly.

Toolbar

* Fixed an issue where the toolbar would not show on custom domains.
{% endtab %}
{% endtabs %}

### v0.5.12 (Beta) 9/29/2022

{% tabs %}
{% tab title="New" %}
[Drive Enhancements](../tutorials/your-drive-and-documents.md#folders)

* [Share Settings Overhaul](../tutorials/your-drive-and-documents.md#share-settings)
  * The Share Settings for each drive item has been overhauled, this shows all ranks that have access and some general share types.
  * There's now a "Ranks with Access Permissions", this will allow all listed ranks to have either edit or view access. This will grant them access regardless of what General Access is set to. This also has a "Inherit Parent Folder Access Permissions" option, this will only show for non-root items and this will inherit the parent folder's access permissions to determine with the drive items existing access permissions.
  * There's now several General Access types:
    * Restricted - Only utilizes "Ranks with All Drive Access" and "Ranks with Access Permissions"
    * Active members with this link - Allows all users that are active within your community to access the drive item, you can also control if they see the drive item in their drive or if they can only access through the share link.
    * Active & pending members with this link - Allows all users within your community to access the drive item, you can also control if they see the drive item in their drive or if they can only access through the share link.
    * Inherit Parent Folder General Access - This will inherit one of the above options depending on what the parent folder is currently set to.
  * The following are the now deprecated share types each drive item had and how they were migrated to the new settings:
    * PRIVATE
      * All drive items with this share type was migrated to **Restricted** General Access share type.
    * UNLISTED
      * All drive items with this share type was migrated to **Active members with this link** General Access share type with it hidden in the drive.
    * PUBLIC
      * All drive items with this share type was migrated to **Active & pending members with this link** General Access share type with it showing in the drive.
    * INHERIT\_FOLDER
      * All drive items with this share type was migrated to **Inherit Parent Folder General Access** General Access share type.
* Right Click Context Menu
  * The right click context menu is now accessible by clicking the green hamburger button.

Dashboard URL Handling

* Individual Rosters & Individual sections of the Admin Panel are now direct linkable, you can now copy the link and go directly back to where you were with that link.
{% endtab %}

{% tab title="Fixed" %}
Drive Uploading

* When uploading to a folder it will now upload directly into the folder instead of putting it directly into the root

Form Management

* WebSocket Error would cause the Form Management panel to be unusable
* Pagination restricted to only see the first initial 20 forms received from the request, it would not update the pagination settings to get more than what it already got
{% endtab %}

{% tab title="Changed" %}
Drive Uploading

* ZIP Uploading will set General Access share type to **Inherit Parent Folder General AccessDa**
{% endtab %}
{% endtabs %}

### v0.5.11 (Beta) 9/19/2022

{% tabs %}
{% tab title="New" %}
[Drive Folder Permissions Expansion](../tutorials/your-drive-and-documents.md#folders)

* Folders can now have their own Share Type & Permissions associated with them.
  * Right click a folder to manage.
* A new Share Type was added to Drive items, you can now set items to the Share Type of "Inherit Parent Folder" which will inherit Share Type & Permissions associated with the folder.
{% endtab %}

{% tab title="Fixed" %}
Available Forms

* Forms available to submit based on associated permissions would not populate the table
* Submitting forms would cause infinite loading or appear to be frozen&#x20;

Form Management

* Submitted forms based on associated permissions would not populate the table

Custom Form

* Auto member fields would not populate with the source data

Rosters

* Roster patrol log columns would not calculate hours and would only be "N/A"

Profiles

* Attempting to view a profile that's not yours would direct to your own profile

Account Viewer

* Filtering accounts by "BANNED" would result in an empty table instead of showing all banned users
{% endtab %}
{% endtabs %}

### v0.5.10 (Beta) 9/8/2022

{% tabs %}
{% tab title="New" %}
[Discord Role Sync](../integration-capabilities/discord-bot-integration.md)

* A system was introduced to handle Discord Role Sync upon the release of the Sonoran Bot's newest update
* This will allow bi-directional syncing
  * CMS <-> Discord
* Utilizes your Sonoran Account Discord Link
  * Does not handle API ID's of Discord ID's, it will only search and grab the Discord account linked to your Sonoran Account

[API Endpoints](../developer-api-documentation/api-integration/api-endpoints/)

* `GET_DEPARTMENTS`
* `SET_ACCOUNT_RANKS`
{% endtab %}

{% tab title="Fixed" %}
Department Editor

* Department creation would remove the department label

Rosters

* Rows not populating due to how data was formatted

Drive

* Drive UI not populating with the correct folders

Stage Editor

* Stages & Stage Groups were not saving in the state causing confusion of what is saved

Form Management

* Filtering would break the page and would require a refresh, the search functionality was disabled at this time while we re-work the search function

Toolbar

* Toolbar should only be showing while viewing a community

Notifications

* Notifications should be getting received in real time instead of on each refresh

Menu

* Community cards will now show the title & subtitle instead of title & description

WS Stability

* Several WS event listeners on the client side have been corrected to be dispatched properly from the server side
{% endtab %}
{% endtabs %}

### v0.5.9 (Beta) 9/1/2022

{% tabs %}
{% tab title="New" %}
Drive

* [File Uploading](../tutorials/your-drive-and-documents.md#uploading-batch-files-zip) now supports **ZIP**s, this means you can bulk import files from popular file hosting services such as Google Drive.
* Easily migrate all your files and directories directly into Sonoran CMS Drive with one ZIP.

Community Templates

* [Template Management](broken-reference)
  * This allows you to create templates from your community setup and share it with other communities to benefit from.
  * All submitted templates will go through a review process with the Sonoran CMS Development Team.
{% endtab %}

{% tab title="Changed" %}
Community Customization

* The way statuses were saved in the Community Customization was changed to improve the workflow of managing statuses.
{% endtab %}
{% endtabs %}

### v0.5.8 (Beta) 8/29/2022

{% tabs %}
{% tab title="New" %}
Community Templates

* "Standard" Community Template was added, accessible through community creation & existing communities
{% endtab %}

{% tab title="Changed" %}
Backend

* Several backend changes were added to assist support with debugging issues
{% endtab %}
{% endtabs %}

### v0.5.7 (Beta) 8/22/2022

{% tabs %}
{% tab title="New" %}
Dashboard URL Handling

* All pages accessible through the left-side menu in the dashboard will now take you to a physical URL that can be copied and pasted to members to open to directly.
* Further handling will be developed in further updates.&#x20;
{% endtab %}

{% tab title="Changed" %}
[FiveM Whitelist Resource](../integration-capabilities/in-game-integration-resources/core/core-submodules/whitelist.md)&#x20;

* The cache backup handling was updated to follow standards with the rest of the resource, now fully using [Sonoran.js](https://www.npmjs.com/package/@sonoransoftware/sonoran.js).
{% endtab %}

{% tab title="Fixed" %}
Community Templates

* Toolbar items set from a template on pre-existing communities will now properly set to imported pages, this was only for using a template on a existing community, not new communities.
{% endtab %}
{% endtabs %}

### v0.5.6 (Beta) 8/17/2022

{% tabs %}
{% tab title="New" %}
[Custom Domain](../tutorials/customization/custom-domain.md)

* Communities are auto-joined when visiting their custom domain (and successfully logging in)

[Custom Pages](../tutorials/community-website/website-builder.md)

* Custom pages can now be setup as direct links from toolbar items

Subscriptions

* Pro subscriptions now come with a 14 day free trial! All other subscriptions currently do not have trials
  * Only one trial per person, and one trial per community

[Community Templates](broken-reference)

* Community templates can now be applied to existing communities! If you wish to apply a template, look under Customization in the Administration Panel
{% endtab %}

{% tab title="Fixed" %}
Affiliates

* Affiliate Links will now correctly display information about Sonoran CMS

Menu

* Automatic redirection to the menu from index page is now much faster
{% endtab %}
{% endtabs %}

### v0.5.5 (Beta) 8/15/2022

{% tabs %}
{% tab title="New" %}
[Sonoran CAD Sync](../integration-capabilities/sonoran-cad-sync.md)

* Map Sonoran CAD permissions to your department ranks to sync permissions directly with Sonoran CAD.&#x20;
* Enable Kick and Ban sync to immediately kick and/or ban a user from your Sonoran CAD community when kicked or banned from your Sonoran CMS.

[Community Templates](broken-reference)

* Community Templates are now accessible through Community Customization, you can replace your community with an available template or add onto your existing community by adding bits and pieces from an available template.
{% endtab %}

{% tab title="Fixed" %}
Calendars

* Fixed an issue regarding an error when attempting to delete a calendar category.&#x20;
* Fixed an issue regarding calendar permissions not allowing certain actions despite what permissions that individual actually has.

Rosters

* Fixed an issue where roster rows wouldn't populate due to a row missing a rank/department.
{% endtab %}
{% endtabs %}

### v0.5.3 (Beta) 8/10/2022

{% tabs %}
{% tab title="New" %}
[Permissions Sync](../integration-capabilities/in-game-integration-resources/core/core-submodules/ace-permission-sync.md)

* A new integration resource was added to allow syncing of permissions between Sonoran CMS and your in-game server.
* Easily manage your in-game permissions by mapping them to specific Sonoran CMS ranks.&#x20;
{% endtab %}
{% endtabs %}

### v0.5.2 (Beta) 8/8/2022

{% tabs %}
{% tab title="New" %}
[Drive & Documents](../tutorials/your-drive-and-documents.md)

* Creating folders and moving files into folders is now possible
  * Permissions for folders coming soon
* Multiple file types now supported
  * +Presentations
  * +Excel Sheets
* Usage is now shown on the drive's toolbar
* Sensitive mode is now added for all file types
{% endtab %}

{% tab title="Fixed" %}
Communities

* Issue with changing Community IDs is resolved
{% endtab %}
{% endtabs %}

### v0.5.1 (Beta) 8/4/2022

{% tabs %}
{% tab title="New" %}
[Drive & Documents](../tutorials/your-drive-and-documents.md)

* Permissions have been expanded for the Sonoran CMS Drive, you'll now be able to set VIEW and EDIT permissions to individual documents by editing the document. This requires the "Modify All Documents (Drive)" permission.
* You can now upload documents directly to the Sonoran CMS Drive.

[Translations](https://github.com/Sonoran-Software/sonorancms_translations)

* A German translation has been added, thank you to [Linztric801](https://github.com/Linztric801) for that.

[Community Templates](broken-reference)

* A new template was added for community creation. Applying templates to created community's will be re-implemented in a future update.
{% endtab %}

{% tab title="Fixed" %}
SSO & Account

* Fixed an issue where your account username would not update on Sonoran CMS when changed on Sonoran Accounts.

Discord Webhooks

* Fixed an issue where form submission webhooks would not be sent out.

Image Uploading

* Fixed an issue that prevented image uploading to not be accessible at all, the button was fixed and will now appear.

Joining & Leaving Communities

* Fixed an issue which wouldn't allow you to join or leave a community.
{% endtab %}
{% endtabs %}

### v0.5.0 (Beta) 7/27/2022

{% tabs %}
{% tab title="New" %}
[Drive & Documents](../tutorials/your-drive-and-documents.md)

* Communities can now create and manage documents within their community directly in Sonoran CMS.
  * Initial permissions have been introduced to manage and/or view all documents.
* Drive includes a complete document editor to create and edit documents.
  * More document types will be supported in future updates.
{% endtab %}

{% tab title="Fixed" %}
Desktop & Mobile Apps

* An issue causing the desktop and mobile apps to not load was fixed.
{% endtab %}
{% endtabs %}

### v0.4.4 (Beta) 7/20/2022

{% tabs %}
{% tab title="New" %}
[Community Pages](../tutorials/community-website/website-builder.md)

* Custom pages now have their own URLs
* Links to custom pages are public (anyone can access the URLs)

Communities

* Community dashboards now load a separate URL: `/com/{community_uuid}`
* The community selection menu can be accessed through a button in the account dropdown

[Custom Domain](../tutorials/customization/custom-domain.md)

* Custom domains will now load the community dashboard at the index URL (i.e. `https://mycustomdomain.com/`
{% endtab %}

{% tab title="Fixed" %}
* Custom domains now properly redirect back with Sonoran Login
  * Discord and Apple logins still redirect back to the main site, unfortunately
* Redirect to login from dashboard being slow is fixed
* Other small bug fixes
{% endtab %}
{% endtabs %}

### v0.4.3 (Beta) 7/18/2022

{% tabs %}
{% tab title="New" %}
[Community Pages](../tutorials/community-website/website-builder.md)

* Communities now have the ability to create multiple custom pages for their community
  * Free: 2
  * Starter: 4
  * &#x20;Standard: 6
  * Plus: 10
  * Pro: Unlimited
{% endtab %}

{% tab title="Fixed" %}
* Bug creating new stage groups
* Bug with manager departments and ranks
* Bug with editing permissions in the department editor
{% endtab %}
{% endtabs %}

### v0.4.2 (Beta) 7/12/2022

{% tabs %}
{% tab title="New" %}
[Community Pages](../tutorials/community-website/website-builder.md)

* Grants all communities a single page they can edit with content sections, videos, and images. This page can be accessed on the Dashboard of a community
  * Much more is pending with community pages, stay tuned!
{% endtab %}

{% tab title="Fixed" %}
Login Issues

* Intermittent issues with login and usage of communities is now fixed

Migration Issues

* Many issues relating to the recent migration from v0.4.0 have been fixed, with more on the way
{% endtab %}
{% endtabs %}

### v0.4.1 (Beta) 7/11/2022

{% tabs %}
{% tab title="New" %}
[Toolbar Customization](../tutorials/customization/community-branding-and-settings.md#toolbar)

* Allows you to customize the top toolbar with buttons and dropdowns options with whatever label and link that you desire.

[Vanity URL](../tutorials/customization/custom-domain.md#vanity-urls-not-implemented)

* Allows all communities the option to use a **FREE** vanity URL with their community, this URL is based on your community ID and will provide you with a custom login page displaying your community's image.
{% endtab %}
{% endtabs %}

### v0.4.0 (Beta) 7/7/2022

This update consisted of a complete rewrite of the backend and partially the frontend. This was to update and move over to more reliable and stable techniques required for future updates. This update didn't consist of any new features but rather **several** fixes throughout the application.

### v0.3.0 (Beta) 4/4/2022

{% tabs %}
{% tab title="New" %}
[Public API](../developer-api-documentation/api-integration/)\
\- Introducing another way for developer's and community's to interact with Sonoran CMS.\
&#x20; \- The first set of endpoints are only the start to a long list of endpoints we have planned to offer.\
\
Clock In/Out\
\- Timestamped Notes were introduced in this update, allowing members to add a timestamped note to a current clock in.\
&#x20; \- Notes are accessible in the community profile view. Downloading/exporting of clock in data is restricted to Plus or higher.\
\
Whitelist System\
\- Introduced hand-in-hand with the public API, paired with the Sonoran provided whitelist script allows multi-server whitelist provided through Sonoran CMS.\
\
Community Accounts\
\- Last Login timestamp has been added and now tracked in the Administrative Panel Account area.\
\
Calendars\
\- The UI for the calendar events have been reworked to favor a large design instead of being so "crammed" and busy. No longer will cause UI to bug out due to missing image.\
\- Overall improvement of reliability of Discord webhooks sending for calendar related Discord webhooks.\
\
[API ID System](../developer-api-documentation/api-integration/getting-started/api-id-system.md)\
\- Allows a bridge between 3rd party resources and Sonoran CMS with utilizing a unique identifier to be used for API calls.
{% endtab %}

{% tab title="Fixed" %}
Billing Portal\
\- Subscriptions infinitely loading or erroring out due to failed subscriptions GET. Will now process if legacy errors out which was the main cause for the issue listed.\
\
Form Management Performance\
\- Large amount of forms would cause performance issues with the Form Management panel, this has been corrected and performance issues should be minimal to non-existent.\
\
Several other bugs were fixed but were very minor to be listed.
{% endtab %}
{% endtabs %}

### v0.2.1 (Beta) 2/5/2022

{% tabs %}
{% tab title="Fixed" %}
Form Permissions\
\- Permission issues related to seeing, changing, and replying to forms were fixed.\
\
Calendar\
\- Calendar times weren't always translated to local time and when sent through a Discord webhook it would provide the local server time, now it'll send the Discord timestamp format that'll automatically show in your local time.\
\
Desktop Version\
\- The desktop version of Sonoran CMS was unusable as of v0.2.0 due to a package issue.
{% endtab %}
{% endtabs %}

### v0.2.0 (Beta) 1/28/2022

{% tabs %}
{% tab title="New" %}
[Custom Form Stages](https://info.sonorancms.com/tutorials/getting-started/creating-custom-form-stages)\
\- Custom Form Stages are stages at which a form can be on, each stage can have powerful actions executed once that form gets changed to that stage. Various actions such as executing a webhook, automatically replying, etc.\


[Custom Form Stage Groups](https://info.sonorancms.com/tutorials/getting-started/creating-custom-form-stage-groups)\
\- Custom Form Stage Groups are _rough_ pre-determined routes you can assign to a form, groups allow you to choose what stage(s) are shown at each stage the form has the potential of being on.

\
Custom Form UI\
\- With this update, we introduced some new UI techniques and practices that we hope to expand throughout the app with. This only affected the custom forms section of the entire application, the forms got a dedicated page UI, dashboard sidebar got visited, etc.\
\
Page Transitions\
\- All pages now have transitions between them, this will make everything feel more smooth. It's nice.
{% endtab %}

{% tab title="Changed" %}
Backend\
\- There were several changes to the backend for the efficiency and productivity of the application. We improved upon the permissions system to sync more efficiently and effectively, allowing for less room for error.
{% endtab %}

{% tab title="Fixed" %}
Default Community Toggle\
\- When toggling default on a community, either off or on, it won't allow you to then select the community to enter it.

\
Rosters - Patrol Log Hour Calculations\
\- Patrol log hour roster columns would only display hours 0-23 instead of all hours, this has been corrected to show all hours after the date specified.\
\
Custom Form Issues\
\- Several issues related to custom forms have been fixed, form content not updating properly after saving, forms not updating at all, seeing forms not within permissions, not seeing forms within permissions, etc.\
\
Discord Webhooks\
\- Saving webhooks returned an error.
{% endtab %}
{% endtabs %}

### v0.1.6 (Beta) 8/4/2021

{% tabs %}
{% tab title="Fixes" %}
Calendar Events - Missing Functionality\
\- Fixed the missing functionality for editing calendar events, editing calendar events is now possible with this update.\
\
Account Creation\
\- Fixed an issue that caused signing up for a new account to be impossible and not work. This was pushed to the web a few days prior to v0.1.6-beta being released.\
\
Custom Forms\
\- Fixed an issue that would result in forms created on an individual to not be available in the available forms which wouldn't allow you to edit or archive the form after it being created.
{% endtab %}
{% endtabs %}

### v0.1.5 (Beta) 8/1/2021

{% tabs %}
{% tab title="Fixes" %}
&#x20;Community Selection Menu\
\- Fixed an issue on top of the last update's issue with being able to join or create multiple of the same community at the same time within a fraction of a second.\
\- Fixed an issue that would cause nothing to happen or show if you leave a community and rejoin that community you just left. It'll display an error and explain the issue if you're banned or for other reasons. Should allow users to rejoin communities now if they leave.\
\
Rosters\
\- Fixed an issue that would cause you to not see columns with the type of textarea when you create or edit a roster row.\
\- Fixed an issue that wouldn't allow you to scroll textarea type inputs if the content text exceeds the viewable box due to the field being disabled when viewing the response.
{% endtab %}
{% endtabs %}

### v0.1.4 (Beta) 7/31/2021

{% tabs %}
{% tab title="Fixes" %}
&#x20;Community Templates\
\- Fixed an issue that allowed for community templates to show all available instead of available within your current limits and would let you use a template that's out of your limits.\
\
Rosters\
\- Fixed an issue that would cause you to not see columns with the type of date or time when you create or edit a roster row.\
\
Community ID Query URL\
\- Fixed an issue that wouldn't properly auto-join/invite you to the community if you signup from a query URL.\
\
Missing Permissions\
\- Fixed an issue that caused the custom domain and discord integration tabs under advanced would not check if they had permissions. Discord Webhook Logging now has its own permission and the custom domain panel is now associated with the community customization permission.\
\
Community Selection Menu\
\- Fixed an issue that would allow you to join or create multiple communities if you spammed the community card or create a community button before it disappeared.
{% endtab %}
{% endtabs %}

### v0.1.3 (Beta) 7/29/2021

{% tabs %}
{% tab title="New" %}
&#x20;[Custom Domain System](../tutorials/customization/custom-domain.md)\
\- Communities that are on the Standard Plan+ can now set up their custom domain through a DNS record to be used as a custom login page for Sonoran CMS.\
\
[Discord RPC](../integration-capabilities/discord-rich-presence.md)\
\- The desktop application now adds rich presence info and buttons to your Discord profile. You can customize the invite link to your Sonoran CMS community, or your community's Sonoran CAD.\
\
[Discord Webhooks](../integration-capabilities/discord-webhooks.md)\
\- We've added Discord Webhooks for all your logging needs, you can now set up Discord webhooks to be sent when you get a new application, someone edits another account's information, etc.\
\
[Community Dashboard Buttons](../tutorials/customization/community-branding-and-settings.md#community-information)\
\- We've introduced functionality to the website and discord inputs that are in the Community Customization area of the Administrative Panel. Both of these inputs will now show buttons located in the initial Dashboard view.\
\
Community Login Query Strings\
\- Sonoran CMS URLs now support the use of ?comid=[**communityID**](../tutorials/customization/community-branding-and-settings.md#community-id) at the end of URLs. You can hand these out to automatically invite users to your community, this will automatically direct them to the community selection menu where they can accept an invite.\
\
[Android Application](../download-the-app.md)\
\- Sonoran CMS is now on the Google Play Store for [download](https://play.google.com/store/apps/details?id=com.sonorancms).&#x20;
{% endtab %}

{% tab title="Fixed" %}
Form Management\
\- Fixed an issue where permissions wouldn't be checked in the form management panel, this would allow anyone that has at least one permission to view that area (view pending, approve pending, deny pending, etc) can view all forms in that area even if they don't have the view pending for that specific form.\
\
Rosters\
\- Fixed an issue that would cause corruption on rosters when you attempt to add or edit a row. If you add a row not all columns would show on the input and if you edit it wouldn't allow you to save.\
\- Status selector column would corrupt and change the status to "Invalid Status" if when saving a row you didn't change the status at all.\
\
Empty Dropdowns for Member and Multi-Member Selector Fields\
\- Fixed an issue where dropdowns would be empty due to communities setting their **name & identifier format** as empty which would result in an empty format. This is fixed and will show the username of the account by default.\
\
Available Forms\
\- When editing a submitted form it wouldn't update locally unless you left the available forms area and then came back, it's been fixed from just saving to the backend.
{% endtab %}
{% endtabs %}

### v0.1.2 (Beta) 7/19/2021

{% tabs %}
{% tab title="New" %}
Delete Community\
\- We've added in the feature to delete your community if you ever need to, this is located in the Administrative Panel > Advanced Limits. View the guide [here](../tutorials/administrative/delete-community.md) for more information!
{% endtab %}

{% tab title="Fixed" %}
Rosters Populating\
\- Fixed an issue that would cause rosters to fail to populate and would infinitely load data due to a character cap for row entries.\
\
Community Templates\
\- Fixed an issue that would cause applying templates to not apply calendar permissions for imported ranks.\
\
Custom Forms - New Member Application\
\- Fixed an issue that would result in users that are set to pending within communities not be able to see custom forms with the type of "New Member Application".
{% endtab %}
{% endtabs %}

### v0.1.1 (Beta) 7/17/2021

{% tabs %}
{% tab title="New" %}
Remove Branding - Premium Feature\
\- A premium feature was added to Pro plan customers that will remove all Sonoran CMS branding and will replace it with community branding.\
\
Leave Community\
\- Leave community feature was added to the community selection menu, the button will be disabled if you own a community.
{% endtab %}

{% tab title="Changed" %}
Electron - Desktop Application\
\- Changed the desktop application frame to be frameless and styled the application bar to use Sonoran CMS branding and community branding if a community is on the Pro plan.
{% endtab %}

{% tab title="Fixed" %}
Default Community\
\- Fixed an issue that would result in the default community button, not function and wouldn't set the community as default.\
\
Clock In/Out System\
\- Fixed an issue that would cause a partial clock in (clocked in but not clocked out) to hang the browser if refreshed.\
\
Backend - Limits\
\- Fixed an issue that would result in limits not getting checked on both the frontend and backend, only the frontend.
{% endtab %}
{% endtabs %}

### v0.1.0 (Beta) 7/15/2021

{% tabs %}
{% tab title="New" %}
Landing Page\
\- A brand new landing page was created for [sonorancms.com](https://sonorancms.com/), a new layout was also introduced located in the footer of the page to direct you to other Sonoran Software Systems, LLC products.\
\
Billing Portal\
\- A billing portal was introduced to Sonoran CMS to accommodate the update to Sonoran CMS Beta. From v0.1.0 forward Sonoran CMS will be subscription-based with a free tier available to all users of Sonoran CMS.
{% endtab %}
{% endtabs %}

### v0.0.6 (Alpha) 7/7/2021

{% tabs %}
{% tab title="New" %}
Pagination Sync\
\- Row pagination will now save the rows per page setting locally for when you return to the page it will automatically sync from your local save.\
\
Administrative Panel - Accounts\
\- When viewing the accounts panel in the administrative panel you'll be able to filter all accounts by their community status (Active, Pending, Banned).\
\- Also when viewing the accounts panel in the administrative panel you'll be able to search for accounts, with this search it'll filter all accounts by their username and community name.
{% endtab %}

{% tab title="Fixed" %}
Administrative Panel - Accounts\
\- Fixed an issue that would cause the "kick" and "ban" features to essentially not work at all.\
\
Dashboard\
\- Fixed an issue that would cause the UI of the dashboard to not correctly update whenever the user's account would get updated.

Dashboard - Community Profile View\
\- Fixed an issue that would allow users to be able to view another account's profile and view all of their "Disciplinary Action" type forms without checking the community power of both accounts.
{% endtab %}
{% endtabs %}

### v0.0.5 (Alpha) 7/6/2021

{% tabs %}
{% tab title="New" %}
Community Templates System\
\- The Community Templates System will allow users to create new communities from templates instead of a blank community, they will also have the option to create a blank community if they choose.\
\- This system allows existing communities to import templates into their community as well, this is outlined in [Community Template System](broken-reference).\
\
Custom Form Editor - Move Fields\
\- Added a feature that allows users to move fields within a section in the Custom Form Editor.\
\
Department Manager - Duplicating Departments & Ranks\
\- Added a feature that allows users to duplicate entire departments and ranks for easier department managing, this is outlined in [Managing Rank Permissions](broken-reference).\
\
Department Manager - Permission Copy & Paste\
\- Added a feature that allows users to copy and paste permissions across different ranks, this is outlined in [Managing Rank Permissions](broken-reference).
{% endtab %}

{% tab title="Changed" %}
App Version UI\
\- Modified the App Version located at the bottom of the version to a redirect to the changelog.\
\
Account Profile\
\- Changed the "Edit Account" button in the account profile to redirect you to the Sonoran Accounts site to modify your username, email preferences, etc.\
\
Roster View\
\- Changed the roster values to only show a tooltip if the total characters are over 25, before this it would have a tooltip for all values.
{% endtab %}

{% tab title="Fixed" %}
Dashboard - Permissions\
\- Fixed an issue that would cause users to be missing permissions and be redirected to the community selection menu when they refresh anywhere on the dashboard. This introduces a more efficient and smoother transition from anywhere to the dashboard.\
\
Administrative Panel - Accounts\
\- Fixed an issue that would allow users to be able to kick/ban themselves.\
\
Dashboard - Community Profile View\
\- Fixed an issue that resulted in "member selector" and "multi-member selector" fields not populating their options correctly.\
\
Community Selection Menu\
\- Fixed an issue that would allow users to select more than one default community.\
\
Dashboard - Community Calendar\
\- Fixed an issue that wouldn't allow community owners to create events unless they had explicit permission.\
\
Custom Forms\
\- There was an issue that was fixed that caused forms in the Form Management area with the "multi-member selector" field to show blank on that field area.\
\- Fixed an issue that would show "for " on the form top bar when submitting a new form in the Available Forms area.\
\- Fixed an issue that would cause an inconsistent input mask between the Clock In/Out form section for dates.\
\
Administrative Panel - Custom Roster Editor\
\- Fixed an issue that would cause the wrong UI being shown with roster columns due to a character case.\
\
Administrative Panel - Department Manager\
\- Fixed an issue that would cause the wrong department to get removed when using the remove department feature within the department manager.&#x20;
{% endtab %}
{% endtabs %}

### v0.0.4 (Alpha) 6/30/2021

{% tabs %}
{% tab title="New" %}
Version Viewer\
\- The version of CMS that you're using will be shown at the very bottom of the page.\
\
Calendar Events Deletion\
\- Added a feature to allow users with permission to delete calendar events off of a calendar.
{% endtab %}

{% tab title="Fixed" %}
Login Password Validation\
\- Fixes an issue where there would be strict input validation on login password input, this would cause users that created a password prior to the new password requirements to not be able to login.\
\
Signup Error\
\- Fixes an issue where it would give you a non-descriptive error if your email was already in use when signing up.\
\
Profile Clock Data\
\- Fixed an issue where it would show "Invalid Date" in the Clock In/Out table.\
\
New Calendar Event Dialog\
\- Fixed an issue where there was no form validation on the new event dialog, this would allow for any user with permission to create an event with no information.\
\
Form Submissions on Profile View\
\- Fixed an issue where nothing would happen once you submit a form on someone's profile, it will now display a top notification and input into the correct table.\
\
Disciplinary Action Forms\
\- Fixed an issue where users that have a "Disciplinary Action" form type submitted on their profile to be able to see that submission and edit it.
{% endtab %}
{% endtabs %}

### v0.0.3 (Alpha) 6/30/2021

{% tabs %}
{% tab title="New" %}
Image Uploading\
\- Image uploading is now supported for community information and custom forms.\
\
Custom Form Editor\
\- Premade form sections will now have a required section toggle similar to the field require toggle.\
\
Custom Forms via Profile View\
\- Custom forms can now be directly submitted to a user within the user's profile view.
{% endtab %}

{% tab title="Changed" %}
Community Customization\
\- Moved "Custom Statuses" from being in the "Community Info" expansion to it's own expansion.\
\
Clock In/Out\
\- Changed the way clock in/out times are parsed and saved.
{% endtab %}

{% tab title="Fixed" %}
Notifications\
\- Fixed an issue where notifications would be sent out but wouldn't be saved in the backend.\
\
Backend\
\- Fixed an issue with multiple DB calls not providing the proper date & time format when saving.

Login, Signup & Top Toolbar\
\- Fixed login, signup and top toolbar having issues with sizing and positioning on smaller screen sizes.\
\
Community Creation Validation\
\- Fixed an issue where there were no validation checks for community creation inputs.\
\
Viewing Forms\
\- Fixed an issue where form styling wouldn't be consistent between all areas that you can view a custom form, now spacing will be more consistent between all areas.\
\
Dashboard\
\- Fixed an issue of getting kicked to the menu page if your system status is "Pending" within the community.\
\
Rosters\
\- Fixed an issue where anyone with roster view permissions to edit any roster data.
{% endtab %}
{% endtabs %}

### v0.0.2 (Alpha) 6/29/2021

{% tabs %}
{% tab title="Changed" %}
Login\
\- Moved "Forgot Password" to utilize an in-app procedure, no longer will redirect to Sonoran Accounts.\
\- Changed login inputs to validate input once the user has lost focus of the input instead of as it's typed in.

Signup\
\- Changed signup inputs to validate input once the user has lost focus of the input instead of as it's typed in.
{% endtab %}

{% tab title="Fixed" %}
Account Registration\
\- Fixed an issue where no email would be sent to the user to verify their account.

Form Management - Form Dialog\
\- Fixed an issue of the "Patrol Start/End" premade form section not showing up on submitted forms within the "Form Management" section of the Dashboard.

Profile - Name Header\
\- Fixed an issue of the name/identifier header to show name fine but with "null".

Custom Rosters\
\- Fixed an issue where you couldn't input select options when selecting the "select" column type.\
\- Fixed an issue where the checkbox column type wouldn't work at all.
{% endtab %}
{% endtabs %}

### v0.0.1 (Alpha) 6/28/2021

{% tabs %}
{% tab title="New" %}
Initial Release\
\- Initial release of Sonoran CMS (Alpha)
{% endtab %}
{% endtabs %}
