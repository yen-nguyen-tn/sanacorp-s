# sanacorp-s — version bump testbed

This repo holds mock fixtures used by the n8n **update-version** workflow.
The workflow (triggered from Slack) reads and bumps:

- `mock/version.json` — `logoutReload` / `systemInformation` counters
- `mock/package.json` — semver `version`

It then opens a PR against the default branch.

The real Sanacorp-S Connect codebase lives elsewhere; this repo intentionally
contains only the files the workflow needs to read and update.
