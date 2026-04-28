# AWS Study Hub

Practice exams and study materials for AWS certification prep. Static HTML — no build, no backend.

## Features

- Timed practice exams with AWS-style scaled scoring (100–1000, 700 to pass)
- Domain-weighted breakdowns for CLF-C02
- Flag questions, strikethrough options, keyboard shortcuts
- Immediate feedback mode or end-of-exam review
- Markdown study guides with clean formatting and auto-generated TOC
- Built-in library of quizzes + upload your own

## Run locally

Browsers block `fetch()` on `file://`, so serve the folder:

```bash
python3 -m http.server
```

Then open http://localhost:8000

## Deploy

Drop the folder on any static host — GitHub Pages, Netlify, Vercel, Cloudflare Pages, S3 + CloudFront. All files are static.

## Add a new quiz

1. Write a `.md` file following the format in `QUESTION_FORMAT.md` (or copy the prompt from the home page into any LLM)
2. Drop it in `quizzes/`
3. Add one line to the `QUIZ_LIBRARY` array in `index.html`:

```js
{ name: 'Your Quiz Name', path: 'quizzes/your-file.md' }
```

Study guides work the same way via `REVIEW_LIBRARY` for files in `learning/`.

## Content covered

- AWS Cloud Practitioner (CLF-C02) — 7 full-length practice exams
- AWS ML/AI Services — quiz + study guide
- Rapid-fire cheatsheet for exam-day review
- Deep-dive notes on IAM, pricing, shared responsibility, Well-Architected, and more

## Structure

```
index.html              Main app (quiz + review)
quiz.html               Standalone quiz-only page
quizzes/                Question banks (.md)
learning/               Study guides (.md)
QUESTION_FORMAT.md      Format spec for new quizzes
```
