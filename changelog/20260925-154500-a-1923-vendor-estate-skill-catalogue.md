---
title: Vendor estate skill catalogue (Matt packs + rheged-skills-setup)
release_note: Agent skills now include the full Rheged and Matt Pocock catalogue; legacy initialise-skills removed.
created_at: "2026-09-25T14:45:00Z"
merged_at: "2026-09-25T14:54:07Z"
branch: a-1923-vendor-estate-skill-catalogue-nx-plugin
pr: 9
commit: d7d85da
author: rob@rheged.studio
co_authors: []
category: chore
breaking: false
issues:
  - A-1923
affected_packages: []
stats:
  files_changed: 220
  loc_added: 8197
  loc_removed: 350
  commits:
---

## Changed

- Installed the estate skill catalogue via `rheged-skills-setup --install --write` (Rheged ship set, Matt Pocock packs, and `rheged-skills-setup`), with configs restored from HEAD (A-706).
- Removed legacy `initialise-skills` in favour of `rheged-skills-setup`.
- Kept repo-specific `initialise-package-repo` and refreshed `.claude/skills.lock` / `skills-lock.json`.
