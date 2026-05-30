# v

Aggregator workspace for the booga vsuite. Bun workspaces + git submodules.

- `packages/v<Name>/` is a git submodule pointing at the per-package repo at a tagged commit.
- `apps/test/`, `apps/docs/`, `apps/web/` are workspace packages (not submodules) that consume `packages/v*` via the workspace protocol.

## Setup

```
git submodule update --init --recursive
bun install
```

## Versioning

The aggregator is not versioned and not published. Per-package versions are pinned via the submodule SHA at the tagged release. Submodule bumps land as tiny dedicated commits.
