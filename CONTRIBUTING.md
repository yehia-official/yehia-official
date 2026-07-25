# Contributing

Thanks for taking an interest in this repository. This repo powers a
personal GitHub profile page, so contributions here are a little
different from a typical open-source project — there's no application
to build or run — but improvements are still welcome, especially to
the automation workflows.

## Table of Contents

- [What lives in this repo](#what-lives-in-this-repo)
- [Ways to contribute](#ways-to-contribute)
- [Reporting an issue](#reporting-an-issue)
- [Suggesting an improvement](#suggesting-an-improvement)
- [Submitting a pull request](#submitting-a-pull-request)
- [Workflow conventions](#workflow-conventions)
- [Style guide](#style-guide)
- [Code of conduct](#code-of-conduct)

## What lives in this repo

| Path | Purpose |
|---|---|
| `README.md` | The profile page itself, rendered on the GitHub profile. |
| `.github/workflows/snake.yml` | Generates the animated contribution snake. |
| `.github/workflows/metrics.yml` | Generates the metrics dashboard SVG. |
| `.github/workflows/blog-post-workflow.yml` | Pulls the latest blog posts into the README. |
| `.github/FUNDING.yml` | Configures the GitHub Sponsors button. |

## Ways to contribute

- **Fix a broken badge, link, or widget** — these are the most common
  and most appreciated fixes.
- **Improve a GitHub Actions workflow** — e.g. better caching, clearer
  comments, safer defaults.
- **Suggest formatting or accessibility improvements** to the README.
- **Point out anything that renders incorrectly** on mobile or dark
  mode.

Please don't open PRs that:

- Add unrelated personal content
- Change the copyright holder in `LICENSE`
- Remove attribution/comments pointing to the original widget projects
  (`Platane/snk`, `lowlighter/metrics`, `gautamkrishnar/blog-post-workflow`,
  etc.) — these are third-party open-source tools and should stay
  credited.

## Reporting an issue

Open a GitHub Issue and include:

1. What you expected to happen
2. What actually happened (a screenshot helps a lot for rendering bugs)
3. Whether the issue is in `README.md` itself or in one of the
   `.github/workflows/*.yml` files

## Suggesting an improvement

Open an Issue first for anything non-trivial (new sections, new
widgets, restructuring) so it can be discussed before you spend time
on a PR. Small fixes (typos, broken links, dead badges) can go
straight to a pull request.

## Submitting a pull request

1. Fork the repository
2. Create a feature branch:
   ```bash
   git checkout -b fix/broken-badge
   ```
3. Make your changes
4. Commit with a clear message:
   ```bash
   git commit -m "Fix: broken WakaTime badge URL"
   ```
5. Push and open a pull request against `main`:
   ```bash
   git push origin fix/broken-badge
   ```
6. Describe what you changed and why in the PR description

## Workflow conventions

If you're touching a `.github/workflows/*.yml` file:

- Keep the `workflow_dispatch: {}` trigger so it can always be run
  manually from the Actions tab for testing.
- Keep the explanatory comment block at the top of the file — it
  documents what secrets/setup the workflow needs.
- Don't hardcode a GitHub username directly where
  `${{ github.repository_owner }}` would work instead — it keeps the
  workflow portable if the repo is ever forked or renamed.
- Test changes on a fork before opening a PR, since these workflows
  write to the repository (commits, branches, or artifacts).

## Style guide

For README changes:

- Keep headings consistent with the existing emoji + title pattern
- Keep the Table of Contents anchors in sync with any heading you
  rename
- Prefer `<details>` collapsible sections for anything long or
  optional, so the page stays scannable
- Don't add a widget without a short comment noting what setup it
  requires (or that it works out of the box)

## Code of conduct

This project follows the guidelines in [CODE_OF_CONDUCT.md](./CODE_OF_CONDUCT.md).
By participating, you're expected to uphold them.
