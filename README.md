# Deprecated Repository

## This repository has evolved into:

**https://github.com/BjeSystems/agentmd-skill**

All active development continues there.

This repository remains as historical reference.

---

## Migration Path

**For existing users:**

1. Switch to the new canonical repository:
   ```bash
   git clone https://github.com/BjeSystems/agentmd-skill.git
   ```

2. Install the new skill:
   ```bash
   mkdir -p ~/.cursor/skills/agentmd
   cp -r agentmd-skill/skill/* ~/.cursor/skills/agentmd/
   ```

3. Use the new commands in any project:
   ```bash
   cd /path/to/your-project
   /AgentMD      # Bootstrap AGENTS.md
   /AgentCheck   # Auto-generate project-specific rules
   ```

---

## What Changed

| Before (this repo) | After (agentmd-skill) |
|-------------------|----------------------|
| Static template | Dynamic bootstrap + auto-update |
| Manual copy | `/AgentMD` command |
| Manual customization | `/AgentCheck` auto-detection |
| 16 sections | Same 17 sections + auto-generated project rules |

---

## Historical Reference

This repository contains:

- Original AGENTS.md template (v2.0)
- Behavioral philosophy (now in agentmd-skill/docs/behavior-foundation.md)
- Foundation for the canonical system

---

## Archive Notice

This repository is ready for archival.

**To archive (manual step):**
1. Go to: GitHub → Settings → Archive Repository
2. This will make the repository read-only
3. All links will redirect to the canonical repo

**No code deletion will occur.**

---

## License

MIT — See LICENSE file

Historical contributions preserved.
