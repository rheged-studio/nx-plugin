---
title: remove Dependabot configuration
release_note: ""
created_at: "2026-11-18T11:23:11Z"
merged_at: ""
branch: disable-dependabot
pr:
commit: ""
author: rob@rheged.studio
co_authors: []
category: chore
breaking: false
issues: []
stats:
  loc_added:
  loc_removed:
  files_changed:
version: ""
---

## Removed

- **Dependabot is switched off.** Deleted `.github/dependabot.yml`, so Dependabot no longer opens weekly GitHub Actions or npm update PRs. This follows the estate-wide decision to stop running Dependabot.

## Changed

- **`CLAUDE.md` no longer says Dependabot bumps the shared reusable callers.** They float on the shared-workflows `@v1` major tag rather than being SHA-pinned, so the note was already stale.
