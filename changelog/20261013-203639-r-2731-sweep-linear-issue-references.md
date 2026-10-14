---
title: Sweep Linear issue references to R and C keys
release_note: ""
version:
created_at: "2026-10-13T20:36:39Z"
merged_at:
branch: r-2731-nx-plugin-sweep-issue-references
pr:
commit:
author: rob@rheged.studio
co_authors: []
category: chore
breaking: false
issues:
  - R-2731
stats:
  loc_added:
  loc_removed:
  files_changed:
---

## Changed

- Rewrote old `A-n` Linear issue references to their new `R` and `C` keys through the committed
  Linear-migrate mapping: 68 files scanned, 32 changed, 177 references rewritten, no flags.
- Left vendored skills, changelog file names and `branch:` lines verbatim, as the tool intends.
- Reflowed one test file where the shorter IDs changed Prettier line breaks.
