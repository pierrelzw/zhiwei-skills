# zhiwei_skills — Marketplace Maintainer Guide

Central marketplace registry for Claude Code plugins by pierrelzw.

## Structure

```
.claude-plugin/
  marketplace.json    # Plugin registry — the only file the marketplace system reads
README.md             # User-facing docs with plugin table and install instructions
```

## Adding a new plugin

1. Add an entry to `.claude-plugin/marketplace.json` → `plugins` array:
   ```json
   {
     "name": "<plugin-name>",
     "source": { "source": "github", "repo": "pierrelzw/<repo>" },
     "description": "...",
     "version": "x.y.z",
     "author": { "name": "pierrelzw" },
     "repository": "https://github.com/pierrelzw/<repo>",
     "license": "MIT",
     "keywords": [...],
     "category": "productivity"
   }
   ```
2. Add a row to the "Available Plugins" table in `README.md`
3. Commit and push

## Version sync

When a plugin repo bumps its `.claude-plugin/plugin.json` version, update the matching `version` field in this marketplace's `marketplace.json` to stay in sync.
