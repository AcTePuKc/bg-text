# bg-text

**Languages:** English | [Български](README.bg.md)

Bulgarian text quality skill for AI assistants and editor workflows.

`bg-text` helps with:
- Bulgarian typography
- clear writing
- editorial review
- UX writing
- business communication
- localization and Bulgarian-specific language issues

The project is now a standalone Bulgarian reference.
It may acknowledge inspiration from similar text-quality skills, but its rules, structure, and formulations are maintained here for Bulgarian.

Maintained by `Shteryan Nikolaev` (`AcTePuKc`).

## What it contains

- `skills/bg-text/SKILL.md` — main skill entry
- `.agents/skills/bg-text/SKILL.md` — repo-scoped adapter for tools that scan `.agents/skills`
- `.claude/skills/bg-text/SKILL.md` — repo-scoped Claude adapter
- `.cursor/skills/bg-text/SKILL.md` — repo-scoped Cursor adapter
- `.gemini/skills/bg-text/SKILL.md` — repo-scoped Gemini adapter
- `skills/bg-text/references/` — domain references
- `skills/bg-text/agents/` — agent-specific guidance
- `.agents/` — reserved root-level space for local or future agent integration files

## Reliability model

`bg-text` distinguishes between:
- `A. Твърда норма`
- `B. Редакторска практика`
- `C. UX/локализационна евристика`
- `D. Проектно решение`
- `E. За проверка`

This matters because not every useful writing rule is a normative language rule.

## Main reference areas

- `typography.md`
- `editorial-punctuation.md`
- `editorial-grammar.md`
- `clear-writing.md`
- `ux-writing.md`
- `business-writing.md`
- `anti-patterns.md`
- `scoring.md`
- `sources.md`
- `addenda.md`

## Sources

For normative Bulgarian language questions, the project relies primarily on:
- Institute for Bulgarian Language at BAS
- BERON
- Language consultation resources of the Institute

See [skills/bg-text/references/sources.md](skills/bg-text/references/sources.md).

This repository is focused on Bulgarian.

## Releases

The repository is primarily designed to be used directly from GitHub, but tagged releases can also provide a downloadable archive.

## Compatibility

This repository currently maintains public packaging or integration surfaces for:
- Codex — maintained against current OpenAI skill and plugin docs
- Claude Code — maintained against current Claude skills and plugin docs
- Cursor — maintained against current Cursor skills and plugin docs
- Gemini CLI — maintained against current Gemini CLI extension and agent skills docs
- OpenClaw — maintained against current OpenClaw native plugin and skills docs
- Notion — maintained as a manual Notion AI skill and Notion MCP usage path

Current release stance:
- documentation-aligned
- structurally maintained
- not all surfaces manually verified end-to-end on real installs

Canonical source of truth:
- `skills/bg-text/SKILL.md` is the maintained canonical skill body
- repo-level adapter skills exist only to make auto-discovery more reliable across agents with different expected skill locations

Notes:
- Gemini support here refers to Gemini CLI extension packaging, not Gemini Apps Gems or a Gemini API-hosted custom skill format
- some surfaces are docs-aligned but still awaiting manual end-to-end verification

If you try `bg-text` in one of these environments and it works or fails in a meaningful way, please report it in a GitHub issue. Short reports are enough:
- platform and version
- install method
- what worked
- what failed or looked inconsistent

This helps separate documentation compliance from real-world compatibility.
