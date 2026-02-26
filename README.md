# Agent Behavior Contract

A reusable behavior layer for AI coding agents (Cursor, Codex, etc.).

## What It Does

Enforces consistent, high-quality agent output through:

- **Tone discipline** — Concise, no filler, professional
- **Documentation-first** — Read before coding, verify before importing
- **Quality gates** — Done criteria, validation checklist
- **Anti-slop rules** — No obvious comments, no tutorial text

## Files

| File | Purpose |
|------|---------|
| `AGENTS.md` | The behavior contract. Place in workspace root. |
| `SKILL.md` | Installation and usage guide. |

## Quick Start

```bash
# Clone to your skills directory
git clone https://github.com/yourusername/agent-behavior-skill.git

# Copy to Cursor
cp AGENTS.md ~/projects/your-project/

# Or install as skill
cp SKILL.md AGENTS.md ~/.cursor/skills/agent-behavior/
```

## How It Works

1. Agent reads `AGENTS.md` at session start
2. Applies tone constraints automatically
3. Queries documentation before framework decisions
4. Executes done criteria before completing tasks

## Hierarchy

```
ENFORCEMENT (workflow rules)
        ↓
WORKFLOW (stage machine)
        ↓
AGENT BEHAVIOR (this file)
        ↓
SKILLS (specialized capabilities)
```

## Customization

Edit `AGENTS.md` sections:

- **§3 Decision Triggers** — Add your skill invocation rules
- **§5 MCP** — Set your documentation source
- **§7 Landing Polish** — Define your quality checklist

## License

MIT
