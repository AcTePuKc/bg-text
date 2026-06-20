---
name: bg-score
description: Score Bulgarian text quality on a 0.0-10.0 scale across 5 dimensions
allowed-tools: Read, Grep, Glob
context: fork
---

# Bulgarian Text Quality Score

Score the text provided in $ARGUMENTS (or the most recent Bulgarian text output if no arguments) using the bg-text scoring rubric.

## Procedure

Reference files: `references/<filename>`

1. **Load rubric** - read `references/scoring.md` for the full rubric with anchors.

2. **Determine domain** - identify whether the text is UI/interface, business email, article, or general:
   - UI text → also load `references/ux-writing.md` for the reader-usefulness dimension
   - Business email → also load `references/business-writing.md` for the reader-usefulness dimension
   - General → use `references/clear-writing.md` only

3. **Evaluate each dimension separately** - score in this order:
   - **Т - Типография** (weight 0.15): quotes, hyphens, spacing, punctuation, Bulgarian typographic conventions per `references/typography.md`
   - **Я - Яснота** (weight 0.25): bureaucratic language, literal translations, clichés, passive voice, unnatural phrasing per `references/clear-writing.md` + `references/anti-patterns.md`
   - **Г - Грамотност** (weight 0.20): spelling, punctuation, agreement, repetition per `references/editorial-grammar.md` + `references/editorial-punctuation.md`
   - **С - Структура** (weight 0.20): logical flow, paragraphing, transitions, headings, readability per `references/clear-writing.md` + `references/addenda.md`
   - **Ч - Полезност за читателя** (weight 0.20): clarity, factual precision, actionability, contextual usefulness per domain rules

4. **For each dimension** - assign a score (0.0-10.0) using the rubric anchors in scoring.md. List 1-3 specific issues, quoting the problematic text fragment.

5. **Apply non-compensatory rules:**
   - Any dimension < 3.0 → cap total at 5.0
   - Typography < 4.0 → cap total at 7.0
   - Grammar < 4.0 → cap total at 7.0
   - Use the most restrictive cap when multiple conditions trigger

6. **Compute composite score:**

```text

S = round₁(T × 0.15 + Я × 0.25 + Г × 0.20 + С × 0.20 + Ч × 0.20)

```

1. **Short text warning** - if text is under 50 words, prepend a reliability caveat.

## Score labels

| Score | Label |
| --- | --- |
| 9.0-10.0 | Еталонен |
| 7.0-8.9 | Добър |
| 5.0-6.9 | Среден |
| 3.0-4.9 | Слаб |
| 0.0-2.9 | Критичен |

## Output format

```

## Оценка: X.X / 10 - [label from table above]

| Измерение             | Балл | Замечания                                     |
| --------------------- | ---- | --------------------------------------------- |
| Типография            | X.X  | [1-3 specific issues with „quoted fragments“] |
| Яснота                | X.X  | ...                                           |
| Грамотност            | X.X  | ...                                           |
| Структура             | X.X  | ...                                           |
| Полезност за читателя | X.X  | ...                                           |

**Формула:** T×0.15 + Я×0.25 + Г×0.20 + С×0.20 + Ч×0.20 = X.X
[If non-compensatory cap triggered: „Ограничение: [dimension] below threshold → final score ≤ X.X“]

### Какво оценката не измерва

Фактическа точност, уместност на тона за аудиторията, креативност, конверсия, съответствие със заданието.

```

If a dimension has no issues, write „Няма забележки“ in the remarks column.
