# Lab Template

Copy the blocks below when starting a new lab. See [Writing a New Lab](writing-a-lab.md)
for where the files go.

## Lab overview page (`index.md`)

````markdown
# Lab: <Outcome> in <Solution>

<span class="task-badge">Beginner</span> &nbsp; **Estimated time:** NN minutes

## What you'll build

One paragraph describing the end state in concrete terms.

## Learning objectives

After completing this lab, you will be able to:

1. ...
2. ...

## Tasks

| # | Task | Time |
| --- | --- | --- |
| 1 | [First task](01-first-task.md) | 5 min |

---

!!! warning "Licenses are real"
    Note any cost or production impact here.
````

## Task page

````markdown
# Task N – <Short Title>

<span class="task-badge">Task N of M</span> &nbsp; **Estimated time:** NN minutes

One or two sentences on what this task accomplishes and why it matters.

## Steps

### Step 1 — <Short description>

The action, in the imperative. Say what the learner should see afterwards.

!!! note "Optional context"
    Background a curious learner would want.

### Step 2 — <Short description>

=== "Option A"

    Steps for the first variation.

=== "Option B"

    Steps for the second variation.

!!! warning
    Something that costs time or money if ignored.

## :material-check-circle: Verify your work

- [ ] Something observable is true.
- [ ] Something else observable is true.

---

[:material-arrow-left: Back: Task N-1](0X-previous.md){ .md-button }
[Next: Task N+1 – Title :material-arrow-right:](0Z-next.md){ .md-button .md-button--primary }
````

## Troubleshooting page

````markdown
# Troubleshooting

## <Symptom as the learner would describe it> {#stable-anchor}

**Cause.** One sentence.

**Fix.**

1. First thing to try.
2. Second thing to try.

---

## Still stuck?

- Product help centre link
- Status page link
````

Link to a specific symptom from the step that can fail:

```markdown
See [Troubleshooting](troubleshooting.md#stable-anchor).
```

## Instructor notes page

````markdown
# Instructor Notes

## Timing

| Segment | Planned | Notes |
| --- | --- | --- |

## Prepare in advance

1. ...

## Known friction points

| Point | What happens | Mitigation |
| --- | --- | --- |

## Discussion prompts

- ...

## Extending the lab

- ...
````
