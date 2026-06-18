# How I Use These Skills

A practical guide to how I actually invoke and combine these skills day-to-day with Claude Code and Codex.

---

## The basics

Skills live in `~/.claude/skills/` and appear as slash commands in Claude Code once installed.

Type `/` in the Claude Code prompt to see available skills. Each skill's `name:` frontmatter value becomes the command name.

```
/clean-code-guard      → runs the code review guard on the current diff
/tdd                   → enters test-driven development mode
/diagnosing-bugs       → starts the bug diagnosis loop
/handoff               → compacts the conversation for the next agent
```

---

## My typical workflows

### Before shipping any code

After an implementation pass, I run `/clean-code-guard` on the diff. It checks for the 23 imperatives — names, function size, SOLID, DRY/KISS/YAGNI, and AI-specific failure modes. I do not skip this step.

If the diff includes tests, I run `/test-guard` alongside it. The two skills are designed to work in tandem.

If the diff includes documentation changes, `/docs-guard` verifies every referenced symbol, sample, and claim against the source.

### When a bug is hard

`/diagnosing-bugs` — always. The key insight: build a tight feedback loop before forming any hypothesis. Skipping this step is how you spend two hours staring at the wrong place.

### When designing a module

`/codebase-design` gives me the vocabulary (module, interface, depth, seam, adapter, leverage, locality). I use this before writing any code when the design question is non-trivial.

### When I want to sharpen a design through interrogation

`/grill-with-docs` runs a relentless interview using `/domain-modeling` underneath. Good for catching assumptions I haven't examined.

### When delegating to Codex

`/codex-delegate` — write the brief, dispatch via `relay.mjs`, review the diff, commit myself. I never trust Codex's self-report; I re-run the gates myself every time.

### When switching sessions

`/handoff` compacts the conversation into a document saved to the OS temp directory. The next agent reads it and picks up without losing context.

---

## Combining skills

Some skills explicitly pair with others:

| Pair | Why |
|------|-----|
| `/clean-code-guard` + `/test-guard` | Code review + test review in one pass |
| `/codebase-design` + `/tdd` | Design the interface first, then drive it with tests |
| `/diagnosing-bugs` → `/tdd` | Diagnosis produces the regression test; TDD locks it in |
| `/codex-delegate` + `/clean-code-guard` | Codex writes, clean-code-guard reviews before I land it |
| `/grill-with-docs` → `/to-prd` | Interview sharpens the design; PRD captures the output |
| `/to-prd` → `/to-issues` | PRD becomes vertical-slice issues on the tracker |

---

## Invocation tips

- Skills can receive arguments: `/handoff What will the next session be used for?`
- Some skills have `disable-model-invocation: true` — they are pure instruction sets, not interactive agents
- If a skill references another skill (e.g. `grill-with-docs` calls `/domain-modeling`), both need to be installed
- Skills are reloaded on each invocation — edits to SKILL.md take effect immediately
