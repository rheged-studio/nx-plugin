---
title: Initialise nx-plugin as an estate package without npm publish
release_note: ""
version:
created_at: "2026-09-25T10:13:54Z"
merged_at: "2026-09-25T11:28:23Z"
branch: cursor/initialise-nx-plugin-5d6e
pr: 7
commit: f2e780e
author: cursoragent@cursor.com
co_authors: []
category: chore
breaking: false
issues: []
stats:
  loc_added: 1095
  loc_removed: 1996
  files_changed: 90
---

## Changed

- Rewrote the package identity from the template placeholder to `@rheged-studio/nx-plugin` and reset `changelog/` to only `README.md` (the copied template entries had been stamped `0.0.0`).
- Pulled the locked shared agent-skills set and generated committed per-skill `config.json` files.
- Added `.github/workflows/changelog-enrich.yml` (`mode: enrich`) so merged PRs get post-merge changelog metadata without a version stamp.
- Gated `pkg-release.yml` jobs on repository variable `ENABLE_NPM_PUBLISH` so a still-active Release workflow cannot publish or stamp `0.0.0`. npm publish, Clacks `matrix.repo`, and GitHub Releases stay deferred.
- Skip `.github/workflows/changelog-enrich.yml` when `ENABLE_NPM_PUBLISH` is `'true'`, so enrich and finalise cannot both write `changelog/**` during a half-flipped npm enable.
- Point `CLAUDE.md` `npm-release` / attestation commands at `rheged-studio/nx-plugin` and drop the dead `README.md#the-required-check-ruleset` link.
