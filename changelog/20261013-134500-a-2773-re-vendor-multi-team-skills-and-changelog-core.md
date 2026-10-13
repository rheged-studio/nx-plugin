---
title: Re-vendor multi-team skills and changelog-core 1.2.0
release_note: ""
version:
created_at: "2026-10-13T13:45:00Z"
merged_at:
branch: a-2773-nx-plugin-re-vendor-the-multi-team-skills-and-changelog-core
pr:
commit:
author: rob@rheged.studio
co_authors: []
category: chore
breaking: false
issues:
  - A-2773
  - A-2730
stats:
  loc_added: 0
  loc_removed: 0
  files_changed: 0
---

## Changed

- Re-vendored the estate skill catalogue from agent-skills v1.13.0 (multi-team Linear skills) into `.claude/skills` and `.agents/skills`.
- Set `issueKeys` to `["R", "A"]` in the root and skill configs; `linearTeamName` stays "Rheged Studio".
- Bumped the `@rheged-studio/changelog-core` devDependency to `^1.2.0`.
