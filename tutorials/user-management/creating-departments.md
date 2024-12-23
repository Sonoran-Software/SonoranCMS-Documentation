---
description: >-
  Now that you've created your community and started to invite users you'll want
  to start creating departments. Learn more below
---

# Creating Ranks

{% embed url="https://www.youtube.com/watch?v=QBcJdXYmMjU" %}

## Accessing the Rank Manager

To access the "Rank Manager", head to `Administrative Panel` > `Ranks`

Within this Ranks panel you'll be able to create departments and ranks  your members, this will be the central panel for deciding permissions based on "ranks", when new, removed, or modified Custom Forms, Calendar Categories, and Rosters will be reflected with available permissions under each rank.

![Sonoran CMS Department Manager Panel - Add/Remove/Edit Departments & Ranks](../../.gitbook/assets/CMS_RankManager.png)

{% hint style="info" %}
Rank **Power** will be compared to other users as a global user power, this will be utilized to determine if you can modify other individuals. If your power is higher than another individual then you can modify them, if it's less then you cannot.
{% endhint %}

## Creating a Department

Click the "Add Department" button, which can be found at the end of your existing departments (or the beginning if you're on mobile). Once clicked, a dialog popup should appear

The dialog contains two crucial fields for your department:

1. Department Name (Example: Police Department)
2. Short Name (Example: PD)

<figure><img src="../../.gitbook/assets/CMS_EditDept.png" alt=""><figcaption><p>Sonoran CMS - Department Editor - Creating a Department</p></figcaption></figure>

You do not need to customize anything to create your department, so saving now is fine. When you're ready to save, click anywhere outside the department box. Or, you can set permissions associated with the department.

### Department Permissions

<figure><img src="../../.gitbook/assets/CMS_EditDeptToggled.png" alt=""><figcaption><p>Sonoran CMS - Rank Editor - Setting Department Permissions</p></figcaption></figure>

This is where you'll need to assign permissions that you want all ranks within the department to inherit. These are the same set of permissions that ranks are able to get assigned but will be applied to all ranks upon permission evaluation.

You can toggle all permissions in a category with the Toggle On/Off button above the permissions.

## Creating a Rank

Under the department header in, click the green plus button to begin creating a new rank

This will bring up a new dialog where you'll need to input a name and setup permissions for your new rank.

Permissions on a rank dictate what a person with that rank can do. There are many different types of permission scopes:

### Assigning Rank Permissions

Rank permissions can be assigned using the same method as department permissions. There are many different categories of permissions you can assign, for example:

* **"Editor"** permissions are for modifying the community and customizations.
* **"System"** permissions are for general administration (e.g. kick, ban, clock in & out).
* **"Navigation"** permissions are for viewing navigation buttons.
* **"Forms"** permissions are for the custom forms.
* **"Rosters"** permissions are based on the custom records made in `Administrative Panel` > `Rosters`.
* **"Calendars"** permissions are based on the calendar categories.
* **"Profile Fields"** permissions are based on the Profile Fields created in the `Administrative Panel` > `Profile Fields`.
* **"Servers"** permissions are based on the API Integration servers made in `Administrative Panel` > `Integrations`.

<figure><img src="../../.gitbook/assets/CMS_EditRank.png" alt=""><figcaption><p>Sonoran CMS - Department Editor - Rank Permissions</p></figcaption></figure>

When you are done customizing your rank permissions, click anywhere outside to close the dialog and automatically save it. Your new rank will show up under the department you created it in.

You search for specific permissions. This will bring display a number of how many settings match your search in each category, and will show only the ranks in a given category that match the search.



<figure><img src="../../.gitbook/assets/CMS_SearchPerms.png" alt=""><figcaption><p>Sonoran CMS - Department Editor - Search Rank Permissions</p></figcaption></figure>

If you ever want to modify permissions, click the person icon to the right of the name to open the dialog again.

### Customize Rank Cosmetic Styling

Ranks are able to be customized to the styling that best fits your community. You are able to customize the color and icon associated with each rank. You can specify common color names or custom hex colors. To access this setting, click on the icon to the left of the rank name.

<figure><img src="../../.gitbook/assets/CMS_RankCosmetics.png" alt=""><figcaption><p>Sonoran CMS - Department Editor - Rank Cosmetic Customization</p></figcaption></figure>

### Customize Rank Power

To the top right of the rank name you will see a number, by default it is 0. Click on this to access the rank power tab. Rank Power determines who has higher authority in the community.

Below this you will be able to specify whether this is a primary or secondary rank. Activating either one will make it so the rank can only be used as a primary rank or a secondary rank. No selection means it can be used for both.

<figure><img src="../../.gitbook/assets/CMS_RankPower2.png" alt=""><figcaption><p>Sonoran CMS - Department Editor - Rank Power</p></figcaption></figure>

## Importing Ranks from Discord Roles

Instead of manually creating rank for everything, you can also directly import the roles from any linked Discord server directly to your CMS Community.

To do this, in any department, click the Discord icon below the deaprtment header.

<figure><img src="../../.gitbook/assets/CMS_RanksImportDiscord01.png" alt=""><figcaption><p>Sonoran CMS - Rank Editor - Import Discord Roles</p></figcaption></figure>

Next, click `Select Guild` and select the linked guild you would like to import roles from. If you have not yet linked a Discord guild to CMS, you must do so through our [Sonoran Discord Bot](https://info.sonoranbot.com/en/tutorials/getting-started).

<figure><img src="../../.gitbook/assets/CMS_RanksImportDiscord03.png" alt=""><figcaption><p>Sonoran CMS - Rank Editor - Select Guild</p></figcaption></figure>

<figure><img src="../../.gitbook/assets/CMS_RanksImportDiscord04.png" alt=""><figcaption><p>Sonoran CMS - Rank Editor - Click Guild</p></figcaption></figure>

When you select a guild to import roles from, it will populate the window with all existing roles within that Discord. You can select which roles you would like to import, or click the top checkbox to select all.

<figure><img src="../../.gitbook/assets/CMS_RanksImportDiscord05.png" alt=""><figcaption><p>Sonoran CMS - Rank Editor - Select Discord Roles</p></figcaption></figure>

Finally, click `Import Roles to Ranks` at the bottom of the window, and new ranks matching the name and color of the roles will be created:

<figure><img src="../../.gitbook/assets/CMS_RanksImportDiscord06.png" alt=""><figcaption><p>Sonoran CMS - Rank Editor - Imported Discord Roles</p></figcaption></figure>

Please note that you will still have to configure permissions for these newly created ranks. By default they will assume the permissions of their department, but any further changes must be done manually.



## Copy Rank IDs

Some integrations may require you to input Sonoran CMS rank IDs.

Select the `...` menu and the `Copy Rank ID` button to copy the rank ID to your clipboard.

<figure><img src="../../.gitbook/assets/image (61).png" alt="" width="174"><figcaption></figcaption></figure>

