# Agent Behavior Contract Skill

> A reusable behavior layer for AI agents.
> Defines tone standards, documentation discipline, and quality gates.
> **Version**: 1.0.0

---

## Installation

Copy `SKILL.md` and `AGENTS.md` to your Cursor/Codex skills directory:

```bash
# Cursor
cp SKILL.md AGENTS.md ~/.cursor/skills/agent-behavior/

# Codex
cp SKILL.md AGENTS.md ~/.codex/skills/agent-behavior/
```

---

## Purpose

This skill enforces consistent agent behavior across sessions:

- **Tone Standards** — Concise, professional communication
- **Anti-Slop Rules** — No filler, no obvious comments, no tutorial text
- **Documentation-First** — Read before coding, verify before importing
- **Quality Gates** — Done criteria, validation checklist

---

## Usage

When the skill is active, the agent will automatically:

1. Re-read `AGENTS.md` at session start
2. Apply tone constraints to all output
3. Query documentation sources before framework decisions
4. Execute done criteria before marking tasks complete

---

## Integration

### With Workflow Rules

Place `AGENTS.md` in your workspace root alongside `.cursor/rules/`:

```
~/.cursor/
├── .cursor/rules/          (enforcement layer)
├── AGENTS.md               (behavior layer) ← this skill
└── skills/
```

Hierarchy: **Enforcement → Workflow → Agent Behavior → Skills**

### With Recurring Tasks

Create `RECURRING_TASKS.md` to define scheduled behaviors:

```markdown
## Validation Check
- Frequency: weekly
- Action: Run Landing Polish on all public pages
```

---

## Customization

Edit `AGENTS.md` to adjust for your context:

- **Section 3** (Decision Triggers) — Add your own skill invocation rules
- **Section 5** (MCP) — Update to your documentation source
- **Section 7** (Landing Polish) — Define your quality checklist

---

## License

MIT — Use, modify, share freely.
