---
description: >-
  Easily view user permissions and determine what ranks are granting or denying
  permissions.
---

# Configuring User Permissions

## Rank Permissions

When configuring a rank, each permission can be set to **Grant**, **Unset**, or **Deny**:

* **Grant** — Explicitly gives the permission to anyone with that rank.
* **Unset** — Neither grants nor denies the permission; it simply leaves it unchanged.
* **Deny** — Blocks the permission, even if another rank would otherwise grant it. A denied permission always overrides a grant.

Use **Deny** sparingly. It’s best suited for special ranks that must override other granted permissions, such as a temporary ban rank. In most cases, leaving a permission **Unset** is sufficient, as it will not grant the permission on its own.

<figure><img src="../../.gitbook/assets/image (2).png" alt="" width="279"><figcaption></figcaption></figure>

## Viewing User Permissions

You can view a user’s computed permissions directly in the account portal. Click the **(?)** icon above their ranks to see every permission that’s granted, unset, or denied. Hover over any permission to see a tooltip listing the groups and ranks responsible for granting or denying it.

<div><figure><img src="../../.gitbook/assets/image (1) (1).png" alt=""><figcaption></figcaption></figure> <figure><img src="../../.gitbook/assets/image (1) (1) (1).png" alt=""><figcaption></figcaption></figure></div>
