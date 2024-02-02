---
description: >-
  Is it time for you to start creating custom forms for your community? Follow
  this page for more information!
---

# Creating Custom Forms

{% embed url="https://www.youtube.com/watch?v=HEJtdmqK4qk" %}

Navigate to the Custom Form Editor

`Administrative Panel` > `Forms`

Within the Form Editor panel you'll be able to create custom forms designed to your liking. Here you can craft your own forms using a variety of custom field types and premade sections and will further enhance the functionality of your CMS by eliminating the need for external form sites and keeping it all in-house.

![Administrative Panel Custom Form Editor - Create Fully Customizable Forms](../../.gitbook/assets/CMS\_FormBuilderRevamp.png)

{% hint style="info" %}
Whenever you create new custom forms you will need to explicitly give ranks permissions to the new custom forms to be used by other individuals. This can be done in the [Department Manager](../user-management/creating-departments.md).

If a user has permissions for a specific form they'll be able to see those forms in the "Available Forms" panel which is accessible on the left side bar. If a user has the permission to approve or deny a specific form they'll be able to see those forms in the "Form Management" panel which is accessible on the left side bar.
{% endhint %}

## Form Stages

Form Stages allow you to control the process (or stages) of your form. Depending on the `Form Type` you selected while creating the form, default form stages may automatically populate.&#x20;

Any form requires at least one stage in order to be used.

To begin customizing form stages, click the orange "Go To Submissions" button in the top right hand of the Form Editor page.

<figure><img src="../../.gitbook/assets/CMS_FormEditor3Arrow.png" alt=""><figcaption><p>Sonoran CMS - Form Editor - Go To Submissions</p></figcaption></figure>

