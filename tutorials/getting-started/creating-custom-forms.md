---
description: >-
  Is it time for you to start creating custom forms for your community? Follow
  this page for more information!
---

# Creating Custom Forms

## Navigate to the Custom Form Editor

{% hint style="info" %}
Ensure that you've created at least one stage group outlined following both [Creating Custom Form Stages](creating-custom-form-stages.md) and [Creating Custom Form Stage Groups](creating-custom-form-stage-groups.md) guides.
{% endhint %}

#### Administrative Panel > Customization > Custom Form Editor

Within this "Custom Form Editor" panel you'll be able to create custom forms designed to your liking. Although this is very similar to the [Sonoran CAD Custom Records editor](https://info.sonorancad.com/tutorials/customization/creating-custom-record-and-report-types) there are some CMS specific features that have been added. For example, there are a few custom field types and premade sections that will further the functionality of your CMS.

![Administrative Panel Custom Form Editor - Create Fully Customizable Forms](../../.gitbook/assets/msedge\_xojS0pu11l.png)

{% hint style="info" %}
Whenever you create new custom forms you will need to explicitly give ranks permissions to the new custom forms to be used by other individuals. This can be done in the [Department Manager](creating-departments.md).

If a user has permissions for a specific form they'll be able to see those forms in the "Available Forms" panel which is accessible on the left side bar. If a user has the permission to approve or deny a specific form they'll be able to see those forms in the "Form Management" panel which is accessible on the left side bar.
{% endhint %}

### Premade Sections

Premade sections are pre-defined sections for forms that have underlying functions. These sections will allow you to leverage further possibilities in a custom form. Below is a list of all premade sections and how they work:

**Patrol Start/End**

This premade section allows your form submitters to import direct clock in entries, this will also allow integration with rosters via for the roster column type "Patrol Log Hours".

### Special Input Types

Special Input Types are inputs that have underlying functions. These input types will allow you to leverage further possibilities in a custom form. Below is a list of all special input types and how they work:

**Member Selector**

This special input type allows form submitters to select **ONE** user from your community, these users are formatted with preferred format set in Community Customization. This special input type can be referenced in a "auto member x" input.

#### Multi-Member Selector

This special input type allows form submitters to select **MULTIPLE** users from your community, these users are formatted with the preferred format set in Community Customization. This special input type **CANNOT** be referenced in a "auto member x" input.

#### Auto Member Types

These special input types allows input values to be automatically generated from a "Member Selector" input or from the form submitters account. When using these input in Custom Form creation ensure to select an option from the "Field/Source to Reference".

<figure><img src="https://i.imgur.com/fttyOpn.png" alt=""><figcaption><p>Sonoran CMS - Custom Form Editor - Auto Member &#x26; Member Selector Inputs</p></figcaption></figure>

<figure><img src="https://i.imgur.com/MXcCFBl.png" alt=""><figcaption><p>Sonoran CMS - Custom Form - Member Selector &#x26; Auto Member Input</p></figcaption></figure>

## Sorting Forms

__[_Introduced in v0.5.23_](../../roadmap/changelog.md#v0.5.23-beta-expected-release-1-9-2023)__

Sonoran CMS allows you to organize the order in which forms appear wherever they're listed, the main area forms are seen in a specific order would be when displaying the allowed forms in "Available Forms", this will allow you to organize the order of your forms for the best experience for your members.

<figure><img src="https://i.imgur.com/B1YZGi2.png" alt=""><figcaption><p>Sonoran CMS - Forms Editor - Sort Mode</p></figcaption></figure>

To enable "Sort Mode" you can click the blue outlined "Sort" button next to the rest of the action buttons. You must not be editing or creating a custom form, it won't allow you to sort during that action. Press the up and down buttons to order the forms in the order you wish, once it's to the ideal order you can click the "Save" button to save.

## Conditional Sections

__[_Introduced in v0.5.23_](../../roadmap/changelog.md#v0.5.23-beta-expected-release-1-9-2023)__

<figure><img src="https://i.imgur.com/XEnjqza.png" alt=""><figcaption><p>Sonoran CMS - Forms Editor - Conditional</p></figcaption></figure>

Conditional sections allow you to make an individual section visible based on conditions.

To enable a section to be "Conditional" simply switch the Conditional switch to "on" state. Once you do that a "Dependency" selector will appear, this will provide you with all eligible fields that can be used for conditional checks. Select the field that you want to be checked for the appearance of this section. Once you've chosen a field it'll provide you with an input, provide all value(s) that you wish to be checked upon on the field.

{% hint style="info" %}
If the field that will be checked is a **checkbox** it will simply check if it's "checked", there won't be any reason to provide a value.
{% endhint %}
