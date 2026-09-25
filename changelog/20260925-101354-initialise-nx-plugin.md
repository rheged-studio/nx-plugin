---
title: Initialise nx-plugin as an estate package without npm publish
release_note: ""
version:
created_at: "2026-09-25T10:13:54Z"
merged_at:
branch: cursor/initialise-nx-plugin-5d6e
pr:
commit:
author: cursoragent@cursor.com
co_authors: []
category: chore
breaking: false
issues: []
---

## Changed

- Rewrote the package identity from the template placeholder to `@rheged-studio/nx-plugin` and reset `changelog/` to only `README.md` (the copied template entries had been stamped `0.0.0`).
- Pulled the locked shared agent-skills set and generated committed per-skill `config.json` files.
- Added `.github/workflows/changelog-enrich.yml` (`mode: enrich`) so merged PRs get post-merge changelog metadata without a version stamp.
- Gated `pkg-release.yml` jobs with `if: ${{ false }}` so a still-active Release workflow cannot publish or stamp `0.0.0`. npm publish, Clacks `matrix.repo`, and GitHub Releases stay deferred.
