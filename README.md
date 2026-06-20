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
