---
description: Customize your community's settings, branding, information, and more!
---

# Community Branding and Settings

{% embed url="https://www.youtube.com/watch?v=Un9AIFXzZqQ" %}

## Branding Removal

Looking to remove Sonoran CMS branding on your website?

{% content-ref url="../../pricing/pricing-faq/branding-removal.md" %}
[branding-removal.md](../../pricing/pricing-faq/branding-removal.md)
{% endcontent-ref %}

## Community Information

The admin customization info section allows you to customize your community's image, name, and more! These settings can be found by navigating to `Administrative Panel` > `Customization`

![Sonoran CMS - Community Customization](<../../.gitbook/assets/Screenshot (301).png>)

| Community Logo        | <p>A link to your community's logo.</p><p>This will be displayed on your community card, community dashboard, and more!</p>                                                          |
| --------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Community Name        | <p>This is your community's name.</p><p>This will be displayed on your community card and community dashboard.</p>                                                                   |
| Community Subtitle    | This is the text displayed below your community name on your community card.                                                                                                         |
| Name Customizations   | <p>This allows customization of how community names are formatted. Many RP communities use a specific naming style.<br>Example: <strong>Format:</strong> <code>{uniqueId}</code></p> |
| Allowed Login Methods | This controls which login methods are available for signing into the CMS community. For example, if you only want users to log in with Discord, you can disable all other options.   |
| On Join Actions       | This configures automatic actions that occur when new members join your community.                                                                                                   |

{% hint style="info" %}
**Admin Icon** will display a cog icon next to a user's Notification Center icon in the top right of the toolbar.
{% endhint %}

## Community ID and Vanity URL

{% hint style="warning" %}
Custom community IDs require the **Standard** version of Sonoran CMS or higher.\
For more information, see our [pricing](https://sonorancms.com/#/pricing) or view how to check your community [limits](../administrative/view-your-limits.md).
{% endhint %}

### **Looking to change your community ID?**

Navigate to **Administrative Panel** > **Limits**\
Click the **Change Community ID** button and enter your new community ID.

Community IDs also customize your [vanity URL](custom-domain.md#vanity-urls).\
`ID.sonorancms.com`

![Sonoran CMS Community Limits - Changing Community ID](<../../.gitbook/assets/Screenshot (303).png>)

## Allowed Login Methods

Some communities may only want specific login methods to be available to their users. Each method can be enabled or disabled in the customization menu.

<figure><img src="../../.gitbook/assets/image (72).png" alt=""><figcaption></figcaption></figure>

### Naming Format

In the `Name Customizations` area, you can also set the automatic naming format for your community. The naming format determines how a user's name is displayed in the community (e.g. on their profile, form submissions, etc.).

<figure><img src="../../.gitbook/assets/CMS_NamingFormatExample.png" alt="" width="355"><figcaption><p>Sonoran CMS - Naming Format Example</p></figcaption></figure>

In the above image, you can see that the name is displayed on the profile as `John Doe | 1A`. In this case, the user's Community Name is set as `John Doe`, and this user has an Identifier of `1A`. To display those together like this, you would set the naming format to `{comName} | {identifier}`.

<figure><img src="../../.gitbook/assets/Screenshot (304).png" alt=""><figcaption><p>Sonoran CMS - Naming Format</p></figcaption></figure>

<table><thead><tr><th>User Information</th><th>Naming Format Variable</th><th data-hidden></th><th data-hidden></th></tr></thead><tbody><tr><td>Community Name</td><td>{comName}</td><td></td><td></td></tr><tr><td>Identifier</td><td>{identifier}</td><td></td><td></td></tr><tr><td>Unique ID</td><td>{uniqueId}</td><td></td><td></td></tr></tbody></table>

### Discord Name Sync

With the Sonoran Bot integration, you can enforce your CMS name format in your Discord Guild(s)!

{% embed url="https://info.sonoranbot.com/tutorials/usage/settings#namesync-settings" %}

## Member On Join Actions

Sonoran CMS lets you define what happens when users join your community — from assigning specific ranks automatically to sending a welcome message via Discord DM. You have complete control over the actions that occur when new members join.

<figure><img src="../../.gitbook/assets/Screenshot (305).png" alt=""><figcaption><p>Sonoran CMS - Member On Join Settings - Button Location</p></figcaption></figure>

<figure><img src="../../.gitbook/assets/Screenshot (306).png" alt=""><figcaption><p>Sonoran CMS - Member On Join Settings</p></figcaption></figure>
