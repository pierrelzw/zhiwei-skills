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
| [bilingual-video-sub](https://github.com/pierrelzw/bilingual-video-sub) | Bilingual Chinese+English subtitle pipeline — video → EN/ZH SRT + burned mp4 | 0.1.0 |
| [smart-cut-monologue](https://github.com/pierrelzw/smart-cut-monologue) | Smart-cut 口播 videos on Apple Silicon — mlx-qwen3-asr + 剪映-style review UI + ffmpeg | 0.1.0 |
| [media-to-srt](https://github.com/pierrelzw/media-to-srt) | Transcribe video or audio (URL or local) → SRT using whisper.cpp + yt-dlp (YouTube/Bilibili/小红书/抖音/podcasts/voice memos/...) | 0.2.0 |
| [xiaoyuzhou-to-audio](https://github.com/pierrelzw/xiaoyuzhou-to-audio) | Download 小宇宙 podcast episodes to local .m4a via aria2c — up to 6 episodes in parallel | 0.1.0 |
| [issue-workflow](https://github.com/pierrelzw/issue-workflow) | End-to-end GitHub issue workflow — preflight → plan (codex review) → worktree → implement → verify → review → PR → CI → merge | 0.1.0 |
| [time-report](https://github.com/pierrelzw/time-report) | Interactive HTML Gantt + token/cost report for Claude Code & Codex sessions | 3.5.0 |

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
