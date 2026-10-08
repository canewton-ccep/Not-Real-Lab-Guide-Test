# Task 7 – Clean Up

<span class="task-badge">Task 7 of 7</span> &nbsp; **Estimated time:** 5 minutes

The lab user is now consuming a Messaging license. This task shows you the two ways to
give it back — which is also exactly what you do in production when somebody changes
role or leaves the company.

!!! warning "Decide before you act"
    Skip this task entirely if you are keeping the user for a later lab. Nothing
    breaks. Just be aware the license stays consumed.

## Choose your approach

| Approach | What happens to the account | What happens to their messages | Use it when |
| --- | --- | --- | --- |
| **A. Remove the license** | Account stays, can still sign in but cannot message | Retained | The person is staying but changing role |
| **B. Delete the user** | Account removed from the organization | Removed from the organization's control | The person has left, or this was a lab account |

For a lab account you created only to practise, **B** is the tidy choice.

## Approach A — Remove the Messaging license

### Step 1

In Control Hub, go to **Management > Users** and click the lab user.

### Step 2

Open the **Services** (or **Licenses**) section.

### Step 3

Clear the **Messaging** checkbox or toggle it off.

### Step 4

Save your change.

### Step 5

Switch to **Window A**, where the new user is signed in. Within a few minutes the app
loses access to messaging features. Signing out and back in makes the change immediate.

!!! note "The license returns to the pool"
    Check **Management > Subscriptions**. The assigned count for Messaging has dropped
    by one and the license is available to assign to somebody else.

## Approach B — Delete the user

!!! warning "This is not reversible"
    Deleting a user removes their account from your organization. Their messages and
    the files they shared are no longer accessible to them through this organization,
    and the account cannot be restored by recreating it with the same email — that
    creates a new, empty account.

    In production, confirm your organization's data-retention and legal-hold
    obligations before deleting anyone. Many organizations deactivate rather than
    delete for this reason.

### Step 1

In Control Hub, go to **Management > Users**.

### Step 2

Click the lab user to open their profile.

### Step 3

Find the delete option — typically **Delete User** at the bottom of the profile, or
under an **Action** / **…** menu on the user's row.

### Step 4

Confirm the deletion. Control Hub asks you to confirm because the action is permanent.

### Step 5

Verify the user no longer appears in the user list, and that
**Management > Subscriptions** shows the Messaging license returned to the available
pool.

## Optional — Clean up the space

The space you created in Task 6 still exists for the remaining members.

In **Window B** (the admin), open **Lab 1 - Onboarding Test**, open the space menu, and
choose **Leave space**.

!!! note "Spaces outlive their members"
    A Webex space persists as long as at least one person is in it. Leaving a space
    removes it from your list but does not delete the conversation for anyone else.
    This surprises customers; it is worth calling out.

## :material-check-circle: Verify your work

- [ ] You chose and completed either Approach A or Approach B (or deliberately skipped both).
- [ ] **Management > Subscriptions** reflects the license change.
- [ ] You understand the difference between removing a license and deleting a user.

---

## :material-trophy: Lab complete

You can now:

- Add a user to a Webex organization manually in Control Hub
- Assign and verify a Webex Messaging license
- Explain the Pending-to-Active lifecycle and when a license is consumed
- Activate a new account and sign in to the Webex App
- Exchange direct messages, use Messaging features, and create a space
- Reclaim a license or remove a user

### Where to go next

- **Add Meetings.** Repeat Task 3 for the same user with the Meetings service, then
  schedule and join a meeting.
- **Add Calling.** Assign a Webex Calling license, which introduces locations, phone
  numbers, and extensions.
- **Scale it up.** Instead of the manual wizard, use the bulk CSV template in
  **Management > Users** to add and license dozens of users at once.
- **Automate it.** The same operation is available over the
  [Webex People API](https://developer.webex.com/docs/api/v1/people), which is how
  real provisioning integrations do it.

---

[:material-arrow-left: Back: Task 6](06-exchange-messages.md){ .md-button }
[Troubleshooting :material-lifebuoy:](troubleshooting.md){ .md-button }
