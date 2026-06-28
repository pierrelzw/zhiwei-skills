# zhiwei_skills — Marketplace Maintainer Guide

Central marketplace registry for Claude Code plugins by pierrelzw.

This is the canonical shared instruction source for all AI agents working in
this repo (Claude Code, Codex, Gemini). `CLAUDE.md` and `GEMINI.md` import it
via `@AGENTS.md`; do not duplicate these rules in those files.

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

When a plugin repo bumps its `.claude-plugin/plugin.json` version, update **both**
the matching `version` field in this marketplace's `marketplace.json` **and** the
matching row in the `README.md` plugin table. `marketplace.json` is the source of
truth; the README table must always mirror it (same plugins, same versions, same
order).
