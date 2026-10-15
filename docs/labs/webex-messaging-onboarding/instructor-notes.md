# Instructor Notes

Notes for whoever delivers this lab. Not intended for the learner-facing handout,
though nothing here is confidential.

## Timing

| Segment | Planned | Notes |
| --- | --- | --- |
| Intro and prerequisites | 10 min | Prerequisite failures are the main schedule risk — see below. |
| Tasks 2–4 (admin side) | 15 min | Fast and reliable. |
| Task 5 (activation) | 15 min | Email delivery is the usual bottleneck. |
| Task 6 (messaging) | 10 min | Learners enjoy this; let it run long if the room is engaged. |
| Task 7 and wrap-up | 10 min | |
| **Total** | **60 min** | Advertise 45 min of content in a 60-minute slot. |

## Prepare in advance

1. **Send prerequisites out at least 48 hours ahead.** Specifically: admin access, an
   available Messaging license, and a usable second email address. Learners who show up
   without these cannot do the lab.
2. **Decide on the organization.** Options, in order of preference:
     - One [developer sandbox](https://developer.webex.com/docs/developer-sandbox-guide) per learner — cleanest.
     - A shared training tenant where each learner uses a distinct `+N` address.
     - The learner's own production tenant — acceptable, but emphasise Task 7.
3. **Verify the plus-address trick works** on whatever mail system your audience uses.
   It works on Gmail and Microsoft 365; some corporate gateways strip or reject it.
4. **Test the whole lab yourself the week before.** Control Hub navigation labels shift
   between releases, and a stale screenshot undermines learner confidence faster than
   no screenshot.

## Known friction points

| Point | What happens | Mitigation |
| --- | --- | --- |
| Same-browser sessions | Learner activates the new user in the browser where they're already signed in as admin and gets confused about identity | Say it out loud at the start of Task 5. Have them open a private window *before* they need it. |
| Activation email in spam | Five minutes lost per learner | Tell everyone to open their junk folder preemptively while the email sends. |
| Invitation email doesn't arrive | Learner is stuck at Task 5 Step 1 | Tell them to sign in at web.webex.com with the address anyway — Webex emails a confirmation code instead. |
| "Last email status: None" in Control Hub | Learner thinks no invitation was sent | The field can lag behind delivery; have them check the inbox. |
| Basic entitlements look like extra licences | Learner tries to untick Basic space meetings / Call on Webex | They are free and locked on once a paid licence is ticked. Explain the Basic vs. paid split from Task 3. |
| Control Hub label drift | Steps say **Management > Users**, the console says something slightly different | The lab already notes this. Reinforce it verbally. |
| Admin account unlicensed for Messaging | Task 6 cannot be completed | Verify your own demo account before the session. |

## Discussion prompts

Use these to turn the clicking into understanding.

- *Why are Basic messaging, Basic space meetings and Call on Webex always assigned?*
  (They are free entitlements; the paid licence layers on top of them.)
- *When would you not want Webex to email new users directly?* (Phased rollouts,
  staged migrations, a communication plan owned by somebody other than IT.)
- *Why would you remove a license instead of deleting a user?* (Retention, legal hold,
  role change, re-hire.)
- *At what organization size does this manual flow stop being viable?* (Leads naturally
  into bulk CSV, directory synchronization, and the People API.)

## Extending the lab

- **Bulk.** Have learners add five users at once via the CSV template and compare the
  effort.
- **Meetings.** Assign a Meetings license and schedule a meeting between the two
  accounts.
- **API.** Perform the same create-and-license operation with the
  [Webex People API](https://developer.webex.com/docs/api/v1/people), which makes the
  provisioning automation story concrete.

## Maintaining this lab

- Re-verify every Control Hub navigation path each quarter.
- Screenshots belong in `docs/assets/images/webex-messaging-onboarding/`. Crop to the
  relevant region, and redact real names, email addresses, and organization names.
- The build runs with `mkdocs build --strict`, so a broken internal link fails CI
  rather than shipping.
