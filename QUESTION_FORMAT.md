# Question Bank Format Guide

You are generating questions for a practice quiz app. Write all questions into `questions.md` following this exact format.

## Rules

- Each question starts with `## Q<number>.` followed by the question text on the same line.
- Answer choices are markdown checkboxes: `- [ ]` for wrong, `- [x]` for correct.
- Each choice is prefixed with a letter (A–E) and parenthesis: `A)`, `B)`, `C)`, `D)`, or `E)`.
- For multi-select questions, mark multiple choices with `[x]`.
- After the last choice, add `### Explanation` on its own line, followed by the explanation text.
- Separate each question block with `---` on its own line (must have a blank line or newline before and after).
- Number questions sequentially starting from 1.
- Do not add blank lines between choices.
- Choice letters must be A–E only. The parser does not support F or beyond.

## Template

```
## Q1. Your question text here?
- [ ] A) First option
- [x] B) Correct option
- [ ] C) Third option
- [ ] D) Fourth option
### Explanation
Why B is correct. Explain why the other options are wrong.
---
```

## Multi-Select Template

```
## Q2. Select TWO correct answers.
- [x] A) Correct option one
- [x] B) Correct option two
- [ ] C) Wrong option
- [ ] D) Wrong option
- [ ] E) Wrong option
### Explanation
A and B are correct because... C, D, and E are wrong because...
---
```

## Parser Details

- The file is split into blocks on `\n---\n` (the `---` must be on its own line with newlines on both sides).
- Each block is scanned for `## Q<number>. <question text>` to identify a question.
- Choices are matched by `- [ ]` or `- [x]` followed by a letter `A)` through `E)`.
- The explanation is captured from `### Explanation` until the next `---` or end of file.
- Blocks that don't match `## Q<number>.` are silently skipped (safe for comment headers).
- The file can start with comment lines (`#` prefix) — the parser ignores them.
- Append new questions to the end of `questions.md`, continuing the numbering from the last question.
