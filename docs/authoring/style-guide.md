# Style Guide

## Voice

Write to one learner, as "you". Use the imperative for actions: "Click **Add user**,"
not "The administrator should click Add user."

Keep sentences short. A step should be one action.

## Formatting conventions

| Element | Convention | Example |
| --- | --- | --- |
| UI element you click | **Bold** | Click **Add user**. |
| Text the learner types | Fenced `text` block | |
| Values shown on screen | `Inline code` | The status reads `Pending`. |
| Placeholders | `<angle-brackets>` | Enter `<new-user-email>`. |
| Keyboard keys | `++enter++` | Press ++enter++. |
| Navigation path | Bold with `>` | Go to **Management > Users**. |

## Callouts

Use them deliberately. A page where everything is a callout has no emphasis at all.

```markdown
!!! note
    Background a curious learner would want. Safe to skip.

!!! tip
    A shortcut or a better way. Safe to skip.

!!! warning
    Something that costs time, money, or data if ignored. Not safe to skip.

!!! success
    Confirmation that a milestone is reached.

??? question "Collapsed by default"
    Recovery detail that only some learners need. Keeps the page short.
```

Rough budget: at most one **warning** per task, and no more than three callouts of any
kind per page.

## Steps

- Number them. Use `### Step 1 — Short description` as the heading.
- One action per step. If a step contains "and then", split it.
- Say what the learner should see after the action, not just what to click.
- Where the UI varies, use content tabs (`=== "Option A"`) rather than parenthetical
  asides.

## Verification checklists

End every task with:

```markdown
## :material-check-circle: Verify your work

- [ ] Something observable is true.
- [ ] Something else observable is true.
```

Write checks the learner can actually see on screen. "The license is assigned" is not
checkable; "The **Services** panel shows Messaging enabled" is.

## Screenshots

- Crop to the region that matters. A full-screen capture buries the one button.
- Redact real names, email addresses, phone numbers, and organization names.
- Add alt text: `![Control Hub user list showing Pending status](../../assets/images/lab/users-pending.png)`
- Prefer describing UI in text where you can. Text survives a product redesign;
  screenshots do not.

## Things to avoid

- "Simply", "just", "obviously", "easy" — if it were easy they wouldn't need the lab.
- Unexplained product jargon on first use.
- Deep links into product UI that break between releases. Link to the console root and
  give the navigation path.
- Claiming a UI label is exact when it drifts between releases. Note the variation
  instead.
