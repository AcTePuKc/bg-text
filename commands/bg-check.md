---
name: bg-check
description: Run a comprehensive Bulgarian text quality check on provided text or recent output
allowed-tools: Read, Grep, Glob
context: fork
---

# Bulgarian Text Quality Check

Review the text provided in $ARGUMENTS (or the most recent Bulgarian text output if no arguments) using the bg-text skill.

## Check order

Reference files: `references/<filename>`

1. **Типография** — read `references/typography.md`, then apply:
   - Quotes: „“ primary, ‚‘ nested
   - Dashes: - (hyphen) in normal text and compounds, – (en dash) only for ranges and special cases
   - Spaces: correct spacing around punctuation, units, percentages, abbreviations, and Bulgarian typographic conventions
   - Ellipsis, abbreviations, special characters, Bulgarian-specific characters like ѝ

2. **Анти-шаблони** — read `references/anti-patterns.md`, then scan for:
   - Bureaucratic language and nominalization
   - Literal translations from English or Russian
   - Passive voice overuse
   - Sentence bloat
   - Tautology and pleonasm
   - Unnatural Bulgarian phrasing

3. **Качество на писане** — read `references/clear-writing.md`, then apply:
   - Filler words and weak constructions
   - Specificity and factual clarity
   - Structure and readability
   - Natural Bulgarian flow and word order

4. **Специфични правила по домейн** — load if text type is identifiable:
   - UI/interface text → `references/ux-writing.md`
   - Email/business → `references/business-writing.md`
   - Needs grammar review → `references/editorial-punctuation.md` + `references/editorial-grammar.md`

## Output format

Return:

1. Corrected text
2. List of changes grouped by category (typography / style / grammar / domain)
3. Severity per change: critical / high / medium / low
