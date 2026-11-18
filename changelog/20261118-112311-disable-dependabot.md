---
title: remove Dependabot configuration
release_note: ""
created_at: "2026-11-18T11:23:11Z"
merged_at: "2026-11-18T11:52:37Z"
branch: disable-dependabot
pr: 20
commit: 5e38fdc
author: rob@rheged.studio
co_authors: []
category: chore
breaking: false
issues: []
stats:
  loc_added: 28
  loc_removed: 37
  files_changed: 3
version: ""
---

## Removed

- **Dependabot is switched off.** Deleted `.github/dependabot.yml`, so Dependabot no longer opens weekly GitHub Actions or npm update PRs. This follows the estate-wide decision to stop running Dependabot.

## Changed

- **`CLAUDE.md` no longer says Dependabot bumps the shared reusable callers.** They float on the shared-workflows `@v1` major tag rather than being SHA-pinned, so the note was already stale.
