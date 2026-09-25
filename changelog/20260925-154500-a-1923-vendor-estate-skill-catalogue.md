---
title: "Vendor estate skill catalogue (Matt packs + rheged-skills-setup)"
release_note: "Agent skills now include the full Rheged and Matt Pocock catalogue; legacy initialise-skills removed."
created_at: "2026-09-25T14:45:00Z"
merged_at:
branch: a-1923-vendor-estate-skill-catalogue-nx-plugin
pr:
commit:
author: "rob@rheged.studio"
co_authors: []
category: chore
breaking: false
issues: ["A-1923"]
affected_packages: []
stats:
  files_changed:
  loc_added:
  loc_removed:
  commits:
---

## Changed

- Installed the estate skill catalogue via `rheged-skills-setup --install --write` (Rheged ship set, Matt Pocock packs, and `rheged-skills-setup`), with configs restored from HEAD (A-706).
- Removed legacy `initialise-skills` in favour of `rheged-skills-setup`.
- Kept repo-specific `initialise-package-repo` and refreshed `.claude/skills.lock` / `skills-lock.json`.
