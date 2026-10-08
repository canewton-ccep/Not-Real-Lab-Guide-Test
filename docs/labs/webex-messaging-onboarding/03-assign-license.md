# Task 3 – Assign the Messaging License

<span class="task-badge">Task 3 of 7</span> &nbsp; **Estimated time:** 5 minutes

A Webex user with no license can exist, but cannot do anything. This task grants the
Messaging service, which is what makes the Webex App usable for chat, spaces, and file
sharing.

## Understand what you are granting

| Service | What it enables | In this lab |
| --- | --- | --- |
| **Messaging** | Direct messages, spaces, file sharing, presence, whiteboards | :material-check: Required |
| **Meetings** | Hosting scheduled and personal-room meetings | Not required |
| **Calling** | PSTN / cloud calling, phone number and extension | Not required |
| **Contact Center**, **Hybrid Services**, others | Specialized workloads | Not required |

!!! note "Messaging is often free of charge"
    In many Webex subscriptions, Messaging is included for all users rather than drawn
    from a counted pool. You still assign it explicitly — the service has to be on the
    account for the Webex App to work.

## Steps

### Step 1 — Read the licensing screen

You are now on the screen where the wizard shows which services the new user will
receive. What you see depends on one organization setting:

=== "Automatic license assignment is ON"

    Control Hub displays the template of services this user will get automatically,
    with no checkboxes to change. Continue to Step 2 to override it.

=== "Automatic license assignment is OFF"

    Control Hub displays a list of services with checkboxes, ready for you to pick.
    Skip to Step 3.

!!! note "What is automatic license assignment?"
    An organization-wide template that grants a standard set of services to every new
    user, so admins don't have to think about it per person. It is configured under
    **Management > Users > Licenses** (or **Account > Licenses**, depending on
    release). It is convenient in production and inconvenient in a lab, which is why
    you override it here.

### Step 2 — Override the automatic assignment

Click **Assign license manually**.

The screen switches to the per-service checkbox view described in the second tab above.

### Step 3 — Choose the subscription

If your organization has more than one subscription, a selector appears. Choose the
subscription you confirmed had free licenses in Task 1.

If you only have one subscription, no selector appears. Continue.

### Step 4 — Select Messaging

Select the checkbox for **Messaging**.

Leave **Meetings**, **Calling**, and every other service **unselected**.

!!! warning "Resist the urge to tick everything"
    Assigning Meetings or Calling here consumes additional licenses from your
    subscription and adds configuration screens (such as location and phone number)
    that this lab does not cover. Messaging only.

### Step 5 — Skip the conditional screens

Depending on what you selected and how your organization is configured, the wizard may
present extra screens. Handle them as follows:

| Screen | What to do |
| --- | --- |
| **Calling location / phone number** | Should not appear. If it does, go back and clear the Calling checkbox. |
| **Tracking codes** | Applies only to Meeting licenses. Should not appear. |
| **Content management** | If it appears, accept the default and click **Next**. |

Click **Next** until you reach the review screen.

### Step 6 — Review

The review screen lists each user you are about to add and the services each one will
receive.

Confirm:

- Exactly one user is listed.
- The email address is `<new-user-email>`, spelled correctly.
- The services column shows **Messaging** and nothing else.

!!! warning "Last chance to fix a typo"
    After submission, correcting a misspelled email address means deleting the user and
    starting over — the email address is the account's identity and cannot be edited
    freely.

### Step 7 — Submit

Click **Add Users**.

Control Hub processes the list and shows a summary of how many records succeeded and
how many failed.

### Step 8 — Finish

Review the summary. It should report **1 record processed** with no errors.

Click **Finish**.

!!! note "When is the license actually consumed?"
    Creating the user does not draw the license down. The license is taken from your
    subscription the **first time the user signs in to Webex** — which happens in
    Task 5.

## :material-check-circle: Verify your work

- [ ] The review screen showed exactly one user with the Messaging service.
- [ ] You clicked **Add Users** and the summary reported no errors.
- [ ] You clicked **Finish** and returned to the user list.
- [ ] `<new-user-email>` now appears in the **Management > Users** table.

If the summary reported an error instead, see
[Troubleshooting](troubleshooting.md#email-already-exists).

---

[:material-arrow-left: Back: Task 2](02-add-user.md){ .md-button }
[Next: Task 4 – Verify in Control Hub :material-arrow-right:](04-verify-user.md){ .md-button .md-button--primary }
