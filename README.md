# zhiwei_skills

Central marketplace for Claude Code plugins by pierrelzw.

## Installation

```bash
claude plugin marketplace add pierrelzw/zhiwei_skills
```

## Available Plugins

| Plugin | Description | Version |
|--------|-------------|---------|
| [search-flights](https://github.com/pierrelzw/search-flights) | Search and compare flight prices across flexible date ranges using Google Flights — bilingual Chinese/English | 0.1.0 |
| [mac-doctor](https://github.com/pierrelzw/mac-doctor) | macOS system doctor — system info, disk cleanup, and maintenance | 0.1.0 |

## Installing Plugins

### Global (all projects)

```bash
claude plugin install search-flights@pierrelzw --scope user
```

### Project only (current project)

```bash
claude plugin install search-flights@pierrelzw --scope project
```

### Scope reference

| Scope | Flag | Effect |
|-------|------|--------|
| User (global) | `--scope user` | Available in all projects (default) |
| Project | `--scope project` | Shared with team via `.claude/plugins.json` |
| Local | `--scope local` | Local only, not committed to git |

## Managing Plugins

```bash
claude plugin list                                      # List installed plugins
claude plugin update search-flights@pierrelzw           # Update to latest version
claude plugin disable search-flights@pierrelzw          # Temporarily disable
claude plugin enable search-flights@pierrelzw           # Re-enable
claude plugin uninstall search-flights@pierrelzw        # Remove
```
