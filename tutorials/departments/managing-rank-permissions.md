---
description: This guide covers managing rank permissions within departments in Sonoran CMS.
---

# Managing Rank Permissions

### What is the CMS Rank System?

Managing Rank Permissions can be a pain when you have several departments that all require several forms, rosters, etc. With Sonoran CMS, we've made improvements to make your life a little easier when managing permissions on ranks.

### Default Department Permissions

Each department is able to have default permissions, these permissions are applied to all ranks within the department upon permission evaluation. These are the same set of permissions that are able to be given to ranks individually.

### Duplicating Ranks & Departments

By allowing users to duplicate an entire department or a single rank, it will make creating and managing departments much easier. Duplicating a whole department will allow you to edit a department before you save the duplicated department. If you do not want to duplicate an entire department and just need to add more ranks to a department, you can duplicate a rank by hitting the orange outlined button next to the move buttons on a rank.

![Sonoran CMS's Duplicate Department Feature](../../.gitbook/assets/69794hi0.png)

![Sonoran CMS's Duplicate & Remove Rank Options](../../.gitbook/assets/08gf7hh4.png)

### Permission Copy & Paste System

While modifying or even creating ranks, you'll want to share permissions across them; you can easily copy and paste permissions across ranks by right-clicking the header permission (ex. "CMS Permissions," "Roster Permissions," etc.) if you want to copy and paste specific roster, form or calendar permissions you can right-click the label of the roster, form, calendar, etc.

![Sonoran CMS's Copy & Paste System - Copying All Applicatin Permissions](../../.gitbook/assets/6i7d144e.png)

![Sonoran CMS's Copy & Paste System - Copying "Los Santos Police Department Roster" Permissions](../../.gitbook/assets/554agfd2.png)

### Permission Explanations

All permissions within the Department Editor have been laid out and detailed with what they do, this should aide in configuring the correct permissions for your community's needs:

#### Community System Permissions

| Permission                       | Explanation                                                                                                                                                  |
| -------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Kick Users                       | Granting this permission will allow a user with this rank to kick another user from the community.                                                           |
| Ban Users                        | Granting this permission will allow a user with this rank to ban another user from the community.                                                            |
| Change Permissions               | Granting this permission will allow a user with this rank to modify another user's permissions and account details from the community.                       |
| Modify Community Customization   | Granting this permission will allow a user with this rank to customize aspects of the Sonoran CMS platform such as Name, Image, Name/Identifier Format, etc. |
| Modify Departments via Manager   | Granting this permission will allow a user with this rank to customize departments and ranks like you are doing now.                                         |
| Modify Custom Forms via Editor   | Granting this permission will allow a user with this rank to customize the custom form templates that are used when users submit forms.                      |
| Modify Custom Rosters via Editor | Granting this permission will allow a user with this rank to customize the roster templates that are used to display the community's roster data.            |
| Modify Discord Logging Webhooks  | Granting this permission will allow a user with this rank to customize the Discord webhook settings for the community.                                       |
| Modify API Integration           | Granting this permission will allow a user with this rank to customize and retrieve API credentials.                                                         |
| Modify Toolbar                   | Granting this permission will allow a user with this rank to customize the toolbar settings for the community.                                               |
| Modify Pages                     | Granting this permission will allow a user with this rank to customize the pages for the community.                                                          |
| Modify All Documents (Drive)     | Granting this permission will allow a user with this rank to manage all documents within the Sonoran CMS Community Drive.                                    |

#### Form Permissions

| Permission             | Explanation                                                                                                                                                       |
| ---------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| View Submitted         | Granting this permission will allow a user with this rank to view all submitted forms of this type.                                                               |
| Edit Own Form          | Granting this permission will allow a user with this rank to edit their submissions of this type of form.                                                         |
| Change Form Stage      | Granting this permission will allow a user with this rank to change the stage of a submitted form of this type.                                                   |
| Enable/Disable Replies | Granting this permission will allow a user with this rank to change the reply settings of a submitted form of this type.                                          |
| Basic Reply Access     | Granting this permission will allow a user with this rank to reply to a submitted form of this type if the reply settings allow for Basic replies.                |
| Mod Reply Access       | Granting this permission will allow a user with this rank to reply to a submitted form of this type if the reply settings allow for Basic or Mod replies.         |
| Admin Reply Access     | Granting this permission will allow a user with this rank to reply to a submitted form of this type if the reply settings allow for Basic, Mod, or Admin replies. |
| Submit Form            | Granting this permission will allow a user with this rank to submit a form of this type.                                                                          |
| Admin Delete           | Granting this permission will allow a user with this rank to fully delete a submission of this form.                                                              |

#### Roster Permissions

| Permission                  | Explanation                                                                                                                                      |
| --------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------ |
| View                        | Granting this permission will allow a user with this rank to view this roster.                                                                   |
| Add Primary Row             | Granting this permission will allow a user with this rank to add a user to the roster as a Primary Row (sorted initially before secondary rows). |
| Add Secondary Row           | Granting this permission will allow a user with this rank to add a user to the roster as a Secondary Row (sorted after primary rows).            |
| Edit Primary Row            | Granting this permission will allow a user with this rank to edit a primary row in this roster.                                                  |
| Edit Secondary Row          | Granting this permission will allow a user with this rank to edit a secondary row in this roster.                                                |
| Remove Primary Row          | Granting this permission will allow a user with this rank to remove a primary row from the roster.                                               |
| Remove Secondary Row        | Granting this permission will allow a user with this rank to remove a secondary row from the roster.                                             |
| View Mod Hidden Column(s)   | Granting this permission will allow a user with this rank to view roster column(s) that are marked as Mod only.                                  |
| View Admin Hidden Column(s) | Granting this permission will allow a user with this rank to view roster column(s) that are marked as Admin only.                                |

#### Calendar Category Permissions

| Permission  | Explanation                                                                                               |
| ----------- | --------------------------------------------------------------------------------------------------------- |
| View        | Granting this permission will allow a user with this rank to view events within this calendar category.   |
| Create      | Granting this permisison will allow a user with this rank to create events within this calendar category. |
| Remove      | Granting this permission will allow a user with this rank to remove events within this calendar category. |
| Edit Others | Granting this permission will allow a user with this rank to edit events within this calendar category.   |

#### Servers Permissions

| Permission      | Explanation                                                                                                                                                                                               |
| --------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Allow Whitelist | Granting this permission will allow a user with this rank to be allowed through the API whitelist (if a user holds the block permission for this server they'll be blocked as block takes precedence).    |
| Block Whitelist | Granting this permission will block a user with this rank to be allowed through the API whitelist (if a user holds the allow permission for this server they'll still be blocked as it takes precedence). |

#### Profile Field Permissions

| Permission                                 | Explanation                                                                                                                                                                                                                   |
| ------------------------------------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Attaches to Profile                        | Granting this permission will attach this profile field to all member's profiles that hold this rank. This will allow anyone who views your profile to see it unless either of the next two permissions are applied.          |
| Hides Field from Profile Owner             | Granting this permission will hide the field from the member's profile that hold's this rank.                                                                                                                                 |
| Require Mod Power to View on Profile       | Granting this permission will require a member to have the "View Field on Other Profiles - Mod Power" in order to view the field on a profile.                                                                                |
| Require Admin Power to View on Profile     | Granting this permission will require a member to have the "View Field on Other Profiles - Admin Power" in order to view the field on a profile.                                                                              |
| View Field on Other Profiles - Mod Power   | Granting this permission will allow a member to view this field on a profile with "Mod Power" in mind. See above permissions for association.                                                                                 |
| View Field on Other Profiles - Admin Power | Granting this permission will allow a member to view this field on a profile with "Admin Power" in mind. See above permissions for association.                                                                               |
| Allow Profile Owner to Edit                | Granting this permission will allow the member that holds this rank to edit this field on their profile. If the "Hides Field from Profile Owner" permission is granted it will ignore this permission as it won't be visible. |
| Edit Field on Other Profiles               | Granting this permission will allow the member that holds this rank to edit this field on any member profiles that their able to view.                                                                                        |