When users submit the form, their submissions will show up underneath their corresponding stage, and administrators will drag-and-drop submissions under other stages to change the stage. This is covered in more detail in [Changing Form Stages](creating-custom-forms.md#changing-form-stages).&#x20;

You can add a new stage using the green plus button to the right, and you can customize any existing stage by clicking on the settings cog.

<figure><img src="../../.gitbook/assets/CMS_BlankFormStages.png" alt=""><figcaption><p>Sonoran CMS - Form Editor - Form Stage Template</p></figcaption></figure>

Within a stage's settings, there will be two tabs: `Info` and `Actions`. The `Info` tab allows you to customize the stage's name, description, color, and icon.&#x20;

<figure><img src="../../.gitbook/assets/CMS_FormStageInfo3.png" alt=""><figcaption><p>Sonoran CMS - Form Stage Editor - Info Tab</p></figcaption></figure>

The `Actions` tab allows you to add "actions" that are performed when a submission is moved to that stage and is explained in [the section below](creating-custom-forms.md#form-stage-actions).

After adding or editing a stage, you will be able to see the stage overview window, which allows you to easily drag-and-drop stages to re-order them. The first stage will always be the "Default" stage, i.e. the stage initially given upon submission.

<figure><img src="../../.gitbook/assets/CMS_FormStages2.png" alt=""><figcaption><p>Sonoran CMS - Form Stages - Overview Window</p></figcaption></figure>

If you have integrated your community with our [Discord Bot](https://info.sonoranbot.com/en/tutorials/getting-started), users can be pinged when a submitted form or application has changed stages.

### Form Stage Actions

You can add actions to any stage you create. Simply click the green plus button to add actions to a new stage.

<figure><img src="../../.gitbook/assets/CMS_FormStageActionsList2.png" alt=""><figcaption><p>Sonoran CMS - Form Stages - New Action</p></figcaption></figure>

The list of possible actions you can add is shown in the image below:

<figure><img src="../../.gitbook/assets/CMS_FormStageActionsAdd.png" alt=""><figcaption><p>Sonoran CMS - Form Stages - Actions List</p></figcaption></figure>

### Action Explanation: Change Submitter's Department/Rank

This action will allow you to modify the submitter's ranks. Additionally this allow you to set the ranks to also expire after a certain amount of time after they've been granted the rank by the action.

{% hint style="info" %}
Checks for rank expirations are done upon each fetch of the account and not **currently** periodically checked.
{% endhint %}

This allows you to select any rank you would like to add, and any rank you would like to remove. To apply an expiration to the rank(s) simply press the dropdown button located on the rank button, this will provide you with the option to access it's Expiration Settings.

<figure><img src="../../.gitbook/assets/CMS_FormsModifySubRank.png" alt=""><figcaption><p>Sonoran CMS - Stages Editor - Modify Submitter's Rank</p></figcaption></figure>

### Changing Form Stages

When users submit forms, their submissions will be displayed in a way that makes it simple to track what stage each submission is in.

To view all form submissions, click the orange `Go To Submissions` button in the top right hand of the Form Editor page.

<figure><img src="../../.gitbook/assets/CMS_FormEditor3Arrow.png" alt=""><figcaption><p>Sonoran CMS - Form Editor - Go To Submissions</p></figcaption></figure>

Once there, you can select the form whose submissions you'd like to manage on the left side, and then you will see all submissions and which stage they are in.

<figure><img src="../../.gitbook/assets/CMS_FormSubmissionManager.png" alt=""><figcaption><p>Sonoran CMS - Form Submission Manager</p></figcaption></figure>

If you have the **Admin Delete** permission for a given form, you can also delete any submissions by right clicking them and selecting `Delete Form`.

<figure><img src="../../.gitbook/assets/CMS_FormSubmissionManagerDelete.png" alt=""><figcaption><p>Sonoran CMS - Delete Form Submission</p></figcaption></figure>

## Sections & Fields

### Premade Sections

Premade sections are pre-defined sections for forms that have underlying functions. These sections will allow you to leverage further possibilities in a custom form. Below is a list of all premade sections and how they work:

**Time Clock Start/End**

This premade section allows your form submitters to import direct clock in entries, this will also allow integration with rosters via for the roster column type "Time Log Hours".

### Special Input Types

Special Input Types are inputs that have underlying functions. These input types will allow you to leverage further possibilities in a custom form. Below is a list of all special input types and how they work:

**Member Selector**

This special input type allows form submitters to select **ONE** user from your community, these users are formatted with preferred format set in Community Customization. This special input type can be referenced in a "auto member x" input.

#### Multi-Member Selector

This special input type allows form submitters to select **MULTIPLE** users from your community, these users are formatted with the preferred format set in Community Customization. This special input type **CANNOT** be referenced in a "auto member x" input.

#### Auto Member Types

These special input types allows input values to be automatically generated from a "Member Selector" input or from the form submitters account. When using these input in Custom Form creation ensure to select an option from the "Field/Source to Reference".

<figure><img src="https://i.imgur.com/MXcCFBl.png" alt=""><figcaption><p>Sonoran CMS - Custom Form - Member Selector &#x26; Auto Member Input</p></figcaption></figure>

## Sorting Forms

Sonoran CMS allows you to organize the order in which forms appear wherever they're listed, the main area forms are seen in a specific order would be when displaying the allowed forms in "Available Forms", this will allow you to organize the order of your forms for the best experience for your members.

To change the sort of your community's forms, you can change the "Sort Order" value for each form in its editor. Smaller values (including negative numbers) indicate that it should be sorted first. For example, if `Form 2` has a sort order of 0, and `Form 1` a sort order of 13, Form 2 would appear first.

## Conditional Sections

<figure><img src="../../.gitbook/assets/CMS_FormBuilderToggleConditional.png" alt=""><figcaption><p>Sonoran CMS - Forms Editor - Conditional Switch</p></figcaption></figure>

<figure><img src="../../.gitbook/assets/CMS_FormBuilderConditionals.png" alt=""><figcaption><p>Sonoran CMS - Forms Editor - Conditional</p></figcaption></figure>

Conditional sections allow you to make an individual section visible based on conditions.

To enable a section to be "Conditional" simply switch the Conditional switch to "on" state for the section you would like to make conditional. Once you do that a "Dependency" selector will appear, this will provide you with all eligible fields that can be used for conditional checks. Select the field that you want to be checked for the appearance of this section. Once you've chosen a field it'll provide you with an input, provide all value(s) that you wish to be checked upon on the field.

{% hint style="info" %}
If the field that will be checked is a **checkbox** it will simply check if it's "checked", there won't be any reason to provide a value.
{% endhint %}

## Limiting Form Submissions

Newly introduced limit settings allow you to limit the amount of submissions users in your community are able to complete. With these various settings you're able to lock it down within the last X days, ignore archived submissions and even add a cooldown in-between form submissions.

<figure><img src="../../.gitbook/assets/CMS_FormLimits.png" alt=""><figcaption><p>Sonoran CMS - Custom Form Editor - Limit Settings</p></figcaption></figure>

**# of Allowed Submissions**\
This number is the total amount of submitted versions of this form that are allowed for each community member. _Setting this to_ `-1` _will not limit form submissions at all._\
\
**Limit Submissions Within Last X Days**\
This number is the amount of days prior that submissions will be searched for, for limiting. For example, if this is set to `3` then it will only check for submissions 3 days prior from now. _Setting this to_ `-1` _will check all-time submitted versions of this form and not within the last X days._\
\
**Submission Cooldown**\
This number is the amount of days between submissions of this form. For example, if this is set to `3` then the member will have to wait three days between submitting versions of this form.\
\
**Ignore Archived Submissions**\
If checked this will not check for any submissions that are currently set to a stage that is the type of "Archived". So if a form is "Archived" it will not be searched for.

Forms that are blocked from being submitted at the current time will be shown this blocked view till the block is lifted based on the settings set for limiting. The member will not be able to submit any version of the form till they no longer meet any requirements to be blocked due to the settings.

## Custom Form Folders

Forms can now be organized within folders, these folders are purely for organizational purposes and doesn't serve any other function.

<figure><img src="../../.gitbook/assets/CMS_FormEditor2.png" alt=""><figcaption><p>Sonoran CMS - Form Editor - Folders</p></figcaption></figure>

To create a folder simply press the green plus button and select folder, this will prompt you to provide a name for the folder to then be created. Once the folder is created you can drag and drop forms into folders to easily organize them.

## Sharing Direct Submission Access

You can directly share a Custom Form via URL to be directly submitted on, if the URL is viewed it'll automatically navigate and provide the form to be submitted. You can get the direct submission access URL by viewing it in Available Forms and grabbing your browsers URL while viewing it or you can navigate to the Custom Form Editor. And before you select a form to edit just hit the settings cog then click green share button above the delete button.

<figure><img src="../../.gitbook/assets/CMS_FormCog (1).png" alt=""><figcaption><p>Sonoran CMS - Form Settings Button</p></figcaption></figure>

<figure><img src="../../.gitbook/assets/CMS_FormShare.png" alt=""><figcaption><p>Sonoran CMS - Share Forms Button</p></figcaption></figure>
