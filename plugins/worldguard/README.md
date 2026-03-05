# WorldGuard Docs

This folder is reserved for WorldGuard documentation content sourced from:

- https://github.com/EngineHub/WorldGuardDocs

## Automated sync

Manual cloning is optional now. This repository includes a GitHub Actions workflow that:

- runs nightly,
- can also be run on demand (`Actions` → `Sync WorldGuard Docs` → `Run workflow`),
- checks out `EngineHub/WorldGuardDocs` into `plugins/worldguard/upstream`,
- commits + pushes only when upstream content changed.

Workflow file:

- `.github/workflows/sync-worldguard.yml`

## Why this helps with `CONNECT tunnel failed, response 403`

If your local environment blocks GitHub clone traffic, the sync can still happen in GitHub-hosted Actions runners (where your local proxy/tunnel is not involved).
