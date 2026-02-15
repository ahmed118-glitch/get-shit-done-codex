# Compatibility: Claude → Codex for get-shit-done

## Tool mapping
- `Task(...)` → `spawn_agent` + `wait`.
- `AskUserQuestion` → direct user interaction in chat.
- Bash-style shell helpers → PowerShell commands.

## Path mapping
- `C:/Users/Ahmed/.claude/get-shit-done/...` → `.claude/get-shit-done/...`
- `C:/Users/Ahmed/.claude/agents/...` → `.claude/agents/...`

## CLI mapping
- Use `node .claude/get-shit-done/bin/gsd-tools.js ...`.
- Keep `--raw` when upstream workflow uses it.
- Parse JSON by `ConvertFrom-Json`.

## Subagent mapping
- `subagent_type=gsd-*` maps to equivalent role contract in `.claude/agents/gsd-*.md`.
- Unspecified `subagent_type` values default to command-context Codex agent behavior.
