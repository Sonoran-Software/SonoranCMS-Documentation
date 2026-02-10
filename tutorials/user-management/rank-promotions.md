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

#### Promotion Flows

\
Create <mark style="color:orange;">**Promotion flows**</mark>  of ranks to promote or demote, Add disciplinary action or even assign new ranks when new actions are needed. \
\
When you select Promotion Flows\
Click the <mark style="color:$success;">**Green Plus Button**</mark> next to the <mark style="color:$info;">search bar</mark>. \
<br>

<figure><img src="../../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

**Actions**

Actions allow you to define what category a specific promotion flow will apply to.\
\
Click <mark style="color:orange;">**Actions**</mark> \
Click the <mark style="color:$success;">**Green Plus**</mark> <mark style="color:$success;">**Button**</mark>

When a promotion occurs, the configured action determines how the system responds based on the segment selected within that promotion flow. This ensures the promotion is processed and applied in accordance with the defined category and targeting rules set during configuration.

<figure><img src="../../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

**Promotion Flows**

Promotion Flows allow you to assign promotions quickly without needing to manually edit ranks each time.

To run a promotion, navigate to **Ranks → Promotions → Run Promotions**, then select the custom promotion ranks you’d like to apply. This streamlines the promotion process and ensures rank changes are applied consistently.

<figure><img src="../../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>

### Permissions

To allow others to manage Promotion Flows on your behalf, you can assign the following permissions.&#x20;



* Create/Edit/Remove Promotion Flows - **Modify Departments**
* Trigger Promotion Flows - **Change Permissions**
* Allows the user to modify anyone’s permissions except the owner’s - **Change Higher Permission**

