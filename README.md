# Cloud Solutions Lab Guides

An [MkDocs](https://www.mkdocs.org/) site, using the
[Material for MkDocs](https://squidfunk.github.io/mkdocs-material/) theme, that hosts
hands-on labs teaching customers and users how to configure and use cloud
collaboration solutions.

**Live site:** https://canewton-ccep.github.io/Not-Real-Lab-Guide-Test/

## Contents

| Path | What's in it |
| --- | --- |
| `mkdocs.yml` | Site configuration: theme, navigation, Markdown extensions |
| `docs/` | All content (Markdown) |
| `docs/labs/` | One folder per lab |
| `docs/authoring/` | How to write a new lab, template, style guide |
| `docs/assets/images/` | Screenshots, one subfolder per lab |
| `docs/stylesheets/extra.css` | Custom styling |
| `.github/workflows/deploy.yml` | Builds and publishes to GitHub Pages on push to `main` |
| `.github/workflows/pr-check.yml` | Builds the site on every pull request |

## Run it locally

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
mkdocs serve
```

Open <http://127.0.0.1:8000>. The site rebuilds as you save.

On Windows, activate with `.venv\Scripts\activate` instead.

## Build

```bash
mkdocs build --strict
```

`--strict` turns warnings — including broken internal links — into errors. This is
what CI runs, so run it before you open a pull request. Output lands in `site/`, which
is gitignored.

## Publishing

This repository is already wired up: pushing to `main` runs the
`Build and deploy lab guide` workflow, which builds the site and publishes it to
GitHub Pages. Watch it under the **Actions** tab.

**Settings > Pages > Source** must be set to **GitHub Actions** — the workflow uses the
Pages deployment API rather than a `gh-pages` branch.

### Forking this for another site

If you reuse this scaffold elsewhere, update these three keys in `mkdocs.yml` to match
the new repository. `site_url` must end with a trailing slash:

```yaml
site_url: https://my-org.github.io/lab-guides/
repo_url: https://github.com/my-org/lab-guides
repo_name: my-org/lab-guides
```

### Private repositories

GitHub Pages on a private repository requires GitHub Enterprise Cloud. On a free or Pro
plan, either make the repository public or host the built `site/` directory somewhere
else — it is plain static HTML and will run from any web server, an S3 bucket, or an
internal intranet host.

## Deploying somewhere other than GitHub Pages

`mkdocs build` produces a self-contained static site in `site/`. Copy that directory
to any static host. If the site will not be served from the domain root, set `site_url`
accordingly so internal links and assets resolve.

## Adding a lab

See [Writing a New Lab](docs/authoring/writing-a-lab.md). Short version: create a
folder under `docs/labs/`, copy the template, add the pages to `nav:` in `mkdocs.yml`,
add a row to `docs/labs/index.md`, and open a pull request.

## Conventions

Content conventions — voice, callout usage, screenshot handling, verification
checklists — are in [the style guide](docs/authoring/style-guide.md). Please read it
before contributing content.
