# Morningwood Gaming (.github)

This repository (**MW-GC/.github**) contains GitHub-wide defaults for the Morningwood Gaming organization, including community health files (Code of Conduct, contributing guidelines, security policy, etc.) that apply across repositories in this org.

## What this repository is for

GitHub supports “community health” files stored in an organization’s `.github` repository. When placed here, these files can automatically provide default guidance across repos (unless a repo overrides them with its own versions).

Use this repo to manage:

- **Code of Conduct** and expected behavior standards
- **Contributing** instructions and PR expectations
- **Security** policy and vulnerability reporting guidance
- **Support** and contact/help directions
- Issue / PR templates and organization-wide GitHub configuration
- **Workflow templates** — reusable GitHub Actions workflows for all repositories
- **Active workflows** — organization-wide workflows that run automatically

## Community health files

These documents are intended to be maintained **in this repo** and used as org-wide defaults:

- `CODE_OF_CONDUCT.md` — community rules and expectations
- `CONTRIBUTING.md` — how to contribute, branch/PR conventions, etc.
- `SECURITY.md` — how to report vulnerabilities responsibly
- `SUPPORT.md` — how to get help / where to ask questions

Depending on how you structure things, you may also include:

- `.github/ISSUE_TEMPLATE/*` — issue templates
- `.github/pull_request_template.md` — PR template
- `.github/FUNDING.yml` — funding links (optional)

## Active workflows

The `.github/workflows/` directory contains workflows that run automatically for this organization:

- **Pull Request Labeler** — Automatically labels PRs in this repo based on file paths
- **PR Size Labeler** — Labels PRs in this repo by size (XS, S, M, L, XL)
- **First Time Contributor Greeting** — Welcomes new contributors to this repo

Configuration: Labeler uses `.github/labeler-config.yml` for label rules.

## Workflow templates

The `workflow-templates/` directory contains reusable GitHub Actions workflow templates that can be used across all repositories in the organization. These templates provide standardized automation for common tasks:

### Available Templates

1. **Pull Request Labeler** — Automatically labels PRs based on file paths (docs, dependencies, JS/TS, .NET, etc.)
2. **PR Size Labeler** — Labels PRs by size (XS, S, M, L, XL) to help reviewers
3. **Stale Issue/PR Management** — Automatically manages and closes stale issues and PRs
4. **Dependency Review** — Scans PR dependencies for security vulnerabilities and license compliance
5. **CodeQL Security Scanning** — Performs automated security analysis (supports JS/TS and .NET)
6. **Auto Assign Reviewers** — Automatically assigns reviewers to PRs based on configuration
7. **First Time Contributor Greeting** — Welcomes new contributors with friendly messages

### Using Workflow Templates

To use these templates in your repository:

1. Go to your repository's **Actions** tab
2. Click **New workflow**
3. Scroll to **Workflows created by Morningwood Gaming**
4. Choose a template and click **Configure**
5. Customize as needed and commit

For detailed documentation, see [workflow-templates/README.md](workflow-templates/README.md).

## How to contribute to this repo

If you’re proposing changes to MWG’s org-wide policies or templates:

1. Open an issue describing what you want to change and why
2. Submit a PR with the proposed edits
3. Keep changes clear, minimal, and easy to review
4. If the change affects contributor expectations, call it out explicitly in the PR description

## Links

- Website: https://mw-gc.com
- Organization: https://github.com/MW-GC

---

If you’re helping improve MWG’s documentation, templates, or policies: thank you.
