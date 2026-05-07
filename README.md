# Claude Code Configuration

Personal Claude Code global configuration, tracked with git for multi-machine sync.

## Tracked files

- `settings.json` — model, plugins, hooks, feature flags
- `CLAUDE.md` — global instructions (references `RTK.md`)
- `RTK.md` — [RTK](https://github.com/mhv2109/rtk) token-optimized CLI proxy usage
- `skills/` — custom skills

## Ignored (not tracked)

`projects/`, `todos/`, `plans/`, `plugins/cache/`, `shell-snapshots/`,
`file-history/`, `sessions/`, `history.jsonl`, `statsig/`, `backups/`

## Bootstrap on a new machine

```sh
# Back up existing config if present
mv ~/.claude ~/.claude.bak

# Clone
git clone git@github.com:mhv2109/claude-config.git ~/.claude

# If rtk is not installed on this machine, neutralize the hook:
# Create ~/.claude/settings.local.json with an empty hooks object or
# install rtk: https://github.com/mhv2109/rtk
```

## Docs

- [Claude Code settings](https://docs.anthropic.com/en/docs/claude-code/settings)
- [Claude Code best practices](https://code.claude.com/docs/en/best-practices)
