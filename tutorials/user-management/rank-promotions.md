---
description: Configure rank promotion flows for your community members.
---

# Rank Promotions

## What are Promotions?

**Promotion flows** let you easily promote or demote members within your community.

For example, a user with the **Rookie** rank can be promoted to **Member**, or an **Administrator** can be demoted to **Moderator**.

## Creating Promotion Flows

### Label and Ranks

1. **Access the Promotions Panel**\
   In the **Promotions** panel, select **Promotion Flows** to view, add, edit, or remove existing promotion flows.
2. **Set Up the Flow Header**\
   Use the **Promote From** and **Promote To** fields to label the flow.\
   **Example:** Promote from **Moderator** to **Admin**.
3. **Configure Rank Changes**
   * In the **Ranks to Add** section, select **Admin**.
   * In the **Ranks to Remove** section, select **Moderator**.
4. **Run the Promotion Flow**\
   When executed, this flow will **add the Admin rank** and **remove the Moderator rank**, effectively promoting the user.

<figure><img src="../../.gitbook/assets/image (77).png" alt=""><figcaption></figcaption></figure>

### Actions

When a promotion flow is ran, you can also run automated actions like a Discord webhook, push notification, and more.

{% hint style="warning" %}
This feature is coming soon!
{% endhint %}

## Running Promotion Flows

### Via CMS

In the **Run Promotions** panel, select the **user(s)**, choose the **promotion flow**, and specify whether to **promote** or **demote**.

Use the **green “+” icon** to add additional rows, allowing you to run multiple promotional flows simultaneously.

<figure><img src="../../.gitbook/assets/image (78).png" alt=""><figcaption></figcaption></figure>

### Via Discord Command

Communities can [run promotional flows right from a Discord command](https://docs.sonoransoftware.com/bot/tutorials/sonoran-cms-integration/promotion-flows)!



### Permissions

To allow others to manage Promotion Flows on your behalf, you can assign the following permissions.&#x20;



* Create/Edit/Remove Promotion Flows - **Modify Departments**
* Trigger Promotion Flows - **Change Permissions**
* Allows the user to modify anyone’s permissions except the owner’s - **Change Higher Permission**

