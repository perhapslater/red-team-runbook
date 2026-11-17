# Red Team Runbook

A practical reference for authorized security assessments, published by PerhapsLater.

[Read the publication](https://perhapslater.github.io/red-team-runbook/) · [GitHub repository](https://github.com/perhapslater/red-team-runbook)

- Protocol and tool playbooks, assessment workflow, and command index.
- Browser-local engagement variables, derived domain values, and an optional guided tour.
- Native documentation search, navigation, syntax highlighting, and code copying.

## Develop locally

Use Python 3.12. Create an environment with `python -m venv .venv`, then activate
it with `.venv\Scripts\Activate.ps1` in PowerShell or `source .venv/bin/activate`
on macOS/Linux.

```sh
python -m pip install --require-hashes -r requirements.lock
python scripts/content_audit.py
python -m mkdocs build --strict
python scripts/publication_audit.py
python -m mkdocs serve
```

The build uses system fonts and local assets. Search and content rendering come
from MkDocs Material. Generated output and browser-local engagement values are
not committed. Use examples only in authorized environments.

## Publish

Follow [the GitHub Pages setup guide](GITHUB_PAGES.md) for repository creation,
Actions, the shared account-level domain, DNS, HTTPS, and verification. Deployment
uses a Pages artifact with a scoped token; no force push or personal access token
is needed. Project repositories inherit the account domain and contain no CNAME.

## Attribution

Technical citations and evidence remain with their articles. See [NOTICE](NOTICE)
and [third-party notices](THIRD_PARTY_LICENSES/mkdocs-material.txt). No new
project-wide license grant is introduced by this migration.
