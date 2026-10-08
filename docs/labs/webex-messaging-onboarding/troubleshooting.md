# Troubleshooting

Problems are listed roughly in the order you would hit them.

## "Add user" is greyed out {#add-user-is-greyed-out}

**Cause.** Either you don't hold the Full administrator role, or your organization
synchronizes users from an external directory.

**Fix.**

1. Confirm your role. In **Management > Users**, find your own account — your role is
   shown on your profile. A read-only administrator cannot create users.
2. Check for directory synchronization under **Management > Organization Settings** or
   the Directory Connector / identity section. If synchronization is active, create the
   user in Active Directory (or your cloud identity provider) and let it sync; Control
   Hub will not let you add people manually.
3. If you purchased through Webex Online (`my.webex.com`), users are managed in **Webex
   User Hub**, not Control Hub.

## "This email already exists" or the user can't be added {#email-already-exists}

**Cause.** The address already belongs to a Webex account somewhere — another
organization, or a free/trial account the person signed up for themselves.

**Fix.**

- **Use a different address.** Fastest option for a lab. A plus-address such as
  `you+lab2@example.com` gives you a fresh identity.
- **If it is a self-signed-up free account**, the owner of that account must delete
  that organization before the address can be claimed by yours.
- **If it belongs to another organization you control**, delete the user there first.

## No activation email arrived {#no-activation-email}

**Cause, most to least likely.** Spam filtering; welcome emails suppressed at the
organization level; a mail gateway rejecting the plus-address; genuine delay.

**Fix.**

1. Check the junk/spam folder.
2. Confirm your plus-address actually delivers — send yourself a plain test message to
   it.
3. Check **Management > Organization Settings > Email** to see whether automated
   welcome emails are suppressed.
4. Resend the invitation from the user's profile in Control Hub.
5. **Skip the email.** It is a convenience. Go to [web.webex.com](https://web.webex.com),
   enter the user's address, and sign in or use the password-reset flow to set a
   password. This works whether or not the email ever arrives.

## The new user's status stays "Pending" {#status-stays-pending}

**Cause.** Pending simply means nobody has signed in yet. It is not an error.

**Fix.** Complete [Task 5](05-activate-signin.md). After a successful first sign-in,
refresh the Control Hub user list — it does not update by itself.

## The user signs in but Messaging features are missing {#messaging-missing}

**Cause.** The Messaging service was not actually assigned, or the client is holding a
stale entitlement.

**Fix.**

1. In Control Hub, open the user's **Services** and confirm Messaging is on. Turn it on
   and save if not.
2. In the Webex App, sign out completely and sign back in. Entitlement changes are
   picked up at sign-in.
3. If it is still missing after ten minutes, restart the app.

## I'm signed in as the wrong person {#wrong-account}

**Cause.** The administrator session and the new-user session are sharing one browser
profile.

**Fix.** Sign out, then use a private/incognito window, a different browser, or a
second device for the new user — as called out at the top of
[Task 5](05-activate-signin.md).

## I can't find the other user when addressing a message {#cannot-find-the-other-user}

**Cause.** One of: they are in a different Webex organization; one of the two accounts
isn't licensed for Messaging; or you are typing a display name that doesn't match.

**Fix.**

1. Type the **full email address** rather than a name. Directory search on partial
   names can miss.
2. Confirm both accounts appear in the same organization's **Management > Users** list.
3. Confirm both accounts have Messaging enabled under **Services**.
4. Note that you *can* message people outside your organization in Webex, but only by
   their full email address — partial-name search will not find them.

## Messages send but never arrive {#messages-not-arriving}

**Cause.** Usually network filtering rather than Webex configuration.

**Fix.**

1. Check the connection indicator in the Webex App. A banner appears when it loses its
   connection.
2. Corporate proxies and firewalls can block the ports and domains Webex needs. Test
   from a different network — a phone hotspot is the quickest check.
3. Review the Webex network requirements with your network team if the hotspot works
   and the corporate network does not.

## An error appears when opening a user's Calling settings {#calling-settings-error}

**Cause.** A known hiccup when a Calling license was just assigned.

**Fix.** Remove the Webex Calling license from the user, save, then reassign it. This
lab does not assign Calling, so you should not hit it.

---

## Still stuck?

- [Webex Help Center](https://help.webex.com)
- [Webex Status](https://status.webex.com) — check for a live incident before debugging further
- Your organization's Webex administrator or Cisco partner
