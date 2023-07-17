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

Each community gets a **FREE** vanity URL, vanity URL's allow all communities to get access to the custom login page system. When visiting your community's vanity URL you will be greeted with a custom login page as shown below with the community's image.

Your community's vanity URL can be found in your **Administrative Panel** > **Advanced** > **Custom Domain**.

{% hint style="info" %}
**Note:** Vanity URL's are based on your community ID, if you change your community ID your vanity URL will also change.
{% endhint %}

## Custom Login Page

The custom login page allows your community members to register, sign-in, and access your CMS all on your own domain!

![Sonoran CMS Custom Domain Login Page Example](https://i.imgur.com/0uGuRyU.png)

## Custom Domain

{% hint style="warning" %}
Custom Domain requires a **Pro** subscription.
{% endhint %}

### 1. Add a CNAME Record for your Domain

{% hint style="warning" %}
**If you are unsure how to add a DNS record, you will need to contact your domain registrar.**\
Or, you may purchase a new domain name with [Sonoran Servers](https://sonoranservers.com/cart.php?a=add\&domain=register).
{% endhint %}

In your domain's DNS records, add a `CNAME` type record with the `name` set to any desired subdomain and the `content` set to `login.sonorancms.com`.

The example record below sets `cms.sonoranroleplay.com` as the custom login page URL.

![Cloudflare - DNS Record ](<../../.gitbook/assets/unknown (10).png>)

{% hint style="info" %}
**Cloudflare Users:** Be sure to have the **DNS record proxy DISABLED** - and set to `DNS Only`.
{% endhint %}

### 2. Set the Domain Name in Sonoran CMS

In the Sonoran CMS Administrative Panel > Advanced > Custom Domain, set the custom domain URL.\
This should not contain any `https://` or other extensions.

Don't forget to press save!\
Users can now visit this custom domain to view the CMS with a custom login page.

![Sonoran CMS - Custom Domain URL](../../.gitbook/assets/brave\_hWyhBJOQAb.png)

{% hint style="warning" %}
When updating or changing an existing DNS record, it may take some time for the change to propagate (based on your TTL).\
\
You can try running `ipconfig /flushdns` in a Windows CMD window and restarting your browser. Otherwise, you can test with other browsers/devices/users while you wait.
{% endhint %}

## Troubleshooting

### I can't see other communities when using a custom domain

Custom domains prevent other Sonoran CMS communities from being visible. You will need to use the root `sonorancms.com` domain to view multiple communities at once.
