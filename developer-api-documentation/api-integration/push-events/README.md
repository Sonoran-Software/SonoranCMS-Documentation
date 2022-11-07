---
description: >-
  Sonoran CMS pushes event data to your community for further integration
  possibilities. Learn more below!
---

# Push Events

### <mark style="color:red;">NOT IMPLEMENTED ON PRODUCTION</mark>

{% hint style="warning" %}
All push events require the **Plus** version of Sonoran CMS or higher. For more information, see our [pricing ](broken-reference)page.
{% endhint %}

{% hint style="success" %}
Looking for VPS, web, or dedicated hosting? Check out our official [server hosting](broken-reference)!
{% endhint %}

## Configuring your Listener

### 1. Admin Panel Configuration

In the Administrative Panel, navigate to: Advanced > API Integration

Enter your server's public IP address and your game server's port. Sonoran CMS will send events to `http://ip:gameport/sonorancms/events` **utilizing your existing game port**.

## Developer Documentation

Our [integration plugins](broken-reference) may rely on these push events for full functionality. Interested in developing your own plugins? Expand the push event and API endpoint documentation in the left side drawer.
