# Task 2 – Add the User

<span class="task-badge">Task 2 of 7</span> &nbsp; **Estimated time:** 5 minutes

Now you create the account. Control Hub walks you through a short wizard: identify the
user, assign services, review, and submit.

!!! note "Can I add users manually?"
    Manual user creation is available when your organization is **not** synchronizing
    identities from an external directory. If your users come from Active Directory via
    Directory Connector, or from a cloud identity provider, Control Hub blocks manual
    creation and you add the user at the source instead. See
    [Troubleshooting](troubleshooting.md#add-user-is-greyed-out).

## Steps

### Step 1 — Open the user list

In Control Hub, go to **Management > Users**.

You see a table of everyone currently in the organization, with columns for name,
email/ID, status, and administrator role.

### Step 2 — Start the Add user wizard

Click **Add user**.

!!! note
    Some releases present this as **Manage users**, which then offers **Manually add
    users** alongside CSV import and directory synchronization. If you see that
    intermediate screen, choose **Manually add users**.

### Step 3 — Choose how to identify the user

The wizard asks how you want to enter people. Choose:

**Names and Email address**

!!! tip "Why not email-only?"
    **Email address** is the fastest option and lets you paste a comma-separated list
    — useful when you are onboarding a batch. For this lab, supplying the name gives
    you a friendlier display name to search for in Task 6, so take the slightly longer
    path.

### Step 4 — Enter the new user's details

Fill in the three fields with the values you wrote down in Task 1:

| Field | Value |
| --- | --- |
| First name | `<new-user-first>` |
| Last name | `<new-user-last>` |
| Email address | `<new-user-email>` |

Then click the **+** (add) control to commit the entry to the list below the form.

!!! warning "The row must appear in the list"
    If you type the details and click **Next** without clicking **+**, some releases
    silently drop the entry and you end up adding nobody. Confirm the person now
    appears as a row before you continue.

### Step 5 — Continue to licensing

Click **Next**.

!!! note "Batch limits"
    You can add up to **25 users at a time** this way. If your organization has marked
    any user attribute as required, the limit drops to **1 user at a time**. One user is
    all this lab needs either way.

## What just happened

Nothing yet — the wizard has only collected your input. The account is not created, and
no license is touched, until you finish the review step in Task 3. You can still cancel
safely at this point.

## :material-check-circle: Verify your work

- [ ] You are in the **Add user** wizard.
- [ ] `<new-user-email>` appears as a row in the list of users to add.
- [ ] The first and last name shown match what you intended.
- [ ] You clicked **Next** and are now on a screen about services or licenses.

---

[:material-arrow-left: Back: Task 1](01-prerequisites.md){ .md-button }
[Next: Task 3 – Assign the Messaging License :material-arrow-right:](03-assign-license.md){ .md-button .md-button--primary }
