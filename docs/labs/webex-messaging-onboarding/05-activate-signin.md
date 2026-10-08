# Task 5 – Activate and Sign In to the Webex App

<span class="task-badge">Task 5 of 7</span> &nbsp; **Estimated time:** 10 minutes

Switch roles. For this task and the next, you are the **new user**, not the
administrator.

!!! warning "Use a separate browser profile or device"
    Your administrator session is already signed in to Webex in this browser. If you
    activate the new user in the same browser profile, the two sessions collide and
    you will spend ten minutes confused about who you are signed in as.

    Use one of these instead:

    - A **private / incognito window**
    - A **different browser** (admin in Chrome, user in Firefox)
    - A **second computer or a phone**

## Steps

### Step 1 — Get the activation email

Open the inbox for `<new-user-email>`.

Look for a message from Webex inviting the user to join the organization. Subject lines
vary by release, but it will reference Webex and contain a prominent activation button
such as **Activate**, **Join**, or **Get started**.

??? question "No email arrived?"
    Work through these in order:

    1. **Check junk/spam.** This is the cause the majority of the time.
    2. **Wait five minutes.** Delivery is usually immediate but not guaranteed.
    3. **Confirm welcome emails aren't suppressed** — you checked this in Task 4,
       Step 5. If they are suppressed, skip to Step 3 below; there is no email and
       none is coming.
    4. **Resend it.** As the administrator, open **Management > Users**, select the
       user, and use the option to resend the activation/invitation email.
    5. **Skip it entirely.** The email is a convenience, not a requirement. The user
       can always go straight to the Webex App and sign in with their address, which
       is Step 3.

    More detail in [Troubleshooting](troubleshooting.md#no-activation-email).

### Step 2 — Click the activation link

Click the activation button in the email.

A browser opens to a Webex page. Depending on how your organization authenticates,
you are asked to either:

=== "Webex-managed passwords"

    Create a password for the account. Choose one that meets the complexity rules shown
    on screen, confirm it, and submit.

    !!! warning "Passwords in a lab"
        Use a throwaway password generated for this lab. Do not reuse a password from
        any other system, and do not share it in chat, tickets, or lab worksheets.

=== "Single sign-on (SSO)"

    You are redirected to your identity provider. Authenticate there as you normally
    would. Webex does not hold a password for the account in this case.

### Step 3 — Open the Webex App

Choose one:

=== "Desktop app (recommended)"

    1. Download the installer from [webex.com/downloads](https://www.webex.com/downloads.html).
    2. Install and launch **Webex**.
    3. On the welcome screen, enter `<new-user-email>` and click **Next**.

=== "Web browser (nothing to install)"

    1. In your private window, go to [web.webex.com](https://web.webex.com).
    2. Enter `<new-user-email>` and click **Next**.

=== "Mobile"

    1. Install **Webex** from the App Store or Google Play.
    2. Launch it and enter `<new-user-email>`.

### Step 4 — Complete sign-in

Enter the password you created in Step 2, or complete your SSO and multi-factor
prompts.

!!! note "This is the moment the license is consumed"
    This first successful sign-in is what draws the Messaging license from your
    subscription. Until now, the license was reserved on paper only.

### Step 5 — Work through the first-run experience

On first launch, Webex shows a short set of introductory tips and may ask for
permissions (notifications, microphone, camera).

- Click through or dismiss the tips.
- Allowing notifications is helpful for Task 6, since it lets you see messages arrive.
- Microphone and camera are not needed for this lab; you may decline them.

### Step 6 — Confirm your identity in the app

Click your **profile picture or initials** in the top corner of the app.

The menu shows the display name and email address of the signed-in account. Confirm it
reads `<new-user-first> <new-user-last>` and `<new-user-email>` — not your admin
account.

### Step 7 — Confirm the status flipped in Control Hub

Switch back to your administrator session and go to **Management > Users**.

Find the new user. Their status now reads **Active** instead of **Pending**.

!!! tip
    If it still shows Pending, refresh the page. Control Hub does not update the table
    live.

## :material-check-circle: Verify your work

- [ ] The Webex App is open and signed in as `<new-user-email>`.
- [ ] The profile menu shows the new user's name and address, not the admin's.
- [ ] The **Messaging** area of the app is visible in the left navigation.
- [ ] In Control Hub, the user's status has changed from **Pending** to **Active**.

---

[:material-arrow-left: Back: Task 4](04-verify-user.md){ .md-button }
[Next: Task 6 – Exchange Messages :material-arrow-right:](06-exchange-messages.md){ .md-button .md-button--primary }
