---
description: >-
  Sonoran CMS pushes event data to your community for further integration
  possibilities. Learn more below!
---

# Push Events

### <mark style="color:red;">NOT IMPLEMENTED ON PRODUCTION</mark>

{% hint style="warning" %}
All push events require the **Plus** version of Sonoran CMS or higher. For more information, see our [pricing ](https://github.com/Sonoran-Software/SonoranCMS-Documentation/blob/master/developer-api-documentation/api-integration/push-events/broken-reference/README.md)page.
{% endhint %}

{% hint style="success" %}
Looking for VPS, web, or dedicated hosting? Check out our official [server hosting](https://github.com/Sonoran-Software/SonoranCMS-Documentation/blob/master/developer-api-documentation/api-integration/push-events/broken-reference/README.md)!
{% endhint %}

## Configuring your Listener

### 1. Admin Panel Configuration

In the Administrative Panel, navigate to: Advanced > API Integration

Enter your server's public IP address and your game server's port. Sonoran CMS will send events to `http://ip:gameport/sonorancms/events` **utilizing your existing game port**.

## Developer Documentation

Our [integration plugins](https://github.com/Sonoran-Software/SonoranCMS-Documentation/blob/master/developer-api-documentation/api-integration/push-events/broken-reference/README.md) may rely on these push events for full functionality. Interested in developing your own plugins? Expand the push event and API endpoint documentation in the left side drawer.
