# Agent365-Overview

Atlanta, USA

[![GitHub](https://img.shields.io/badge/--181717?logo=github&logoColor=ffffff)](https://github.com/)
[Cloud2BR OSS - Learning Hub](https://github.com/Cloud2BR-MSFTLearningHub)

Last updated: 2026-08-04

----------

Detailed Microsoft Agent 365 setup and operations documentation hub. This repo
provides practical guidance for platform, IT, security, and compliance teams to
observe, govern, secure, and operationalize agents at enterprise scale.

## Documentation Hub

GitHub Pages site:

- https://cloud2br-msftlearninghub.github.io/Agent365-Overview/

Documentation tracks:

- Foundation: architecture, control plane, identity, and data boundaries.
- Observe: registry, map, telemetry, health, and KPI frameworks.
- Govern: lifecycle, approvals, policy, tools, and MCP governance.
- Secure: security posture, runtime defense, and Purview data controls.
- Operations: deployment checklist, operating model, and incident response.
- Extend: SDK and integration paths for custom and third-party agents.

## Workflow Summary

| Workflow | Trigger | What it does |
| --- | --- | --- |
| `.github/workflows/validate_and_fix_markdown.yml` | Pull requests to `main` | Runs `markdownlint`, auto-fixes Markdown style issues when possible, validates the required header block for every tracked Markdown file, and pushes any fixes back to the PR branch. |
| `.github/workflows/update-md-date.yml` | Pull requests to `main` | Looks at the full PR diff, updates the `Last updated:` line inside the standard Markdown header block for changed Markdown files, and pushes the result back to the PR branch. |
| `.github/workflows/validate_and_fix_notebook.yml` | Pull requests to `main` | Validates Jupyter notebooks, normalizes widget metadata when needed, and commits notebook-format fixes back to the PR branch. |
| `.github/workflows/use-visitor-counter.yml` | Pull requests to `main` and manual runs | Runs the vendored visitor-counter script stored in this repo to refresh Markdown counter badges and `metrics.json`, then commits the updated repository traffic data. |
| `.github/workflows/deploy-github-pages.yml` | Push and pull requests to `main`, and manual runs | Builds the MkDocs Material documentation site with `mkdocs build --strict` and, on `main`, deploys it to GitHub Pages. |

## Repository Structure

| Path | Purpose |
| --- | --- |
| `mkdocs.yml` | Site metadata, theme settings, and page navigation. |
| `requirements.txt` | Build dependencies for MkDocs Material. |
| `docs/index.md` | Landing page for the Agent365 setup and overview hub. |
| `docs/overview.md` | Agent365 capability and architecture overview. |
| `docs/foundation/` | Control-plane architecture, identity, and compliance foundations. |
| `docs/observe/` | Inventory, observability, and value-tracking guidance. |
| `docs/govern/` | Lifecycle, approvals, policy, and tooling governance guidance. |
| `docs/secure/` | Defender and Purview-aligned security and data controls. |
| `docs/operations/` | Deployment and day-two operations runbooks. |
| `docs/extend/` | SDK and integration patterns for enterprise agent onboarding. |
| `docs/assets/css/custom.css` | Shared organization visual style for documentation pages. |
| `docs/assets/js/logo-link.js` | Makes the top-left logo route to the site root. |
| `docs/assets/js/external-links.js` | Opens external links in a new tab with `noopener noreferrer`. |

## Build And Preview Locally

```powershell
python -m pip install --disable-pip-version-check -r requirements.txt
mkdocs serve
```

Strict validation build:

```powershell
mkdocs build --strict
```

## Authoring Standards

- Keep the required Markdown header block in tracked Markdown files.
- Prefer official Microsoft documentation links for technical references.
- Use practical rollout guidance: owners, approvals, controls, validation, rollback.
- Keep production recommendations explicit and auditable.

## Required Markdown Header

> Within this org, every tracked Markdown file must include the following block immediately below the main `# Title` line. The location line can vary, but it must exist. The GitHub badge line, the `Cloud2BR OSS - Learning Hub` org link line, the date format, and the separator are org-wide standard and must match this structure exactly. The `Validate and Fix Markdown` workflow checks every tracked `.md` file against this header pattern on pull requests.

```md
# Document Title

City, Country

[![GitHub](https://img.shields.io/badge/--181717?logo=github&logoColor=ffffff)](https://github.com/)
[Cloud2BR OSS - Learning Hub](https://github.com/Cloud2BR-MSFTLearningHub)

Last updated: YYYY-MM-DD

----------
```

<!-- START BADGE -->
<div align="center">
  <img src="https://img.shields.io/badge/Total%20views-43-limegreen" alt="Total views">
  <p>Refresh Date: 2026-08-04</p>
</div>
<!-- END BADGE -->
