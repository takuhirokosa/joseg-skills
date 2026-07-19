# Article Structure

Use this structure as a decision guide, not a rigid template. Omit a section only when the source material provides no honest content for it.

## Recommended Structure

1. **Benefit-led title**
   - Name the reader or problem first.
   - State the useful change.
   - Put the tool or technique after the benefit when possible.
2. **Opening hook**
   - Describe the frustrating starting state.
   - Show the practical cost of leaving it unresolved.
   - Preview the result without exaggeration.
3. **Context and constraints**
   - Explain what the author was trying to achieve.
   - Include only constraints that affected the solution.
4. **What changed**
   - Summarize the key decision or method before listing steps.
5. **Reproducible process**
   - Present the smallest sequence a reader can follow.
   - Explain why each important step exists.
   - Replace private paths and identifiers with placeholders.
6. **What failed and why**
   - Include failed approaches only when they prevent a likely reader mistake.
7. **Observed result**
   - Use concrete evidence from the logs.
   - Separate measured results from expectations.
8. **Reusable lessons**
   - Convert project-specific details into general rules.
9. **Checklist or next action**
   - Give the reader a short way to apply the method immediately.

## Transformation Rules

Convert raw log patterns as follows:

| Raw material | Article form |
| --- | --- |
| Repeated command attempts | One concise failure pattern and its cause |
| Long tool output | Relevant evidence or measurement only |
| Internal file path | Descriptive placeholder such as `<project>/config.json` |
| Personal decision note | Reader-facing tradeoff and decision criterion |
| Successful execution message | Result only after matching it to observable evidence |
| Unresolved error | Explicit limitation or next investigation step |
| Timeline chatter | Omit unless sequence explains causality |

## Title Patterns

- `<Reader>が<problem>を避けて<result>を得る方法`
- `<Pain>を<time or effort reduction>に変えた<method>`
- `<Tool>で失敗した原因と、再発を防いだ<decision>`

Avoid titles that merely say an event happened, such as "I tried X" or "Development diary for today," unless the user explicitly wants a diary.

## Verification Note

After the draft, report only material uncertainty:

```markdown
## Verification note

- Verified: <claim and supporting source>
- Inferred: <claim and why it is an inference>
- Unresolved: <missing evidence or test>
```

Omit empty categories. If the user asks for article text only, keep the note separate from the copy-ready article.
