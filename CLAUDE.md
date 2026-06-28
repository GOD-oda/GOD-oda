# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this repository is

This is a GitHub **profile repository** (`GOD-oda/GOD-oda`). Because the repo name matches the
username, GitHub renders the root `README.md` directly on the user's profile page
(https://github.com/GOD-oda). There is no application code, no build system, no tests, and no lint —
the only workflow is editing Markdown/images and committing. Verification means checking how the
Markdown renders on GitHub, not running a command.

## Structure and conventions

- **`README.md`** (root) — the profile page. It composes itself from external badge/stats services
  (`github-readme-stats.vercel.app`, `shields.io`, `komarev.com` page-view counter) plus a
  **Certifications** section. When adding a certification, place the badge image under
  `certifications/<vendor>/` and wrap the `<img>` in an `<a>` linking to its public Credly badge URL,
  following the existing AWS entries. The certification headings are pre-seeded by level
  (Foundational / Associate / Professional / Specialty for AWS; the GCP block is a placeholder with
  no badges yet) — add new badges under the matching level rather than creating new sections.

- **`16personalities/`** — a chronological log of 16personalities test results. `README.md` here has
  one `## YYYY-M-D` heading per test date, each immediately followed by `![YYYY-M-D](img/YYYY-M-D.png)`.
  Adding an entry = drop the screenshot into `16personalities/img/` and append a new dated section at
  the **bottom** (entries are oldest-first).
  - **Date format is not zero-padded**: use `2024-7-1`, not `2024-07-01` (note existing files like
    `img/2024-7-1.png` and `img/2022-11-10.png`). The heading text, the image alt text, and the
    image filename must all use the identical date string, or the image won't resolve.

- **`certifications/`** — badge images only, organized by vendor (currently `aws/`), referenced from
  the root README.

## Notes

- `.gitignore` only excludes `.idea/` (JetBrains). Commit images alongside the Markdown that
  references them; relative image paths must stay correct for GitHub to render them.
- Image paths in Markdown are repo-relative and resolve on GitHub's rendered view — there is no local
  preview server in this repo.
