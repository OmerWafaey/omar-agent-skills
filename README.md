# Omar's Agent Skills

A personal collection of workflow skills for Claude Code and Codex — small, opinionated guides that make AI agents work the way I actually work.

Some I wrote myself. Some are adapted from public examples or other people's ideas. When something isn't originally mine, I say so in [docs/ATTRIBUTION.md](docs/ATTRIBUTION.md).

---

## Skills

| Skill | What it does |
|-------|--------------|
| [clean-code-guard](skills/clean-code-guard/SKILL.md) | Review code before it ships — SOLID, DRY, KISS, YAGNI, and AI-specific failure modes |
| [codebase-design](skills/codebase-design/SKILL.md) | Design deep modules with a shared vocabulary |
| [codex-delegate](skills/codex-delegate/SKILL.md) | Delegate implementation to OpenAI Codex CLI, then review and land the diff yourself |
| [diagnosing-bugs](skills/diagnosing-bugs/SKILL.md) | Systematic diagnosis loop for hard bugs and performance regressions |
| [docs-guard](skills/docs-guard/SKILL.md) | Review documentation accuracy before publishing |
| [domain-modeling](skills/domain-modeling/SKILL.md) | Build and sharpen a project's ubiquitous language |
| [git-guardrails-claude-code](skills/git-guardrails-claude-code/SKILL.md) | Block dangerous git commands via Claude Code hooks |
| [grill-with-docs](skills/grill-with-docs/SKILL.md) | Relentless design interview that produces ADRs as it goes |
| [handoff](skills/handoff/SKILL.md) | Compact a conversation into a handoff doc for the next agent |
| [setup-pre-commit](skills/setup-pre-commit/SKILL.md) | Set up Husky + lint-staged + Prettier pre-commit hooks |
| [tdd](skills/tdd/SKILL.md) | Test-driven development, vertical slices only |
| [teach](skills/teach/SKILL.md) | Stateful teaching workspace with missions, lessons, and learning records |
| [test-guard](skills/test-guard/SKILL.md) | Review test code against universal testing rules |
| [to-issues](skills/to-issues/SKILL.md) | Break a plan into independently-grabbable vertical-slice issues |
| [to-prd](skills/to-prd/SKILL.md) | Turn a conversation into a PRD on the issue tracker |

---

## Installation

### Copy a single skill

```powershell
Copy-Item "C:\path\to\agent-skills\skills\clean-code-guard" `
  "$env:USERPROFILE\.claude\skills\clean-code-guard" -Recurse
```

Repeat for each skill you want.

### Junction the whole directory (Windows)

Keeps your local copy in sync with the repo automatically:

```powershell
cmd /c mklink /J "$env:USERPROFILE\.claude\skills" "C:\path\to\agent-skills\skills"
```

> **Heads up:** this replaces everything in `~/.claude/skills`. Only do it if you manage all your skills from this repo.

### Verify

Type `/` in Claude Code — installed skills appear as slash commands using their `name:` frontmatter value.

---

## Attribution

See [docs/ATTRIBUTION.md](docs/ATTRIBUTION.md) for the origin of each skill.

---

## A note on these skills

These are personal tools, not universal best practices. They're opinionated, evolving, and shaped by the kind of work I keep coming back to. Take what's useful, ignore the rest.
