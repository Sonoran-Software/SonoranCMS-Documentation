---
description: >-
  Allow further customization on your community member's profiles. Easily add
  and edit date directly on a profile with view & edit permissions.
---

# Profile Fields

{% embed url="https://www.youtube.com/watch?v=f7kPZXi1Fdc" %}

<figure><img src="../../.gitbook/assets/CMS_ProfileOverview.png" alt=""><figcaption><p>Sonoran CMS - Profile View - Profile Information / Profile Fields</p></figcaption></figure>

Profile Fields allow communities to put direct information onto member's profiles that can be restricted to certain viewers, editors, etc. with rank permissions. Profile Fields are dynamically displayed on profiles depending on what ranks the profile you're viewing holds.

<figure><img src="../../.gitbook/assets/CMS_ProfileFieldsEditor.png" alt=""><figcaption><p>Sonoran CMS - Profile Fields Editor</p></figcaption></figure>

Easily create and edit profile fields to your liking to fit your community's needs. Each field can be customized to have a different type and label with more to come in the future.

### Creating Profile Fields

To start creating profile fields go to the Administrative Panel > Accounts > Profile Fields Editor.

Once you've located the editor you can start by clicking the green **New** button, this will enable the creation process. From here you'll customize the label, type, and options (if you have chosen the field type of **select**).

If you choose the field type of **select** you'll be required to enter at least one option, once you type in an option press **Enter** on your keyboard and a new option will be added.

Once you're satisfied with the customizations you made to the field you can click the orange **Save** button.

Now that you've created a field you'll want to move onto the next section detailing the permissions associated with fields.

{% hint style="info" %}
All existing profile fields will display on the preview profile on the right, this is how they'll appear in the member profile view.
{% endhint %}

### Managing Profile Field Permissions

Profile Field Permissions are essential to managing your fields for your members, permissions create "settings" for each field that accounts abide by when viewing profiles. Understanding these permissions will allow you to better leverage the use of Profile Fields.

Navigate to the Administrative Panel > Community > Ranks.

Select the rank that you'd like to edit and review the permissions below while selecting which permissions you'd like to grant to the rank.

<figure><img src="../../.gitbook/assets/CMS_ProfileFieldPerms.png" alt=""><figcaption><p>Sonoran CMS - Department Editor - Profile Fields Permissions</p></figcaption></figure>

Below we've outlined each permission and how they work with fields:

<table><thead><tr><th width="240">Permission</th><th width="509">Explanation</th></tr></thead><tbody><tr><td>Attaches to Profile</td><td>Granting this permission will attach this profile field to all member's profiles that hold this rank. This will allow anyone who views your profile to see it unless either of the next two permissions are applied.</td></tr><tr><td>Hides Field from Profile Owner</td><td>Granting this permission will hide the field from the member's profile that hold's this rank.</td></tr><tr><td>Require Mod Power to View on Profile</td><td>Granting this permission will require a member to have the "View Field on Other Profiles - Mod Power" in order to view the field on a profile.</td></tr><tr><td>Require Admin Power to View on Profile</td><td>Granting this permission will require a member to have the "View Field on Other Profiles - Admin Power" in order to view the field on a profile.</td></tr><tr><td>View Field on Other Profiles - Mod Power</td><td>Granting this permission will allow a member to view this field on a profile with "Mod Power" in mind. See above permissions for association.</td></tr><tr><td>View Field on Other Profiles - Admin Power</td><td>Granting this permission will allow a member to view this field on a profile with "Admin Power" in mind. See above permissions for association.</td></tr><tr><td>Allow Profile Owner to Edit</td><td>Granting this permission will allow the member that holds this rank to edit this field on their profile. If the "Hides Field from Profile Owner" permission is granted it will ignore this permission as it won't be visible.</td></tr><tr><td>Edit Field on Other Profiles</td><td>Granting this permission will allow the member that holds this rank to edit this field on any member profiles that their able to view.</td></tr></tbody></table>

### Editing Profile Fields

<figure><img src="../../.gitbook/assets/CMS_ProfileFields_InitiateEditingWide (1).png" alt=""><figcaption><p>Sonoran CMS - Member Profile - Hover on Profile Field</p></figcaption></figure>

While viewing a profile you can hover over them to determine if you have edit permissions or not. Hovering over a field that you can edit will display the tooltip as shown above.

<figure><img src="../../.gitbook/assets/CMS_EditProfileField_Nickname2.png" alt=""><figcaption><p>Sonoran CMS - Member Profile - Editing Profile Field</p></figcaption></figure>

Once you've clicked a field it will give you a pop-up to begin editing the field's value. Depending on what field type it is it will display the relevant field input type. Once you're satisfied with the fields new value you can click the green **Save** button to save it on the profile.

#### Text Array Profile Field Editing

The `text array` profile field allows for multiple strings of text to be added to an individual profile field, this is useful to store notes, Steam IDs, IPs, etc.

To edit, click the "Expand" expansion located under the Profile Field Label. This will display all entries of the array. Click in the middle of the entries or if you have none, you can press the "Click Me" button. Once you're satisfied with the field's new value(s) you can click the green **Save** button to save it on the profile.

{% hint style="info" %}
**TIP:** You can organize the order in which the entries are sorted by dragging and dropping them in the order of your preference.
{% endhint %}

<figure><img src="../../.gitbook/assets/CMS_EditProfileField_TextArray.png" alt=""><figcaption><p>Editing a Text Array Profile Field within Profile</p></figcaption></figure>
