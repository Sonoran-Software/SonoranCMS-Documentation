---
description: >-
  Looking to use your own domain name with Sonoran CMS? We've made it easy for
  you!
---

# Custom Domain / Vanity URL



{% hint style="warning" %}
Only the **Community Owner** will have access to change and view Custom Domain settings.
{% endhint %}

{% hint style="warning" %}
Custom domains require the **pro** version.\
For more information, see our [pricing](../../pricing/pricing-faq/) or view how to check your community [limits](../administrative/view-your-limits.md).
{% endhint %}

{% hint style="success" %}
Looking for VPS, web, or dedicated hosting? Check out our official [server hosting](../../other-products/server-hosting.md)!
{% endhint %}

## Vanity URL's

Each community gets a **FREE** vanity URL, vanity URL's allow all communities to get access to the community homepage without a login.

Your community's vanity URL can be found in your `Administrative Panel` > `Advanced` > `Custom Domain`.

<figure><img src="../../.gitbook/assets/image (16).png" alt="" width="375"><figcaption></figcaption></figure>

The vanity URL will take users to the home page created in the website builder.

<figure><img src="../../.gitbook/assets/image (11).png" alt="" width="375"><figcaption></figcaption></figure>

## Custom Domain

{% hint style="warning" %}
Custom Domain requires a **Pro** subscription.
{% endhint %}

### 1. Enter your Domain Name

This can be a root domain `sonoranroleplay.com` or a subdomain `cms.sonoranroleplay.com`

<div align="center" data-full-width="false">

<figure><img src="../../.gitbook/assets/image (5) (2).png" alt="" width="375"><figcaption></figcaption></figure>

</div>

### 2. Add a CNAME Record for your Domain

{% hint style="warning" %}
**If you are unsure how to add a DNS record, you will need to contact your domain registrar.**\
Or, you may purchase a new domain name with [Sonoran Servers](https://sonoranservers.com/cart.php?a=add\&domain=register).
{% endhint %}

<figure><img src="../../.gitbook/assets/image (1) (4).png" alt="" width="375"><figcaption></figcaption></figure>

In your domain's DNS records, add a `CNAME` type record with:

* `name` set to the subdomain or `@` for the root domain
* `content` set to `login.sonorancms.com`.

The example record below sets `cms.sonoranroleplay.com` as the custom login page URL.

![Cloudflare - DNS Record ](<../../.gitbook/assets/unknown (10).png>)

{% hint style="info" %}
**Cloudflare Users:** Be sure to have the **DNS record proxy DISABLED** - and set to `DNS Only`.
{% endhint %}

#### 3. Save the Custom Domain

{% hint style="warning" %}
When updating or changing an existing DNS record, it may take some time for the change to propagate (based on your TTL).\
\
You can try running `ipconfig /flushdns` in a Windows CMD window and restarting your browser. Otherwise, you can test with other browsers/devices/users while you wait.
{% endhint %}

Press `Set Custom Domain` in the CMS to save.

<figure><img src="../../.gitbook/assets/image (11) (3).png" alt="" width="375"><figcaption></figcaption></figure>

Your new domain name will be shown below your vanity URL.

<figure><img src="../../.gitbook/assets/image (18).png" alt="" width="375"><figcaption></figcaption></figure>

## Troubleshooting

### I can't see other communities when using a custom domain

Custom domains prevent other Sonoran CMS communities from being visible. You will need to use the root `sonorancms.com` domain to view multiple communities at once.
