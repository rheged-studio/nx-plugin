---
title: Sweep Linear issue references to R and C keys
release_note: ""
version:
created_at: "2026-10-13T20:36:39Z"
merged_at: "2026-10-14T08:06:55Z"
branch: r-2731-nx-plugin-sweep-issue-references
pr: 16
commit: 8e70743
author: rob@rheged.studio
co_authors: []
category: chore
breaking: false
issues:
  - R-2731
stats:
  loc_added: 153
  loc_removed: 128
  files_changed: 33
---

## Changed

- Rewrote old `A-n` Linear issue references to their new `R` and `C` keys through the committed
  Linear-migrate mapping: 68 files scanned, 32 changed, 177 references rewritten, no flags.
- Left vendored skills, changelog file names and `branch:` lines verbatim, as the tool intends.
- Reflowed one test file where the shorter IDs changed Prettier line breaks.
