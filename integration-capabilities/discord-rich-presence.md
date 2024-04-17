---
description: Our desktop app allows you to advertise your community right in Discord!
---

# Discord Rich Presence

{% hint style="danger" %}
**ATTENTION**: This feature is currently no longer within Sonoran CMS and will be reintroduced in a future update.
{% endhint %}

{% hint style="info" %}
Rich presence is included with all versions of Sonoran CMS, but customization requires the **Standard** plan or higher, and the **Pro** plan for complete customization with the icon.\
For more information, see our [pricing](../pricing/pricing-faq/) or view how to check your community [limits](../tutorials/administrative/view-your-limits.md).
{% endhint %}

## What is Discord Rich Presence?

When running our [desktop application](../download-the-app.md), Discord can automatically detect and display information about your community.

![Sonoran CMS - Discord Rich Presence](../.gitbook/assets/DiscordPTB\_Tzluj4WYgI.png)

## Customizing your Rich Presence

![Sonoran CMS - Discord Rich Presence Customization](../.gitbook/assets/electron\_U2tSqNbvS8.png)

### Customizing Buttons

Discord presence currently allows for two customizable buttons.

Navigate to Administrator Panel > Customization > Community Customization > Discord Rich Presence Customization

#### For communities on the **Standard** plan or higher:

\- Button #2 may be customized to any [Sonoran CAD](../other-products/sonoran-cad.md) or [Sonoran CMS](https://info.sonorancms.com/why-choose-sonoran-cms/why-choose-sonoran-cms) invitation link.\
\- Ex: `https://sonorancad.com/#/?comid=mycommunityid` or `https://sonorancms.com/#/?comid=mycommunityid`

#### For communities on the Pro plan:

\- Both buttons may be customized to any URL desired.\
\- The Icon and title can also be customized with a Discord developer application.

### Customizing the Icon

Communities on the **Pro** version may customize the rich presence icon:

#### 1. Create a new Discord Application

On [https://discord.com/developers/applications](https://discord.com/developers/applications) create a new application

![Discord Developer - New Application](<../.gitbook/assets/image (5) (1) (1) (1) (1).png>)

#### 2. Copy your Client ID

Under OAuth2, copy your `Client ID`&#x20;

![Discord Developer - Application Client ID](<../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1).png>)

#### 3. Add an Icon

Next, upload an icon for your new application. Be sure to copy down the name of the icon for later.

![Discord Developer - Application Icon](<../.gitbook/assets/image (2) (1) (1) (1) (1) (1).png>)

#### 4. Configure in Sonoran CMS

Back in the admin customization menu, we can paste the Discord application's Client ID and Icon name.

![Sonoran CMS - Custom Discord Presence Config](../.gitbook/assets/electron\_usiYhP7qa1.png)

Once saved, your Discord presence for all community members will reflect your custom icon, title, and buttons.

![Sonoran CAD - Custom Discord Presence View](../.gitbook/assets/DiscordPTB\_aQhYkv2DGy.png)

## Toggle On/Off Rich Presence <a href="#toggle-on-off-rich-presence" id="toggle-on-off-rich-presence"></a>

### Community Toggle <a href="#community-toggle" id="community-toggle"></a>

To hide the invite button for your community's Discord Rich Presence, simply leave the button text and URL blank.

### User Toggle <a href="#user-toggle" id="user-toggle"></a>

In the profile dropdown, users can toggle this display on or off for their individual desktop client.

![Sonoran CMS Profile Dropdown - Disable Discord's Rich Presence](../.gitbook/assets/electron\_KUr68rZjLj.png)
