---
description: Generate custom short URLs with your CMS vanity or custom domain!
---

# URL Shortener

<figure><img src="../../.gitbook/assets/rectangle_linkshort.png" alt=""><figcaption><p>Sonoran CMS - URL Shortener</p></figcaption></figure>

{% hint style="danger" %}
**The URL Shortener is only enabled with a Pro Subscription!**

Learn more about our [paid plans](../../pricing/pricing-faq/create-and-manage-a-subscription.md).
{% endhint %}

## What are Short URLs?

Create friendly, short URLs for anything in your community!

The URL shortener takes any link and converts it to a short and readable format!\
Ex: `https://discord.com/invite/123456` -> `mycommunity.com/discord`

## Creating a Short URL

### New Short URL

To forward `https://discord.com/invite/123456` to our [custom domain](../customization/custom-domain.md#custom-domain)'s `mycommunity.com/discord`

1. Enter the existing URL `https://discord.com/invite/123456`
2. Enter the new short URL path `discord`
3. (Optional) add a description `Discord invite link`

<figure><img src="../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" width="365"><figcaption></figcaption></figure>

After adding the new short URL, it will be viewable, searchable, and copyable in the table below.

<figure><img src="../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" width="375"><figcaption></figcaption></figure>

### Domain Formats

The CMS supports three types of short URL formats:

* [Custom Domain](../customization/custom-domain.md#custom-domain): `customdomain.com/shorturl`
* [Custom Subdomain](url-shortener.md#custom-subdomains): `example.customdomain.com/shorturl`
* [Vanity Domain](../customization/custom-domain.md#vanity-urls): `communityid.sonorancms.com/shorturl`
* Long Domain: `sonorancms.com/com/communityuuid/shorturl`

The custom path will work on all three of these options. The toggle simply allows you to select which format you are copying.

## Custom Subdomains

Subdomains are extensions of your custom domain and are used to organize or separate different sections of a website (e.g., info.customdomain.com).

### Adding A Subdomain

<details>

<summary>1. Click to Add a New Subdomain</summary>

Click the `+` icon next to the short URL type selector.

<img src="../../.gitbook/assets/image (52).png" alt="URL Shortener: Add Subdomain" data-size="original">

</details>

<details>

<summary>2. Enter the Desired Subdomain</summary>

Enter your desired subdomain for your community's [configured custom domain](../customization/custom-domain.md#custom-domain).

Here, the subdomain is `links` and the custom domain is `sonoranrp.com`

<img src="../../.gitbook/assets/image (53).png" alt="URL Shortener: Subdomain Url" data-size="original">

</details>

<details>

<summary>3. Copy and Add DNS Records</summary>

Copy the information from the panel to create a `CNAME` and `TXT` DNS record.

<img src="../../.gitbook/assets/image (57).png" alt="" data-size="original">

The examples below show DNS management via Cloudflare.\
If you are unsure how to add a DNS record, contact your domain provider.

\
If you are using Cloudflare, **DISABLE the proxy mode** and set it to `DNS Only`

<img src="../../.gitbook/assets/image (55).png" alt="Cloudflare: Subdomain CNAME Record" data-size="original"><img src="../../.gitbook/assets/image (56).png" alt="Cloudflare: Subdomain TXT Record" data-size="original">

</details>

<details>

<summary>4. Save and Use Subdomain</summary>

After saving your new `CNAME` and `TXT` record, click `Add Link Subdomain` to verify the DNS records.

Note: _Depending on your DNS provider, there may be a cache delay before the DNS records are detected._

<img src="../../.gitbook/assets/image (58).png" alt="" data-size="original">

You can now select the custom domain in the `URL Type` drop-down to be used when creating a new short URL.

![](<../../.gitbook/assets/image (60).png>)

</details>

## Reserved Paths

Sonoran CMS has several internal URL paths that can not be overridden by a custom short URL.

Sonoran CMS will also not allow you to override an existing [website slug](../community-website/website-builder.md) with a custom short URL.

```
admin
index
login
logout
signup
gallery
menu
event
account
oauth/discord
oauth/sonoran
oauth/apple
drive/file
game/menu
game/qbcore
profile
roster
forums
forums/topics
calendar
forms
```

These paths are restricted only in their absolute form. Appending additional paths to these are allowed. For example:

A short URL can **NOT** be: `example.com/forms`

However, a short URL **CAN** be: `example.com/forms/civ`
