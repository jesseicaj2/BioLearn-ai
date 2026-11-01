# BioLearn AI

**An AI-assisted interactive learning platform for cellular signaling.**

BioLearn AI is a browser-based educational prototype designed to help biomedical science students learn fundamental cell signaling mechanisms through short lessons, a knowledge-check quiz, and interactive study tools. It was developed as a project for **Introduction to Artificial Intelligence (Week 9 midterm)**.

> **AI transparency:** AI tools assisted in planning and writing the application. BioLearn AI does **not** run a live AI model, generate real-time AI explanations, or send student data to an AI service. Its quizzes, feedback, and recommendations use predefined content and JavaScript rules.

## Versions and branches

| Branch | Purpose | Status |
| --- | --- | --- |
| [`main`](../../tree/main) | Version 1 baseline: original learning and quiz prototype | Previously tested on a tablet |
| [`develop-v2`](../../tree/develop-v2) | Version 2 development: interactive pathway, flashcards, analytics, interface and source notes | Code committed; full browser testing pending |

The branches are intentionally separate so the original working prototype can be preserved while Version 2 is evaluated. **Version 2 is not yet a verified release.**

## Learning content

The application introduces three interconnected topics:

1. **Cell Signaling Fundamentals:** ligands, receptors, signal reception, transduction, and cellular responses.
2. **Receptor Tyrosine Kinases (RTKs):** receptor activation, tyrosine phosphorylation, and recruitment of signaling proteins.
3. **Ras/MAPK Signaling:** the simplified EGFR → Grb2/SOS → Ras-GTP → Raf → MEK → ERK signaling cascade.

The content is introductory and uses simplified canonical examples; it does not cover all receptor types, feedback loops, or context-dependent signaling outcomes.

## Features

### Version 1 — baseline

- Three selectable lessons with mechanisms, terminology, and biological examples.
- Nine multiple-choice questions (three per lesson).
- Immediate answer feedback and one recorded answer per question until reset.
- Overall answered count, correct count, accuracy percentage, progress bar, and review suggestion.
- Quiz reset.

### Version 2 — development branch

All Version 1 features are retained, plus:

- **Interactive pathway explorer:** eight selectable stages in a simplified EGFR–Ras/MAPK pathway and a conceptual MEK-inhibition question.
- **Lesson-specific analytics:** attempted questions, correct answers, and accuracy for each lesson.
- **Terminology flashcards:** 12 revealable cards with a hide-all control.
- **Improved navigation and layout:** Learn, Quiz, Pathway, Flashcards, Progress, and Sources sections, with responsive layout and accessibility improvements.
- **Sources and content notes:** suggested scientific reading and explicit limitations of the simplified teaching model.

## How to run

No installation, account, server, build tools, or API key is required.

1. Select the branch for the version you want to inspect.
2. Download that branch's **`index.html`** file (or download the repository ZIP and extract it).
3. Open `index.html` in a modern browser.
4. Use the navigation buttons to explore lessons and study activities.

The application is a self-contained HTML file and its core functionality works offline. External reference links require an internet connection.

## How to use Version 2

1. **Learn:** review the three lessons.
2. **Pathway:** select signaling components and read their roles; try the MEK-inhibition reasoning check.
3. **Flashcards:** reveal definitions and hide the cards to practice again.
4. **Quiz:** answer the nine questions and read the feedback.
5. **Progress:** inspect overall and per-lesson performance; reset to start a new attempt.
6. **Sources:** review suggested readings, scientific simplifications, and AI-use disclosure.

**Progress limitation:** quiz answers and flashcard states are stored in page memory only. Reloading the page starts a fresh session. There is no account, backend, database, or persistent learning history.

## Development approach

1. Define the educational problem and select cellular signaling as the subject.
2. Build Version 1 as a single-file browser prototype with AI assistance.
3. Manually test Version 1's lessons, quiz feedback, scoring, and reset on a tablet; screenshots showed 8/9 correct (89%) and a successful reset.
4. Preserve Version 1 on `main`.
5. Create `develop-v2` and commit the enhanced application.
6. Document Version 2 changes and prepare a separate acceptance-testing checklist.

Human review remains necessary: AI-assisted code and explanations should be inspected and tested rather than assumed correct.

## Testing status

- **Version 1:** observed manual tests of the nine-question quiz, scoring, review prompt, and reset were successful in the provided screenshots.
- **Version 2:** functional browser testing and scientific content verification are **pending**. See [TESTING_CHECKLIST.md](TESTING_CHECKLIST.md) for the test plan.

## Scientific reading and limitations

Suggested references (links require internet):

- [OpenStax Biology 2e](https://openstax.org/details/books/biology-2e) — cell communication and signal transduction.
- [NCBI Bookshelf](https://www.ncbi.nlm.nih.gov/books/) — molecular and cell biology reference material.
- [Cell Signaling Technology: Signaling Pathways](https://www.cellsignal.com/learn-and-support/pathways) — pathway-oriented educational material.

These are **suggested readings**, not a claim that every sentence has already been verified against them. RTK activation, Ras signaling, ERK output, and pathway regulation vary by biological context. The pathway explorer is a conceptual teaching diagram, **not** a computational simulation or clinical decision tool.

## Repository documents

- [CHANGELOG.md](CHANGELOG.md) — version history and feature changes.
- [TESTING_CHECKLIST.md](TESTING_CHECKLIST.md) — manual acceptance tests and evidence checklist.

## Academic context

Created for an Introduction to Artificial Intelligence midterm to demonstrate AI-assisted software creation, iterative improvement, human judgment, and Git-based version control. The project is an educational prototype, not a commercial product.
