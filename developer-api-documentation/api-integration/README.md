---
description: >-
  Sonoran CMS's open API endpoints allow you to utilize the whitelist system,
  clock in and out users, etc.
---

# 📖 API Integration

## Sonoran JS - NPM Library

Sonoran CMS offers a complete Node API library from NPM!

`npm i @sonoransoftware/sonoran.js`

[Learn more about our NPM library](https://www.npmjs.com/package/@sonoransoftware/sonoran.js)!

## How are API calls sent?

All API calls are sent via an HTTP POST with a JSON formatted body.

## Can I integrate this with my gamemode/framework?

Yes, our API calls can be integrationed into nearly any gamemode with nearly any programming language.

We provide several drag-and-drop resources written in JS/TS.



You can also write your own script using our API endpoints:

{% content-ref url="api-endpoints/" %}
[api-endpoints](api-endpoints/)
{% endcontent-ref %}

## Are there rate limits?

Yes, Sonoran CMS will automatically block any malicious or spammed traffic. While we don't publicly publish these limits, it's not best to not make more than one call per second for an extended period of time.

{% content-ref url="getting-started/" %}
[getting-started](getting-started/)
{% endcontent-ref %}
