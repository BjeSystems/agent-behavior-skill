# Agent Behavior Contract

A universal behavior template for AI agents (Cursor, Codex, etc.).
Copy `AGENTS.md` to any project to enforce consistent, high-quality agent behavior.

**Version**: 2.0.0 — Now with 16 sections including Git Discipline and Local Checkpoints.

## What It Does

Enforces consistent agent output across all your projects:

- **Tone Discipline** — Concise, no filler, professional communication
- **Documentation-First** — Read before coding, create docs after coding
- **Quality Gates** — Done criteria, validation checklist
- **Anti-Slop Rules** — No obvious comments, no tutorial text
- **Git Discipline** — Time-based commits (every 15 min) + change-based commits
- **Local Checkpoints** — 15-minute recovery snapshots via git stash
- **Secrets Detection** — Automatic scan before public push
- **Repository Visibility** — Private-by-default stance

## Files

| File | Purpose |
|------|---------|
| `AGENTS.md` | The behavior contract (16 sections). Copy to project root. |
| `SKILL.md` | Template guide with customization instructions. |

## Quick Start

### Method 1: Project-Level (Recommended)

Copy `AGENTS.md` directly to your project:

```bash
# Any project
cp AGENTS.md /path/to/your-project/

# Or download raw file
curl -O https://raw.githubusercontent.com/<username>/agent-behavior-skill/main/AGENTS.md
```

### Method 2: As Personal Skill (Cursor)

```bash
# Install as Cursor skill
mkdir -p ~/.cursor/skills/agent-behavior
cp SKILL.md AGENTS.md ~/.cursor/skills/agent-behavior/
```

## How It Works

When `AGENTS.md` is in project root, agent automatically:

1. Reads `AGENTS.md` at session start
2. Applies tone constraints to all output
3. Queries documentation before framework decisions
4. Creates documentation for code changes (§5)
5. Commits work every 15 minutes (§16)
6. Executes done criteria before completing tasks (§7)
7. Creates local checkpoints for crash recovery (§17)

## Hierarchy

```
ENFORCEMENT (.cursor/rules/)
        ↓
WORKFLOW (stages 0-6)
        ↓
AGENT BEHAVIOR (AGENTS.md) ← Copy this file
        ↓
SKILLS (specialized capabilities)
```

## Customization

Edit `AGENTS.md` after copying to match your project:

### Essential Sections to Customize

| Section | What to Edit |
|---------|--------------|
| §3 Decision Triggers | Replace `ui-ux skill`, `react skill` with your actual skill names |
| §6 MCP Integration | Update documentation source if not using Context7 |
| §7 Done Criteria | Adjust checklist for your workflow (testing, deployment, etc.) |
| §12-13 Visibility/Secrets | Modify for your security requirements |
| §16 Git Discipline | Adjust commit frequency (default: 15 minutes) |
| §17 Local Checkpoints | Remove if not using stash-based recovery |

### Examples by Project Type

**Web Development Project:**
```markdown
§3 Triggers:
- "landing page" → Trigger Landing Polish + design skill
- "React component" → Trigger react-best-practices skill
```

**Backend/API Project:**
```markdown
§3 Triggers:
- "API endpoint" → Trigger api-design skill
- "database" → Trigger db-schema skill
§7 Done Criteria:
- Add: API tests written
- Add: Migration tested
```

**Infrastructure/DevOps:**
```markdown
§3 Triggers:
- "Terraform" → Trigger iac-validation skill
- "Docker" → Trigger container-best-practices skill
§12 Visibility:
- Emphasize: All infra repos private
```

## Version History

- **v2.0** — Added Code Documentation Creation (§5), Git Discipline (§16), Local Checkpoints (§17), Secrets Detection (§13)
- **v1.0** — Initial release with Tone Standards, Anti-Slop, Done Criteria

## License

MIT — Use, modify, share freely.
