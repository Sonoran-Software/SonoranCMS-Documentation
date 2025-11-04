---
description: >-
  Looking to use your own domain name with Sonoran CMS? We've made it easy for
  you!
---

# Custom Domain / Vanity URL

{% embed url="https://www.youtube.com/watch?v=JwgKe_CHwp4" %}

{% hint style="warning" %}
Only the **Community Owner** will have access to change and view Custom Domain settings.
{% endhint %}

{% hint style="warning" %}
Custom domains require the **pro** version.\
For more information, see our [pricing](../../pricing/pricing-faq/) or view how to check your community [limits](../administrative/view-your-limits.md).
{% endhint %}

{% hint style="success" %}
Looking for VPS, web, or dedicated hosting? Check out our official [server hosting](https://docs.sonoransoftware.com/promotions/fivem-hosting)!
{% endhint %}

## Vanity URL's

Each community gets a **FREE** vanity URL, vanity URLs allow all communities to get access to the community homepage without a login.

You can also [customize your Community ID](community-branding-and-settings.md#community-id-and-vanity-url).

Your community's vanity URL can be found in your `Administrative Panel > Custom Domain`.

<figure><img src="../../.gitbook/assets/Screenshot (307).png" alt=""><figcaption></figcaption></figure>

The vanity URL will take users to the home page created in the website builder.

## Custom Domain

{% hint style="warning" %}
Custom Domain requires a **Pro** subscription.
{% endhint %}

### 1. Enter your Domain Name

This can be a root domain `example.com` or a subdomain `cms.example.com`

<figure><img src="../../.gitbook/assets/Screenshot (307) (1).png" alt=""><figcaption></figcaption></figure>

### 2. Configure DNS Records for your Domain

{% hint style="warning" %}
**If you are unsure how to add a DNS record, you will need to contact your domain registrar.**
{% endhint %}

Copy and paste the values to add three DNS records (two `CNAME` records and one `TXT` record). This verifies your domain ownership, community ownership, and redirects traffic on your domain to the CMS.

<figure><img src="../../.gitbook/assets/Screenshot (308).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
**Some DNS providers are different!**\
\
Check with your DNS provider if using a "root domain" (i.e. `example.com` instead of `cms.example.com`) to see what to add as the `name`. \
\
Typically it is `@` or left blank.
{% endhint %}

The example record below sets `cms.example.com` as the custom login page URL.

<figure><img src="../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption><p>Cloudflare - DNS Record </p></figcaption></figure>

{% hint style="info" %}
**Cloudflare Users:** Be sure to have the **DNS record proxy DISABLED** - and set to `DNS Only`.
{% endhint %}

If you are using Sonoran Servers, our company's server hosting, for your domain name please note the differences in how to enter the settings pictured below. Each DNS provider is a bit different and requires different input for the Host Name.&#x20;

Typically the Host Name is left blank or in this case a `@` is used to point the record at the root domain name of "`sonoranroleplay.com`"

### 3. Save the Custom Domain

{% hint style="warning" %}
When updating or changing an existing DNS record, it may take some time for the change to propagate (based on your TTL).\
\
You can try running `ipconfig /flushdns` in a Windows CMD window and restart your browser. Otherwise, you can test with other browsers/devices/users while you wait.
{% endhint %}

Press **Set Custom Domain** in the CMS to save. Your new custom domain name will be shown below your vanity URL.

<figure><img src="../../.gitbook/assets/image (4).png" alt="" width="563"><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (3).png" alt="" width="563"><figcaption></figcaption></figure>

## Troubleshooting

### I can't see other communities when using a custom domain

Custom domains prevent other Sonoran CMS communities from being visible. You will need to use the root `sonorancms.com` domain to view multiple communities at once.
