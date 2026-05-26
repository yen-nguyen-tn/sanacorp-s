# sanacorp-s — version bump testbed

This repo holds mock fixtures used by the n8n **update-version** workflow.
File paths mirror the real Sanacorp-S Connect repo so the workflow can be
ported back unchanged:

- `package.json` (root) — semver `version`
- `app/src/version.json` — `logoutReload` / `systemInformation` counters

The workflow is triggered from Slack, bumps both files on a new branch off
`develop`, and opens a PR back into `develop`.

Everything else is gitignored — this repo intentionally contains only the
fields the workflow reads and updates.
