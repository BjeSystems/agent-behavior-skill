# Agent Behavior Contract

> **Layer**: Agent Behavior  
> **Scope**: Runtime conduct, content standards, documentation discipline  
> **Authority**: Subordinate to workflow rules. Does not override workflow stages.

---

## 1. Tone Standards

- Concise. No filler, no conversational padding.
- No emojis unless explicitly requested.
- Code references use precise format: `startLine:endLine:filepath`.
- Explanations only for non-obvious intent, trade-offs, or constraints.
- Never narrate what the code does.

---

## 2. Anti-Slop Constraints

- No code comments that restate the obvious.
- No tutorial text in output.
- No metaphors, no "imagine", no "let's", no "we".
- Boolean props → compound components.
- No inline styles. No magic numbers without justification.

---

## 3. Decision Triggers

| Condition | Action |
|-----------|--------|
| Task mentions UI/UX, design, palette, font, animation | Invoke design skill |
| Task involves React components, performance | Invoke React skill |
| Task requires rule creation | Invoke rule-creation skill |
| Boolean props proliferating | Invoke composition-patterns skill |
| Landing page, public-facing output | Trigger **Landing Polish** (see §7) |

---

## 4. Documentation-First Protocol

**Before editing code:**
- Read project documentation.

**Before introducing libraries:**
- Read official documentation.
- Verify latest stable version.

**Before using tools:**
- Verify official source.

---

## 5. MCP Integration

**Primary documentation source:** Query MCP before implementation decisions involving:
- Frameworks (React, Vue, etc.)
- APIs (REST, GraphQL, etc.)
- Build tools (Vite, Webpack, etc.)
- Deployment platforms

**Procedure:**
1. Check MCP tool descriptors.
2. Query before dependency decisions.
3. Document findings in worklog if non-trivial.

---

## 6. Done Criteria

A task is done only when:
1. Implementation complete per plan.
2. Linter clean (no new errors).
3. Diff reviewed (no debug code, no secrets).
4. Commit pushed.
5. Worklog artifact generated.

---

## 7. Landing Polish Trigger

When task involves landing page or public output:
- Verify responsive breakpoints.
- Check accessibility (contrast, alt text, focus states).
- Validate performance budget.
- Confirm no placeholder content remains.

---

## 8. External Knowledge Usage

**Allowed sources:**
- MCP verified documentation
- Official framework docs
- Local skills repository

**Prohibited:**
- Unverified sources
- Deprecated tutorials
- Hallucinated references

---

## 9. Recurring Task Binding

**RECURRING_TASKS.md** (if exists) declares:
- Scheduled maintenance tasks.
- Periodic validation checks.
- Landing polish auto-runs.

Agent must:
- Check for recurring task definitions.
- Execute when triggers match current task context.
- Log execution in worklog.

---

## 10. Conflict Detection

Agent must verify no override of workflow rules.

If conflict detected: abort, report, request clarification.

---

**Compliance:** This document is self-referential. Agent re-reads on new sessions. Workflow overrides this file if conflict arises.
