# Writing a New Lab

## 1. Create the folder

Every lab is a folder under `docs/labs/`, named in kebab-case after the lab:

```text
docs/labs/<solution>-<outcome>/
├── index.md              # Lab overview: objectives, time, task table
├── 01-<first-task>.md
├── 02-<second-task>.md
├── ...
├── troubleshooting.md
└── instructor-notes.md
```

Screenshots go in `docs/assets/images/<lab-folder-name>/`.

## 2. Copy the template

Start each task page from the [Lab Template](lab-template.md). It already has the
badge, the step structure, the verification checklist, and the navigation buttons.

## 3. Add it to the navigation

Labs do not appear until you list them in the `nav:` block of `mkdocs.yml`:

```yaml
nav:
  - Labs:
      - Overview: labs/index.md
      - "Solution: Outcome":
          - Lab Overview: labs/my-new-lab/index.md
          - "Task 1 – First Thing": labs/my-new-lab/01-first-thing.md
```

Also add a row to the table in `docs/labs/index.md`.

## 4. Preview locally

```bash
python3 -m venv .venv && source .venv/bin/activate && pip install -r requirements.txt && mkdocs serve
```

Open <http://127.0.0.1:8000>. The site rebuilds as you save.

## 5. Check it builds strictly

```bash
mkdocs build --strict
```

This is what CI runs. It fails on broken internal links, so fix anything it reports
before opening a pull request.

## 6. Open a pull request

The PR check builds the site. Merging to `main` publishes it to GitHub Pages
automatically.

## Structural rules

| Rule | Why |
| --- | --- |
| One task per page | Learners track progress by page. A 2,000-word page feels endless. |
| Every task ends with a verification checklist | Learners need a way to know they succeeded before moving on. |
| Every task page links forward and back | Nobody should have to use the sidebar to advance. |
| State time estimates per task | Lets a learner decide whether to start before a meeting. |
| Put recovery steps in `troubleshooting.md`, not inline | Keeps the happy path short; link to the anchor from the step that can fail. |
| Keep instructor material in `instructor-notes.md` | Learners can read it, but it stays out of their way. |
