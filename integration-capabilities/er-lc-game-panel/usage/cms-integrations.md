---
description: The ER:LC panel also has extended functionality from other areas of the CMS
---

# CMS Integrations

## Form Stage Actions

<details>

<summary>Form Stage Actions</summary>

[Form stages have configurable actions](../../../tutorials/forms/creating-custom-forms.md#form-stages) to send webhooks, messages, modify ranks, in-game commands, and more. When a form submission is moved to the stage, the stage actions are ran.

CMS form stage actions also support running ER:LC commands.

The ER:LC commands can be ran on the form submitter, the user who changed the form stage, or on a specific user selected in the submission with a **Member Select** type form field.

**Example: Priority Request**

In this example, when a user's **Priority Request** form submission is moved to **Accepted** we send that user an in-game private message.

<figure><img src="../../../.gitbook/assets/image (3) (1).png" alt=""><figcaption></figcaption></figure>

</details>

## Roster Activity Time

<details>

<summary>Roster Activity Time</summary>

The ER:LC panel extends functionality to [CMS rosters](../../../tutorials/rosters/creating-custom-rosters.md) by allowing you to add an `Activity Tracker Hours` column that automatically displays each user’s in-game time over a configurable period. This column can also be configured to track time spent on specific ER:LC team(s).

<div><figure><img src="../../../.gitbook/assets/image (25).png" alt="" width="375"><figcaption></figcaption></figure> <figure><img src="../../../.gitbook/assets/image (26).png" alt="" width="234"><figcaption></figcaption></figure></div>

</details>

## Routine Actions

<details>

<summary>Routine Actions</summary>

The [CMS Actions panel](../../../tutorials/administrative/actions.md) performs routine actions at custom intervals. This panel integrates with the ER:LC panel to offer automated in-game hints and notifications.

<figure><img src="../../../.gitbook/assets/image (24).png" alt="" width="375"><figcaption></figcaption></figure>

</details>

## Disciplinary Points

<details>

<summary>Disciplinary Points</summary>

[Disciplinary points](../../../tutorials/administrative/disciplinary-panel.md) can be assigned either through an [ER:LC player record](player-records.md) or manually in the CMS. Once a user exceeds a defined point threshold, the associated disciplinary actions are executed automatically.

The ER:LC panel extends this functionality by enabling automated kicks or bans when a user reaches the configured disciplinary point limit.

<figure><img src="../../../.gitbook/assets/image (7) (1).png" alt="" width="375"><figcaption></figcaption></figure>

</details>
