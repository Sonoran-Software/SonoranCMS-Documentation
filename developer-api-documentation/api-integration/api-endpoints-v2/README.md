---
description: REST-style v2 API documentation for Sonoran CMS.
---

# API Endpoints V2

{% hint style="info" %}
The v2 API uses `Authorization: Bearer <api key>`, standard HTTP verbs, proper status codes, and a consistent success envelope:

```json
{
  "success": true,
  "data": {},
  "meta": {
    "timestamp": "2026-04-14T00:00:00.000Z",
    "path": "/v2/community"
  }
}
```

Errors are returned as `application/problem+json`.
{% endhint %}

Base URL example: `https://api.sonorancms.com/v2`

Each section below expands into individual endpoint pages.

## Rate Limits

{% content-ref url="rate-limits.md" %}
[rate-limits](rate-limits.md)
{% endcontent-ref %}

## Available Sections

### Libraries

Use the official Sonoran SDK libraries if you want package-managed helpers for the v2 API.

{% content-ref url="libraries.md" %}
[libraries](libraries.md)
{% endcontent-ref %}

### General

{% content-ref url="general/" %}
[general](general/)
{% endcontent-ref %}

### Accounts

{% content-ref url="accounts/" %}
[accounts](accounts/)
{% endcontent-ref %}

### Servers

{% content-ref url="servers/" %}
[servers](servers/)
{% endcontent-ref %}

### Events

{% content-ref url="events/" %}
[events](events/)
{% endcontent-ref %}

### Forms

{% content-ref url="forms/" %}
[forms](forms/)
{% endcontent-ref %}

### Rosters

{% content-ref url="rosters/" %}
[rosters](rosters/)
{% endcontent-ref %}

### Disciplinary

{% content-ref url="disciplinary/" %}
[disciplinary](disciplinary/)
{% endcontent-ref %}

### ERLC

{% content-ref url="erlc/" %}
[erlc](erlc/)
{% endcontent-ref %}

### Sessions

{% content-ref url="sessions/" %}
[sessions](sessions/)
{% endcontent-ref %}
