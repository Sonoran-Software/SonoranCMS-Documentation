---
description: >-
  Stop wasting time manually reviewing applications. With Sonoran CMS, your
  community can set custom rules to automatically score forms and seamlessly
  move them through the right workflow stage.
---

# AI Form Processing

<figure><img src="../../.gitbook/assets/upgrade_ai_forms.png" alt=""><figcaption></figcaption></figure>

## AI Forms Processing

{% hint style="danger" %}
AI form processing is currently in **early-access with our partnered communities**.

Public availability will be released soon!
{% endhint %}

{% hint style="danger" %}
**AI form processing is only enabled with a Pro Subscription!**

Learn more about our [paid plans](../../pricing/pricing-faq/create-and-manage-a-subscription.md).
{% endhint %}

Stop wasting time manually reviewing applications. With Sonoran CMS, your community can set custom rules to automatically score forms and seamlessly move them through the right workflow stage.

### Understanding AI Processing Stages

When a form enters a specific stage (e.g., _Awaiting Review_), you can define how the AI should evaluate the submission’s responses. Based on the scoring criteria you set, the AI will automatically advance the form to the next stage—such as _Accepted_ or _Denied_.

### Setting Section Criteria

For each section of your form, you can define criteria for the AI to score responses. Criteria can be marked as **required** or **preferred**, and each section can be assigned a **scoring weight** to determine its importance. Every section visible to the user (see: [form dependencies](creating-custom-forms.md#conditional-sections)) will be scored.

To set this up:

1. Select **Add Section**.
2. Choose the section from the drop-down.
3. Assign a weight (how much this section should influence the overall score).
4. Add your custom criteria.

Some criteria can act as **deal-breakers**. For example, if applicants must be 18+ regardless of other answers, mark that criterion as **required**.

<figure><img src="../../.gitbook/assets/image (66).png" alt="" width="270"><figcaption></figcaption></figure>

### Setting Scoring Rules

In the **Scoring** section, the dropdown lets you specify a stage if any **required criteria** are missed. For example, if your application requires applicants to be 18+ but the user is underage, the form can automatically be moved to the **Denied** stage regardless of other responses.

Rules are applied according to their hierarchy and can be reordered using drag-and-drop.

Next, define the **scoring rules** that determine how forms progress:

1. Select **Add Rule**.
2. Enter the **minimum score**.
3. Enter the **maximum score**.
4. Choose the **form stage** to move to.

<figure><img src="../../.gitbook/assets/image (67).png" alt="" width="262"><figcaption></figcaption></figure>

#### **Disciplinary Points & Account Flags** Rules can also include limits on disciplinary points and account flags:

* [**Account Flags**](../administrative/security-center/#account-flags) are added when alternate accounts are detected.
* [**Disciplinary Points**](../administrative/disciplinary-panel.md) are assigned by staff when users have prior infractions.

For example, you may want to prevent a form from being automatically accepted if the applicant has a flagged account or too many disciplinary points.

<figure><img src="../../.gitbook/assets/image (68).png" alt="" width="255"><figcaption></figcaption></figure>

## Tips and Tricks

### Using "Likely" Accepted/Denied Stages

**AI form processing** is a powerful way to handle the majority of submissions. It can quickly filter out low-quality responses and highlight the best applications.

For critical applications—especially those that automatically add or remove ranks—it’s recommended to route them to **“Likely Accepted”** or **“Likely Denied”** stages. This ensures the AI speeds up the process while still allowing a **final human review** before a decision is made.

### Account Flags

[**Account Flags**](../administrative/security-center/account-flags.md) help protect your community against alternate accounts and ban evasion. If an applicant has active flags on their account, it’s recommended to route their submission to a **Manual Review** stage for further investigation before approval.
