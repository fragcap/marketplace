# FragCap Marketplace

The official plugin registry for [FragCap](https://github.com/fragcap/plugin) — the Claude Code plugin that captures knowledge capsules from your sessions.

## What is this?

`marketplace.json` is the machine-readable catalog consumed by the Claude Code plugin marketplace. It lists the fragcap plugin with its metadata, source URL, and current version.

## Fields in `marketplace.json`

| Field | Description |
|-------|-------------|
| `name` | Plugin identifier |
| `source.url` | Git URL used to install the plugin |
| `version` | Must match the version in `plugin/plugin.json` |
| `homepage` | Project homepage |
| `repository` | Source code repository |
| `license` | License identifier |
| `keywords` | Searchable tags in the marketplace |
| `category` | Marketplace category |

## Adding a new plugin

1. Fork this repository.
2. Add a new entry to the `plugins` array in `.claude-plugin/marketplace.json`.
3. Open a pull request — the entry will be reviewed before merging.

## Version update process

When the fragcap plugin publishes a new release:

1. Update `version` in `.claude-plugin/marketplace.json` to match the new version in [fragcap/plugin](https://github.com/fragcap/plugin).
2. Open a pull request with the title `chore: bump fragcap to vX.Y.Z`.
3. Merge after CI passes.

> The version in this file must always match the `version` field in `fragcap/plugin/.claude-plugin/plugin.json`.
