---
name: agent-behavior
description: Universal agent behavior contract template. Copy AGENTS.md to project root to enforce consistent agent behavior across sessions. Version 2.0.
---

# Agent Behavior Template

> A universal behavior layer for AI agents.
> Defines tone standards, documentation discipline, quality gates, git discipline, and time-based recovery.
> **Version**: 2.0.0

---

## Installation

### As Project-Level Behavior (Recommended)

Copy `AGENTS.md` to your project root:

```bash
cp AGENTS.md /path/to/your/project/
```

The agent will automatically detect and apply behavior rules from project root.

### As Personal Skill (Cursor/Codex)

Copy to skills directory:

```bash
# Cursor
cp SKILL.md AGENTS.md ~/.cursor/skills/agent-behavior/

# Codex
cp SKILL.md AGENTS.md ~/.codex/skills/agent-behavior/
```

---

## Purpose

This template enforces consistent agent behavior across sessions:

- **Tone Standards** — Concise, professional communication
- **Anti-Slop Rules** — No filler, no obvious comments, no tutorial text
- **Documentation-First** — Read before coding, create docs after coding
- **Quality Gates** — Done criteria, validation checklist
- **Git Discipline** — Time-based and change-based commits
- **Local Checkpoints** — 15-minute recovery snapshots (optional)

---

## Template Structure

| Section | Content |
|---------|---------|
| 1 | Tone Standards |
| 2 | Anti-Slop Constraints |
| 3 | Decision Triggers (customize for your skills) |
| 4 | Documentation-First Protocol |
| 5 | Code Documentation Creation |
| 6 | MCP Context7 Integration |
| 7 | Done Criteria |
| 8 | Landing Polish Trigger |
| 9 | External Knowledge Usage |
| 10 | Recurring Task Binding |
| 11 | Conflict Detection |
| 12 | Repository Visibility Behavior |
| 13 | Secrets Detection Protocol |
| 14 | Agent Autonomy & Spatial Reasoning |
| 15 | Identity & Scope |
| 16 | Git Discipline |
| 17 | Local Checkpoints (optional) |

---

## Customization Guide

Edit `AGENTS.md` after copying to match your project:

### Essential Customizations

**Section 3 — Decision Triggers:**
Replace generic skill names with your specific ones:
- `ui-ux skill` → `your-design-skill`
- `react skill` → `your-frontend-skill`
- `rule-creation skill` → `your-rule-skill`

**Section 6 — MCP Integration:**
Update to your documentation source if not using Context7.

**Section 7 — Done Criteria:**
Adjust checklist for your workflow (add testing steps, deployment checks, etc.).

**Section 16 — Git Discipline:**
Modify commit frequency (default: 15 minutes) or rules.

**Section 17 — Local Checkpoints:**
Optional. Remove if not using stash-based recovery.

### Project-Specific Additions

Add project-specific rules in new sections (18, 19, etc.) or modify existing ones.

---

## Usage

When `AGENTS.md` is in project root, the agent will automatically:

1. Re-read `AGENTS.md` at session start
2. Apply tone constraints to all output
3. Query documentation sources before framework decisions
4. Create documentation for code changes (Section 5)
5. Execute done criteria before marking tasks complete
6. Persist work via git commits (Section 16)
7. Create local checkpoints every 15 minutes (Section 17, optional)

---

## Integration

### With Workflow Rules

Place `AGENTS.md` in your workspace root alongside `.cursor/rules/`:

```
your-project/
├── .cursor/rules/          (enforcement layer)
├── AGENTS.md               (behavior layer) ← this template
├── README.md
└── src/
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

## Version History

- **2.0.0** — Added Code Documentation Creation, Git Discipline, Local Checkpoints (16 sections)
- **1.0.0** — Initial template with Tone Standards, Anti-Slop, Done Criteria (4 sections)

---

## License

MIT — Use, modify, share freely.
