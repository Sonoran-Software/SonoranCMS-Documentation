---
description: >-
  Now that you've created your community and started to invite users you'll want
  to start creating departments. Learn more below
---

# Creating Departments

## Accessing the Department Manager

#### Administrative Panel > Customization > Department Manager

Within this "Department Manager" panel you'll be able to create departments and ranks for those departments, this will be the central panel for deciding permissions based on "ranks", when new, removed, or modified Custom Forms, Calendar Categories, and Rosters will be reflected with available permissions under each rank.

![Sonoran CMS Department Manager Panel - Add/Remove/Edit Departments & Ranks](https://i.imgur.com/arHqC68.png)

{% hint style="info" %}
Rank **Power** will be compared to other users as a global user power, this will be utilized to determine if you can modify other individuals. If your power is higher than another individual then you can modify them, if it's less then you cannot.
{% endhint %}

## Creating Departments Guide

### 1.  Fill Out Department Information

You will be prompted for three information fields:

1. Department Name (Example: Police Department)
2. Short Name (Example: PD)
3. Department Type (Primarily will use Primary Department)

### 2. Assign Default Department Permissions

<figure><img src="https://i.imgur.com/W9u5D4N.png" alt=""><figcaption><p>Sonoran CMS - Department Editor - Default Department Permissions</p></figcaption></figure>

This is where you'll need to assign permissions that you want all ranks within the department to inherit. These are the same set of permissions that ranks are able to get assigned but will be applied to all ranks upon permission evaluation.

### 3. Add Ranks

Click the green "Add Rank" button.

This will create a new section where you'll need to specify both of the following fields:

1. Rank Name (Example: Chief of Police)
2. Power (Example: 75) _Look above at the blue informational hint for **Power** explanation._
3. "P" & "S" Buttons (This will specify if a rank can be assigned to someone as a primary or secondary rank only.

### 4. Customize Rank Cosmetic Styling

<figure><img src="https://i.imgur.com/etO5NPo.png" alt=""><figcaption><p>Sonoran CMS - Department Editor - Rank Cosmetic Customization</p></figcaption></figure>

Ranks are able to be customized to the styling that best fits your community, customize the color and icon associated with each rank. You can specify common color names or custom hex colors.

{% hint style="info" %}
The rank icon can be an image if you specify `img:` at the start of the image URL, for example: `img:https://i.imgur.com/RE73BNW.png`
{% endhint %}

### 5. Assign Permissions

This is where you'll need to assign permissions for the system under "CMS Permissions"

* **"Form Permissions"** is for the custom forms
* **"Calendar Permissions"** are based on the calendar categories made in Administrative Panel > Customization > Customization
* **"Roster Permissions"** are based on the custom records made in Administrative Panel > Customization > Custom Roster Editor.
* **"Server Permissions"** are based on the API Integration servers made in Administrative Panel > Advanced > API Integration.
* **"Profile Fields Permissions"** are based on the Profile Fields created in the Administrative Panel > Customization > Profile Fields Editor.

### 6. Add Department

Once you've created your department and ranks to your liking with the specific permissions that you would like you will need to hit the green "Add" button located above the Department Information. This will save and add the department to the system.
