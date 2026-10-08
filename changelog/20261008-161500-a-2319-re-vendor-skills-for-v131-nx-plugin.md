---
title: Re-vendor agent skills for mattpocock/skills 1.3.1
release_note: ""
version:
created_at: "2026-10-08T16:15:00Z"
merged_at:
branch: a-2319-re-vendor-skills-for-v131-nx-plugin
pr:
commit:
author: rob@rheged.studio
co_authors: []
category: chore
breaking: false
issues:
  - A-2319
---

## Changed

- Refreshed Rheged ship bundles and Matt Pocock engineering/productivity packs via `fleet-update`.
- Dropped upstream-removed `resolving-merge-conflicts`; added Rheged `pr`, Matt `implement-spec`, and `retro`.
- Renamed domain-modeling `CONTEXT-FORMAT.md` to `GLOSSARY-FORMAT.md` (mattpocock 1.3.0 glossary rename).
- Restored triage-pr unattended Phase B settings (`humanEnvelope: false`, `followUpLabel: follow-up`).
- Left repo-local `initialise-package-repo` untouched.
