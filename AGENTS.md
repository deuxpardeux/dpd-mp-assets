# Agent instructions for dpd-mp-assets

## Code graph and workflow maps (Deux par Deux)

Before changing code or workflows, read the Archify map and query Graphify (graphify-latest).

Query the shared `code_catalog.jsonl` on the `graphify-latest` release in `deuxpardeux/dpd-tools`. This repo's structure, scripts, and manifests are included; image and other binary blobs are not indexed.

```bash
gh release download graphify-latest --repo deuxpardeux/dpd-tools --pattern code_catalog.jsonl --dir /tmp/graphify --clobber
rg -i 'dpd-mp-assets/' /tmp/graphify/code_catalog.jsonl
```

See dpd-tools `.claude/skills/graphify-query/SKILL.md` and `bridge/GRAPHIFY.md`.
The catalog refreshes at 06:35 and 18:35 UTC. If the release is unavailable or a file is absent, use a scoped local file index or GitHub path search. Do not install Graphify MCP on W10.

This repo is excluded from the shared catalog (image assets). Use the
catalog for covered company code, then scoped local lookup for this repo.
Never upload this repo's contents to the shared catalog.
