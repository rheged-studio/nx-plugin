# @rheged-studio/nx-plugin

Estate Nx plugin — generators-first hybrid UI/util scaffolding.

`src/` is still the template placeholder. npm publish is **not** enabled: the
Release workflow (`pkg-release.yml`) is dormant until Trusted Publishing is
bootstrapped. Dated changelog notes still run after merge via
[`.github/workflows/changelog-enrich.yml`](.github/workflows/changelog-enrich.yml)
(`mode: enrich` — post-merge metadata, no version stamp).

## Commands

```bash
pnpm install
pnpm run build
pnpm tsc
pnpm lint
pnpm test
pnpm validate:changelog
```

Node 22 (`engines.node: ">=22"`). pnpm is pinned via `packageManager`.

## Changelog

One dated Markdown file per PR under [`changelog/`](changelog/README.md), written
by `/send-it`. Entries stay version-less until this package joins the npm
release path (`matrix.repo` + `pkg-release.yml` `mode: finalise`).
