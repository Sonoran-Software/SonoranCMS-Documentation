---
description: View the latest changes to Sonoran CMS!
---

# 📋 Changelog

## Roadmap

[View our upcoming roadmap!](https://roadmap.sonorancms.com/)

## Changelog

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
[**Calendar** RSVP Limits](../tutorials/calendars/community-events.md#regarding-rsvp-limit)

Calendar events can now be RSVP limited, you can now set how many members can RSVP to an individual event.

**API Endpoints**

[**Event RSVP**](../developer-api-documentation/api-integration/api-endpoints/events/rsvp.md)

[**Drive** Downloads](../tutorials/getting-started/your-drive-and-documents.md#drive-downloads)

Additional file types can now be uploaded and downloaded directly from the Sonoran CMS Drive. Any **.rpf**, **.wav**, **.mp3**, **.zip**, and **.pdf** are accepted. They aren't "viewable" but are able to be downloaded easily. Additionally there's now a download URL that can be copied for the _downloadable_ file types as described above.

[**Community Gallery**](../tutorials/getting-started/gallery-system.md)

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
_Side Menu & Hamburger Menu while Signed into a Community_\
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

Ranks can now be applied to [individuals manually](../tutorials/getting-started/modify-users-permissions-and-information.md#granting-expiring-ranks) or through [stage actions](../tutorials/getting-started/creating-custom-forms.md#action-explanation-change-submitters-department-rank) to set a rank to expire, the rank will automatically be removed upon the next check (every fetch for the account) if found expired. Ranks can be set to expire after X amount of hours/days or by a exact time/day that you set.

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
[**Custom Page Paths**](../tutorials/customization/custom-pages.md#custom-page-paths)

Custom pages can now have a custom path slug to further customize your pages. These path slugs will replace the number ID that is given by default for all custom pages. These paths support custom domains, example: `lspd/sop` would append to a custom domain such as `cms.sonoranrp.com/lspd/sop`.

[**Custom Form Folders**](../tutorials/getting-started/creating-custom-forms.md#custom-form-folders)

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
[**Automatic Rosters**](../tutorials/getting-started/creating-custom-rosters.md#department-automatic)

Rosters have been reworked to add additional functionality and purpose. All existing rosters have been moved to the type of "Custom", this type is considered for all rosters that will allow you to add and remove rows as you please. With this change the previous _Department_ and _Sub-Department_ type have been deprecated.\
\
A new roster type, Department, was added to replace the previous _Department_ roster type. This new roster type is considered automatic meaning rows will be dynamically created based on all members that hold a rank within the specified department. Members will be sorted in the order which their rank within the department is shown, as well as alphabetically.
{% endtab %}

{% tab title="Fixed" %}
**Form Management**

Filtering forms to show only **Deleted Forms** would show no forms despite fetching all deleted forms.

[**Custom Forms**](../tutorials/getting-started/creating-custom-forms.md)

An internal ID was not setting correctly upon save which would make the form no longer editable or usable.

**Menu Items**

Menu items would not correctly evaluate permissions.
{% endtab %}
{% endtabs %}

### v0.5.29 (Beta) 2/17/2023

{% tabs %}
{% tab title="New" %}
[**Form Submission Limits**](../tutorials/getting-started/creating-custom-forms.md#limiting-form-submissions)

Custom Form Templates now have limit settings, these settings will allow you to customize how your forms are being submitted. This allows for submissions to be limited to a certain amount per user, within the last X days, and even with a cooldown between submissions.

* Limit Total Submissions from each User
  * Ignore submissions that are set to a stage with the type of "Archived"
* Submission Cooldown
* Limit Within Last X Days

[**Department Rank Cosmetic Customization**](../tutorials/getting-started/creating-departments.md#4.-customize-rank-cosmetic-styling)

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
[Forum System](../tutorials/getting-started/forum-system.md)

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
[Dashboard](../tutorials/customization/custom-pages.md#default-dashboard-page)

The community Dashboard / Landing page has been completely reworked, this now allows for the full customization of the Custom Page Editor. Set any existing custom page as your community's dashboard page.

[Custom Page Editor](../tutorials/customization/custom-pages.md#page-editing)

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

[Navigation Button Visibility](../tutorials/customization/navigation-sidebar.md)

Navigation items on the sidebar can now be dynamically shown based upon permissions. Documentation explains how each navigation item is permission evaluated.

[Privatized Pages](../tutorials/customization/custom-pages.md#privatized-pages)

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
[Custom Forms](../tutorials/getting-started/creating-custom-forms.md)

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

[Page Re-ordering](../tutorials/customization/custom-pages.md#sorting-pages)

* The ability to sort the position of the pages in which they appear in lists.

[Form Re-ordering](../tutorials/getting-started/creating-custom-forms.md#sorting-forms)

* The ability to sort the position of the forms in which they appear in Available Forms.

[Conditional Custom Form Sections](../tutorials/getting-started/creating-custom-forms.md#conditional-sections)

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
[Forum System](../tutorials/getting-started/forum-system.md)

Several new changes have been added to the forum system;

* [Sub-Categories](../tutorials/getting-started/forum-system.md#creating-forum-sub-categories)
* [Topic Attachments](../tutorials/getting-started/forum-system.md#topic-creation-forum-topic-attachments)
* [Private Topics](../tutorials/getting-started/forum-system.md#creating-private-topics)
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
[Forum System](../tutorials/getting-started/forum-system.md)

Several new changes have been added to the forum system;

* [Dedicated Forum Category Page](../tutorials/getting-started/forum-system.md#dedicated-forum-category-page)
* [Topic Pinning & Locking](../tutorials/getting-started/forum-system.md#topic-actions-pin-and-lock)
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
[Forum System](../tutorials/getting-started/forum-system.md)

**Delete Topics** permission section for forum category's has been moved to **Manage Topics** allowing that same permission section to handle topic deletion, pinning and locking.\
**Delete Topics -> Manage Topics**
{% endtab %}
{% endtabs %}

### v0.5.19 (Beta) 12/6/2022

{% tabs %}
{% tab title="New" %}
[Forum System](../tutorials/getting-started/forum-system.md)

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

[Community Discovery](../tutorials/getting-started/community-discovery.md)

* Bumping
  * Bumping your community will now include your community's banner image upon bump. If no banner image is set it won't include any image.

[Custom Pages](../tutorials/customization/custom-pages.md)

* Page Elements
  * Two new page elements have been added, `Button` and `Button Group`. Both these elements can be added to any custom page. Each button's functionality and style can be configured to fit your needs. Buttons can target to a external website, custom form and custom page.
{% endtab %}

{% tab title="Fixed" %}
[Community Discovery](../tutorials/getting-started/community-discovery.md)

* Clicking community cards to open up the community modal would not be possible unless you click the image or text on the card. The whole card should be clickable.
* Clicking a community card would display a modal with additional community information and options to join, this would not include the image.
{% endtab %}

{% tab title="Changed" %}
[Department Manager](../tutorials/departments/)

* Performance
  * Several improvements have been implemented to decrease any issues with performance regarding permission management of departments.
{% endtab %}
{% endtabs %}

### v0.5.17 (Beta) 11/14/2022

{% tabs %}
{% tab title="Fixed" %}
[Community Drive](../tutorials/getting-started/your-drive-and-documents.md)

* Editing Files
  * An issue which would cause files to not be edited within the member editing page but would still allow edits through the public-sided edit file page.

[Discord Webhook Logging](../integration-capabilities/discord-webhooks.md)

* Editor
  * An issue which would cause the webhook input editor to not load fully or at all.
* Webhooks Executing
  * An issue which would causing the Calendar Creation webhook to not execute at all.

[Community Discovery](../tutorials/getting-started/community-discovery.md)

* Bump System
  * An issue which would cause the Discord advertisement webhook message to include various programmatic types within the message such as '\[object Object]' & 'undefined'.

[Community Member Profile](../tutorials/customization/community-profile-fields.md)

* Forms
  * An issue which would cause individuals to be unable to submit forms directly onto another user's profile to attach it to their profile.

[Rosters](../tutorials/getting-started/creating-custom-rosters.md)

* Column Types
  * Community Identifier row columns would not populate with a user's primary identifier properly unless the conditions which very specific.

[Custom Stage Form Actions](broken-reference)

* Status Modifier
  * An issue which would cause the stage action to change community status to not execute properly unless the individual was active within the community from the start.
{% endtab %}

{% tab title="Changed" %}
[Community Discovery](../tutorials/getting-started/community-discovery.md)

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
[Community Discovery](../tutorials/getting-started/community-discovery.md)

* [Bump System](../tutorials/getting-started/community-discovery.md#community-discovery-bump-system)
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
[Community Discovery](../tutorials/getting-started/community-discovery.md)

The Community Discovery Portal brings more members to communities by streamlining the joining process for your community. Joining a community through the discovery portal will automatically prompt them with the community's new member application. Advertise your community to the thousands of users using Sonoran CMS!

[Default Department Permissions](../tutorials/departments/managing-rank-permissions.md#default-department-permissions)

Default Department Permissions applies the same set of permissions to all ranks within the department to easily manage permissions.

[Admin Form Delete](../tutorials/forms/admin-managing-forms.md)

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
[Drive](../tutorials/getting-started/your-drive-and-documents.md#folders)

* [Publicly Accessible Files](../tutorials/getting-started/your-drive-and-documents.md#publicly-accessible-files)
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
[Drive Enhancements](../tutorials/getting-started/your-drive-and-documents.md#folders)

* [Share Settings Overhaul](../tutorials/getting-started/your-drive-and-documents.md#share-settings)
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
[Drive Folder Permissions Expansion](../tutorials/getting-started/your-drive-and-documents.md#folders)

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
[Discord Role Sync](../integration-capabilities/discord-role-sync/)

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

* [File Uploading](../tutorials/getting-started/your-drive-and-documents.md#uploading-batch-files-zip) now supports **ZIP**s, this means you can bulk import files from popular file hosting services such as Google Drive.
* Easily migrate all your files and directories directly into Sonoran CMS Drive with one ZIP.

Community Templates

* [Template Management](../tutorials/other-features/community-template-system.md#template-management)
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
[FiveM Whitelist Resource](../integration-capabilities/in-game-integration-resources/gta-rp-integrations/available-resources/whitelist.md)&#x20;

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

[Custom Pages](../tutorials/customization/custom-pages.md)

* Custom pages can now be setup as direct links from toolbar items

Subscriptions

* Pro subscriptions now come with a 14 day free trial! All other subscriptions currently do not have trials
  * Only one trial per person, and one trial per community

[Community Templates](../tutorials/other-features/community-template-system.md)

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

[Community Templates](../tutorials/other-features/community-template-system.md)

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
[Permissions Sync](../integration-capabilities/in-game-integration-resources/gta-rp-integrations/available-resources/ace-permission-sync.md)

* A new integration resource was added to allow syncing of permissions between Sonoran CMS and your in-game server.
* Easily manage your in-game permissions by mapping them to specific Sonoran CMS ranks.&#x20;
{% endtab %}
{% endtabs %}

### v0.5.2 (Beta) 8/8/2022

{% tabs %}
{% tab title="New" %}
[Drive & Documents](../tutorials/getting-started/your-drive-and-documents.md)

* Creating folders and moving files into folders is now possible
  * Permissions for folders coming soon
* Multiple file types now supported
  * \+Presentations
  * \+Excel Sheets
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
[Drive & Documents](../tutorials/getting-started/your-drive-and-documents.md)

* Permissions have been expanded for the Sonoran CMS Drive, you'll now be able to set VIEW and EDIT permissions to individual documents by editing the document. This requires the "Modify All Documents (Drive)" permission.
* You can now upload documents directly to the Sonoran CMS Drive.

[Translations](https://github.com/Sonoran-Software/sonorancms\_translations)

* A German translation has been added, thank you to [Linztric801](https://github.com/Linztric801) for that.

[Community Templates](../tutorials/other-features/community-template-system.md)

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
[Drive & Documents](../tutorials/getting-started/your-drive-and-documents.md)

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
[Community Pages](../tutorials/customization/custom-pages.md)

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
[Community Pages](../tutorials/customization/custom-pages.md)

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
[Community Pages](../tutorials/customization/custom-pages.md)

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
\- This system allows existing communities to import templates into their community as well, this is outlined in [Community Template System](../tutorials/other-features/community-template-system.md).\
\
Custom Form Editor - Move Fields\
\- Added a feature that allows users to move fields within a section in the Custom Form Editor.\
\
Department Manager - Duplicating Departments & Ranks\
\- Added a feature that allows users to duplicate entire departments and ranks for easier department managing, this is outlined in [Managing Rank Permissions](../tutorials/departments/managing-rank-permissions.md#duplicating-ranks-and-departments).\
\
Department Manager - Permission Copy & Paste\
\- Added a feature that allows users to copy and paste permissions across different ranks, this is outlined in [Managing Rank Permissions](../tutorials/departments/managing-rank-permissions.md#permission-copy-and-paste-system).
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
