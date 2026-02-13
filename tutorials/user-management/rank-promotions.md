---
description: Configure rank promotion flows for your community members.
---

# Rank Promotions

{% embed url="https://app.guidde.com/share/playbooks/wJ25VP5VoPdCjmsS44zKHr?origin=G25dDmjNZ2b8ccFUz9X7G7W8T1k1" %}

## What are Promotions?

**Promotion flows** let you easily promote or demote members within your community.

For example, a user with the **Rookie** rank can be promoted to **Member**, or an **Administrator** can be demoted to **Moderator**.

<figure><img src="../../.gitbook/assets/Screenshot (477).png" alt=""><figcaption></figcaption></figure>

## Creating Promotion Flows

<details>

<summary>Flow Information and Ranks</summary>

1. Access the Promotions Panel

In the **Promotions** panel, select **Promotion Flows** to view, add, edit, or remove existing promotion flows.

2. Configure Promotion Ranks

Use the **Promote From** and **Promote To** fields to label the flow.\
Exampl&#x65;**:** Promote from **Moderator** to **Admin**.

**Configure Rank Changes**

* In the **Ranks to Add** section, select **Admin**.
* In the **Ranks to Remove** section, select **Moderator**.

3. **Run the Promotion Flow**

When executed, this flow will **add the Admin rank** and **remove the Moderator rank**, effectively promoting the user.

<figure><img src="../../.gitbook/assets/image (77).png" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary>Flow Actions</summary>

When a promotion flow is ran, you can also run automated actions like a Discord webhook, push notification, and more.

<figure><img src="../../.gitbook/assets/Screenshot 2026-02-13 at 11.08.50 AM.png" alt="" width="375"><figcaption></figcaption></figure>

</details>

### Multi-Flow Actions

<details>

<summary>Multi-Flow Actions</summary>

Communities can also define general actions that trigger when any one or more promotional flows are executed. This allows, for example, a single community announcement that summarizes all users included and all promotions applied.

<figure><img src="../../.gitbook/assets/Screenshot 2026-02-13 at 11.11.01 AM.png" alt="" width="375"><figcaption></figcaption></figure>

</details>

## Running Promotion Flows

<details>

<summary>Via CMS</summary>

In the **Run Promotions** panel, select the **user(s)**, choose the **promotion flow**, and specify whether to **promote** or **demote**.

Use the **green “+” icon** to add additional rows, allowing you to run multiple promotional flows simultaneously.

<figure><img src="../../.gitbook/assets/image (78).png" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary>Via Discord Command</summary>

Communities can [run promotional flows right from a Discord command](https://docs.sonoransoftware.com/bot/tutorials/sonoran-cms-integration/promotion-flows)!

</details>

### Permissions

To allow others to manage Promotion Flows on your behalf, you can assign the following [permissions](creating-departments.md#assigning-rank-permissions).&#x20;

* Create/Edit/Remove Promotion Flows
  * **Modify Departments**
* Trigger Promotion Flows
  * **Change Permissions**
* Trigger promotion flows that include ranks above the triggering user’s permission level.
  * **Change Higher Permission**
