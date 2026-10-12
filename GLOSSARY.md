# Estate Nx plugin

`@rheged-studio/nx-plugin` is the Rheged Studio estate's Nx plugin, intended to scaffold packages through generators. Today it is a shell: the publishing and changelog machinery is live, but the plugin's own public API is still a placeholder.

## Language

### The plugin

**Estate Nx plugin**:
The package `@rheged-studio/nx-plugin`, the single home for the estate's Nx scaffolding.
_Avoid_: Nx package, nx-plugin library

**Generator**:
An Nx generator exported by the plugin that scaffolds code into a workspace. Generators are the plugin's intended public API.
_Avoid_: Schematic, scaffolder, template

**Generators-first**:
The plugin's stated design stance ("generators-first" in its description) that generators, not other Nx extension points, are its primary public surface.
_Avoid_: Executor-first

**Hybrid UI/util scaffolding**:
The remit named in the package description: scaffolding that covers both UI packages and utility packages. The concrete generator set is not yet defined.
_Avoid_: Full-stack scaffolding

**Placeholder API**:
The current `src/index.ts`, which exports only `PACKAGE_NAME`, standing in until the first real generators land.
_Avoid_: Stub, skeleton

### Provenance

**Package template**:
The `npm-package-template` repo this plugin was spawned from, which supplies its CI, release and changelog shell.
_Avoid_: Boilerplate, starter

### Release and changelog

**Publish deferral**:
The state in which npm publishing is switched off: `pkg-release.yml` (workflow name `Release`) is dormant and its jobs are gated on the repository variable `ENABLE_NPM_PUBLISH`.
_Avoid_: Unpublished, private mode

**Trusted Publisher bootstrap**:
The one-off step of binding npm Trusted Publishing to `pkg-release.yml`, which must happen before publishing can be enabled and before the repo joins Clacks `matrix.repo`.
_Avoid_: First publish, npm setup

**Clacks**:
The estate's release orchestrator (`rheged-studio/clacks`), which opens and merges release-please PRs and cuts releases for repos listed in its `matrix.repo`.
_Avoid_: Release bot, orchestrator

**GO/NO GO**:
The single aggregator check-run in `ci.yml` that the estate treats as the required merge gate; it succeeds only if every other job succeeded or was skipped.
_Avoid_: Build & Lint, CI status

**Changelog entry**:
One dated Markdown file in `changelog/` per PR, named `<YYYYMMDD-HHMMSS>-<slug>.md` and written by `/send-it`.
_Avoid_: Release notes, CHANGELOG.md

**Enrich**:
The post-merge changelog mode (`mode: enrich`, run by `changelog-enrich.yml`) that fills `merged_at`, `commit`, `pr` and `stats` but leaves `version` blank. It is what this repo runs today.
_Avoid_: Backfill

**Finalise**:
The npm-target changelog mode (`mode: finalise`, run from `pkg-release.yml`) that does everything Enrich does and also stamps `version`. It replaces Enrich once publishing is enabled.
_Avoid_: Stamp, release enrich
