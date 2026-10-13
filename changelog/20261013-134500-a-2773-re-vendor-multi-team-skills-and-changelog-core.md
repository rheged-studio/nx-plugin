---
title: Re-vendor multi-team skills and changelog-core 1.2.0
release_note: ""
version:
created_at: "2026-10-13T13:45:00Z"
merged_at: "2026-10-13T13:31:51Z"
branch: a-2773-nx-plugin-re-vendor-the-multi-team-skills-and-changelog-core
pr: 13
commit: 44c6b3b
author: rob@rheged.studio
co_authors: []
category: chore
breaking: false
issues:
  - R-2773
  - R-2730
stats:
  loc_added: 2302
  loc_removed: 704
  files_changed: 83
---

## Changed

- Re-vendored the estate skill catalogue from agent-skills v1.13.0 (multi-team Linear skills) into `.claude/skills` and `.agents/skills`.
- Set `issueKeys` to `["R", "A"]` in the root and skill configs; `linearTeamName` stays "Rheged Studio".
- Bumped the `@rheged-studio/changelog-core` devDependency to `^1.2.0`.
