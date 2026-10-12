# From Spring Boot to AI

An interactive study book for Java backend developers who want to build AI features.
It runs in the browser as a single page: no build step, no framework, no backend.

**Live site:** https://pycharm0422.github.io/spring-boot-to-ai/

## What's inside

| Phase | Chapters |
| --- | --- |
| 1. Foundations | How LLMs work · Prompting · Calling an LLM API · Working with coding agents |
| 2. LLM features in Spring Boot | Spring AI basics · Tool calling |
| 3. Your data: RAG, agents and MCP | Embeddings and vector search · RAG · Agents · MCP |
| 4. Production-grade AI | Evals · Observability and cost · Security · Deployment and cloud platforms |

Every chapter has plain-language explanations, Java and Spring AI examples, "check yourself" questions,
a key-terms list and a 6-question chapter test. Each phase ends with an exam: multiple choice,
written answers with model answers, and a build project with a checklist.

Interactive labs: token splitter, temperature (softmax) lab, API cost calculator,
similarity search lab and chunking lab.

## How it's built

- One HTML file: [`site/index.html`](site/index.html)
- Plain HTML, CSS and JavaScript
- Content (chapters, quizzes, tests) lives in JavaScript objects; small render functions build each view
- Hash routing (`#ch5`, `#exam2`) for navigation
- Progress and drafts saved in the browser's `localStorage`
- Light and dark themes; works on phones

## Run locally

Open `site/index.html` in a browser, or serve the folder:

```bash
cd site
python3 -m http.server 8000
# then open http://localhost:8000
```

## Deployment

Every push to `main` deploys `site/` to GitHub Pages through
[`.github/workflows/deploy.yml`](.github/workflows/deploy.yml).
