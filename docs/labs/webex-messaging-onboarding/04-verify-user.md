# Task 4 – Verify the User in Control Hub

<span class="task-badge">Task 4 of 7</span> &nbsp; **Estimated time:** 5 minutes

Before you hand the account to the user, confirm from the administrator side that it
looks the way you intended. Catching a wrong license here is far cheaper than
debugging it after the user reports "Webex doesn't work."

## Steps

### Step 1 — Find the user

Go to **Management > Users**.

In the search box above the table, type part of `<new-user-email>` or
`<new-user-first>`. The table filters as you type.

!!! tip
    If the user does not appear, clear any active filters on the table (status,
    license, administrator role) — a filter left over from earlier browsing is the
    usual cause.

### Step 2 — Read the status

Look at the **Status** column for your new user. It reads **Pending**.

!!! note "What Pending means"
    **Pending** means the account exists in your organization but the person has never
    signed in. It is the expected state for a brand-new user. It becomes **Active**
    after the first successful sign-in, which you will do in Task 5.

    A Pending user is not a failure, and it is not consuming a license yet.

### Step 3 — Open the user's profile

Click the user's row.

A detail panel or page opens, showing tabs or sections such as **Profile**,
**Services** (or **Licenses**), **Devices**, and **Meetings**.

### Step 4 — Confirm the assigned services

Open the **Services** section.

Confirm:

| Service | Expected state |
| --- | --- |
| **Messaging** | Enabled / toggled on |
| **Meetings** | Off |
| **Calling** | Off |

!!! tip "Fixing it here"
    This panel is also where you change a license after the fact. If Messaging is off,
    turn it on and save — you do not need to delete and recreate the user. Likewise, if
    an extra service was assigned by an automatic template, clear it here.

### Step 5 — Note the activation email behaviour

Whether the new user received a welcome/activation email depends on an
organization-wide setting.

To check it, go to **Management > Organization Settings** and find the
**Email** section, which controls whether automated welcome emails are suppressed.

| Setting | What the user experiences |
| --- | --- |
| Welcome emails **enabled** (default) | The user receives an activation email at `<new-user-email>`. |
| Welcome emails **suppressed** | No email is sent. The user must be told to go to the Webex App and sign in with their address. |

Make a note of which case applies — Task 5 branches on it.

!!! note "Why would anyone suppress the email?"
    Large organizations often stage thousands of accounts weeks before go-live and do
    not want users activating early or filing help-desk tickets about an unexpected
    email. They send their own communication instead, on their own schedule.

## :material-check-circle: Verify your work

- [ ] `<new-user-email>` is listed under **Management > Users**.
- [ ] Their status is **Pending**.
- [ ] Their **Services** show Messaging enabled.
- [ ] No other service (Meetings, Calling) is enabled.
- [ ] You know whether your organization sends welcome emails.

---

[:material-arrow-left: Back: Task 3](03-assign-license.md){ .md-button }
[Next: Task 5 – Activate & Sign In :material-arrow-right:](05-activate-signin.md){ .md-button .md-button--primary }
