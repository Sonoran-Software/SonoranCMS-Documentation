---
description: >-
  Just like Google Drive or Microsoft Office, create and store documents in your
  community's drive!
---

# Drive & Documents

{% embed url="https://www.youtube.com/watch?v=S7do0P7pJJU" %}

<figure><img src="../.gitbook/assets/image (1) (1) (1).png" alt=""><figcaption><p>Sonoran CMS - Document Drive Management</p></figcaption></figure>

With your drive, you're able to create files and folders for your community. These files are completely customizable, and have a similar style editor to the Microsoft Office suite

{% hint style="warning" %}
This feature is currently experimental. It is known that phones and other small devices may not have the best compatibility with editing/viewing files
{% endhint %}

![Document Editor](https://i.imgur.com/zdVfQRQ.png)

## Your Drive

You can navigate to your drive using the `Drive` button on the menu sidebar. Once in the drive, you'll see all create documents! If you have permission to edit/create documents, then there will be some additional buttons for you

To view a document, simply click it in either grid or list view. This will show a read-only view of the document

To quick manage Drive items you can right click the item, it'll provide a menu of actions that can be performed on that item.

<div align="left">

<figure><img src="https://i.imgur.com/Fg5MtWt.png" alt=""><figcaption><p>Sonoran CMS - Drive - Quick Manage (Right Click)</p></figcaption></figure>

</div>

### Folders

Folders help you organize your community's drive! To create folders, just use the green plus button on the top, then drag n drop files into the folders. You can also drag n drop files on the breadcrumbs on the top

![](https://i.imgur.com/XQX9D1D.png)

To move a file without drag n drop, you can use the blue arrow button on a document and select the folder in the popup

Folders can have permissions associated with them to mass organize files with permissions. To edit a folder's permissions/share type you can right click the folder and select "Change Permissions". All items within the folder that have the Share Type of "Inherit Parent Folder" will inherit the Share Type & Permissions associated with the folder.

### View Mode

You can change the view mode between grid and list by using the toggle button on the Drive's toolbar

<div align="left">

<img src="https://i.imgur.com/HHHUJsx.png" alt="Change View">

</div>

![Drive List View](https://i.imgur.com/mnoLjLa.png)

### Document Types

You're able to create multiple document types, from presentations to excel sheets to word files!

<div align="left">

<img src="https://i.imgur.com/GhvgwCh.png" alt="Create File Dialog">

</div>

### Document Actions

If you have access to modify documents, then you'll be able to create/edit/delete them.

* To edit a document, press the orange button with a pen and paper on the document
* To delete a document, press the red trash can on the document
* To create a document, press the green plus button on the top right (next to the view mode selector)

## Editing a Document

![Word Document Editor](https://i.imgur.com/7L9wLdS.png)

Editing documents is fairly easy! On the editor page, you have the main editor, a section to rename, and a section to change share settings

To rename the page, simply type the new name and press the checkmark.

{% hint style="info" %}
**Tip:** You can view, edit, rename, etc. directly from the Drive view by right clicking a drive item. This will provide several options that are available for that item.
{% endhint %}

### Share Settings

<figure><img src="https://i.imgur.com/8kY6U72.png" alt=""><figcaption><p>Sonoran CMS - Drive - Share Settings Dialog</p></figcaption></figure>

To change share settings, simply right click the green hamburger button on the drive item and select "Share Settings". If you're editing the document already you can simply click the "Share Settings" button on the top.

**Ranks with All Drive Access**

This shows all ranks that have the "Modify Documents (Drive)" permission, this will automatically grant them permission to modify this drive item.

**Ranks with Access Permissions**

This shows all ranks that have been added to have direct view or edit access regardless of what the General Access share type is set to. If a user has a rank listed here the drive item will show in their Drive as well.

There's also a "Inherit Parent Folder Access Permissions" option for all nested drive items, this will inherit the parent folder's access permissions ranks.

**General Access**

This allows for various share settings to be applied to the drive item from a single selection. There's various options that will grant members access automatically, the options are the following:

_Restricted_

This will only utilize the Ranks with All Drive Access and Ranks with Access Permissions to determine if they have access to the document.

_Anyone - Not yet accessible, pending update v0.5.13_

This will allow ANYONE with the share link provided with the button to either view and/or edit the file, depending on what it set. You can click the icon on the left to either hide or show the drive item in your community member's Drive, if you have it hidden they'll still have access to either view or edit depending on what's set directly through the share link. Someone who is not apart of your community's CMS or even signed into Sonoran CMS will be able to view and/or edit through the share link provided.&#x20;

_Active members with this link_

This will allow all users with the community status of "ACTIVE" not "PENDING" to either view or edit the drive item, depending on what's set. You can click the icon on the left to either hide or show the drive item in their Drive, if you have it hidden they still have access to either view or edit depending on what's set directly through the share link.

_Active & pending members with this link_

This will allow all users within the community to either view or edit the drive item, depending on what's set. You can click the icon on the left to either hide or show the drive item in their Drive, if you have it hidden they still have access to either view or edit depending on what's set directly through the share link.

_Inherit Parent Folder General Access_

This will inherit the parent folder's general access settings, this will simply inherit whatever option from above the folder is set to.

{% hint style="info" %}
**Inherit Parent Folder General Access** General Access Share Type cannot be set for any Drive item that is in the root (Home).
{% endhint %}

### Sensitive Documents

You can also change the sensitivity of the document. With sensitive mode enabled, viewers will not be able to download, print, or copy the document. A watermark will also be added.

<div align="left">

<img src="../.gitbook/assets/image (15).png" alt="Sonoran CMS - Sensitive Document Toggle">

</div>

### Saving

Due to limitations with the editor, it's not able to save automatically. To save, you can press the floppy-disk icon on the top left or press `CTRL+S`

<div align="left">

<img src="https://i.imgur.com/ZLlc5og.png" alt="">

</div>

A warning will be shown if you try to leave the page with unsaved changes

### Multi-user editing

The editor allows multiple people to edit the same document at the same time! No special instructions needed, all you need to do is load up the editor and it'll handle the magic

## Uploading / Migrating Files

<figure><img src="https://i.imgur.com/ndNb0VX.png" alt=""><figcaption><p>Sonoran CMS - Drive - Upload a Document</p></figcaption></figure>

Sonoran CMS easily allows you to upload individual files or multiple files via a ZIP. This will allow your community to easily migrate community documents and assets easily over from standard document hosting services such as Google Drive!

### Uploading Individual Files

As shown in the image above you'll want to navigate to the Sonoran CMS Drive, locate the blue upload cloud button and click it.\
\
From there, you'll be able to select a file with the following type:

* `.docx` Document
* `.xlsx` Spreadsheet
* `.pptx` Presentation
* `.pdf` PDF
* `.mp3` Audio
* `.wav` Audio
* `.rpf` GTA Archive

<figure><img src="https://i.imgur.com/BCEiVpM.png" alt=""><figcaption><p>Sonoran CMS - Drive - File Uploader</p></figcaption></figure>

Once you select the file(s) you'd like to upload click the white cloud upload icon to the right of "Upload Document". This will now upload the file and alert you once it's completed.

### Uploading Batch Files / ZIP

As mentioned above you can upload / migrate complete directories from standard document hosting services such as Google Drive.

While in the Sonoran CMS Drive locate the blue cloud upload button in the top right area of the drive, click it and begin selecting file(s).

From there you'll be able to select a ZIP file, keep in mind that the following file types will be the only ones recognized by Sonoran CMS once uploaded.

* `.docx` Document
* `.xlsx` Spreadsheet
* `.pptx` Presentation
* `.pdf` PDF
* `.mp3` Audio
* `.wav` Audio
* `.rpf` GTA Archive

<figure><img src="https://i.imgur.com/L8gUSEA.png" alt=""><figcaption><p>Sonoran CMS - Drive - ZIP Upload Alerts</p></figcaption></figure>

Once you select the file(s) you'd like to upload click the white cloud upload icon to the right of "Upload Document". You will get alerted for all the files that were successfully uploaded from the ZIP and which ones were rejected with reason.

### Migrate Files from Google Drive

Migrating files from Google Drive to the Sonoran CMS is very easy! All you need to do is go to your Google Drive, locate the directory or select a group a files that you're wanting to migrate and right click, you'll be given several options, click the "Download" option. This will now generate and download a ZIP file containing all files/directories that you selected. Now just follow the directions that were put above to complete migrating over files.

<figure><img src="https://i.imgur.com/8TIowQH.png" alt=""><figcaption><p>Google Drive - Right Click Options</p></figcaption></figure>

## Publicly Accessible Files

<figure><img src="https://i.imgur.com/OJ4jcH5.png" alt=""><figcaption><p>Sonoran CMS - Publicly Accessible File Preview</p></figcaption></figure>

Sonoran CMS Drive allows files to be publicly viewable and editable with a simple share setting change and sharing the generated share link. When a file's general access is set to "Anyone with this link" it will allow anyone with that generated link access to view or edit the file. This will not require the user to sign in or to be part of your community.

<figure><img src="https://i.imgur.com/pg9rokQ.png" alt=""><figcaption><p>Sonoran CMS - File Share Settings for Anyone with this link</p></figcaption></figure>

If a user of your community accesses the public generated link they will be automatically redirected to view the file in your community's Drive.

## Drive Downloads

There are several file types that the Sonoran CMS Drive accepts but only handles them as _downloadable_ content that isn't for viewable use. The following file types are currently supported for _downloadable content_:

* GTA Archive | .rpf
* Audio | .wav, .mp3
* ZIP | .zip
* PDF | .pdf

<figure><img src="https://i.imgur.com/Qj42DMV.png" alt=""><figcaption></figcaption></figure>

When one of these file types are uploaded they'll be given different options to interact with, as shown in the image you're able to download, remove or modify the share settings. Additionally you're able to copy a direct download link to share among peers. If someone is able to see the file in their Drive they're able to download it.
