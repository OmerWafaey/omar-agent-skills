# Attribution

This file records what I know (and don't know) about the origin of each skill in this repo.

I have not invented authors or sources. Where origin is unclear from the files themselves, I say so honestly.

---

## How I determined origin

For each skill I checked:
- The `SKILL.md` frontmatter (`license:`, `author:`, source URLs)
- Whether the folder was a filesystem junction pointing elsewhere (`~/.agents/skills/`)
- Internal references to named projects or people (e.g. "setup-matt-pocock-skills")
- The writing style and structure

---

## Skill origins

### clean-code-guard

- **Installed via:** junction from `~/.agents/skills/clean-code-guard`
- **License in file:** none declared
- **Origin:** Unknown / local skill folder. Arrived via the `.agents/skills` mechanism; not written by me. Style is consistent with the claude-plugins-official / superpowers family but this is not confirmed.
- **Status:** Copied (not adapted). Used as-is.

---

### codebase-design

- **Installed via:** normal folder in `~/.claude/skills`
- **License in file:** none declared
- **Origin:** Unknown / local skill folder. Covers John Ousterhout's "deep modules" vocabulary and Michael Feathers' "seam" concept. Not written by me.
- **Status:** Copied. Used as-is.

---

### codex-delegate

- **Installed via:** normal folder in `~/.claude/skills`
- **License in file:** `MIT` (declared in frontmatter)
- **Origin:** Unknown author. MIT licensed. Bundles a `scripts/relay.mjs` helper (Node.js, no external deps) for dispatching tasks to the OpenAI Codex CLI.
- **Status:** Copied. MIT license applies. `scripts/relay.mjs` makes no network calls of its own.

---

### diagnosing-bugs

- **Installed via:** normal folder in `~/.claude/skills`
- **License in file:** none declared
- **Origin:** Unknown / local skill folder. Not written by me.
- **Status:** Copied. Used as-is.

---

### docs-guard

- **Installed via:** junction from `~/.agents/skills/docs-guard`
- **License in file:** none declared
- **Origin:** Unknown / local skill folder. Arrived via the `.agents/skills` mechanism. Style consistent with the clean-code-guard / test-guard family.
- **Status:** Copied. Used as-is.

---

### domain-modeling

- **Installed via:** normal folder in `~/.claude/skills`
- **License in file:** none declared
- **Origin:** Unknown / local skill folder. References Eric Evans (DDD), Michael Feathers (seams), and Ousterhout (modules). Not written by me.
- **Status:** Copied. Used as-is.

---

### git-guardrails-claude-code

- **Installed via:** normal folder in `~/.claude/skills`
- **License in file:** none declared
- **Origin:** Unknown / local skill folder. Bundles `scripts/block-dangerous-git.sh`. Not written by me.
- **Status:** Copied. Used as-is.

---

### grill-with-docs

- **Installed via:** normal folder in `~/.claude/skills`
- **License in file:** none declared
- **Origin:** Unknown / local skill folder. A thin wrapper that delegates to `/domain-modeling`. Not written by me.
- **Status:** Copied. Used as-is.

---

### handoff

- **Installed via:** normal folder in `~/.claude/skills`
- **License in file:** none declared
- **Origin:** Unknown / local skill folder. Not written by me.
- **Status:** Copied. Used as-is.

---

### setup-pre-commit

- **Installed via:** normal folder in `~/.claude/skills`
- **License in file:** none declared
- **Origin:** Unknown / local skill folder. Covers Husky v9+, lint-staged, Prettier. Not written by me.
- **Status:** Copied. Used as-is.

---

### tdd

- **Installed via:** normal folder in `~/.claude/skills`
- **License in file:** none declared
- **Origin:** Unknown / local skill folder. References Fowler's refactoring definition and the tracer-bullet pattern. Not written by me.
- **Status:** Copied. Used as-is.

---

### teach

- **Installed via:** normal folder in `~/.claude/skills`
- **License in file:** none declared
- **Origin:** Unknown / local skill folder. References spaced repetition, desirable difficulty, and Tufte-style typography. Not written by me.
- **Status:** Copied. Used as-is.

---

### test-guard

- **Installed via:** junction from `~/.agents/skills/test-guard`
- **License in file:** none declared
- **Origin:** Unknown / local skill folder. Arrived via the `.agents/skills` mechanism. Style consistent with the clean-code-guard / docs-guard family.
- **Status:** Copied. Used as-is.

---

### to-issues

- **Installed via:** normal folder in `~/.claude/skills`
- **License in file:** none declared
- **Origin:** Unknown / local skill folder. References `/setup-matt-pocock-skills` for issue tracker vocabulary — possibly from Matt Pocock's skill collection or inspired by it, but this is not confirmed. Not written by me.
- **Status:** Copied. Used as-is.

---

### to-prd

- **Installed via:** normal folder in `~/.claude/skills`
- **License in file:** none declared
- **Origin:** Unknown / local skill folder. Also references `/setup-matt-pocock-skills`. Same note as `to-issues`. Not written by me.
- **Status:** Copied. Used as-is.