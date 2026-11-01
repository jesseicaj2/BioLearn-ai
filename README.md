# BioLearn AI

**An AI-assisted interactive learning platform for cellular signaling.**

BioLearn AI is a browser-based educational prototype designed to help biomedical science students learn fundamental cell signaling mechanisms through short lessons, a knowledge-check quiz, and interactive study tools. It was developed for the **Introduction to Artificial Intelligence — Week 9 midterm**.

**Current release: V2.0 — Week 9 Midterm Prototype (November 1, 2026).**

**[Launch BioLearn AI](https://jesseicaj2.github.io/BioLearn-ai/)** · [V2.0 release](https://github.com/jesseicaj2/BioLearn-ai/releases/tag/V2.0) · [V1.0 release](https://github.com/jesseicaj2/BioLearn-ai/releases/tag/V1.0)

> **AI transparency:** AI tools assisted in planning and writing the application. BioLearn AI does **not** run a live AI model, generate real-time AI explanations, or send student data to an AI service. Its quizzes, feedback, and recommendations use predefined content and JavaScript rules.

## Versions and branches

| Reference | Purpose | Status |
| --- | --- | --- |
| [`main`](../../tree/main) | Current application and documentation | **V2.0 merged and deployed** |
| [`V1.0`](../../releases/tag/V1.0) | Original working prototype snapshot | **Preserved release** |
| [`V2.0`](../../releases/tag/V2.0) | Week 9 midterm prototype snapshot | **Published release** |
| [`develop-v2`](../../tree/develop-v2) | Development branch used to implement and review V2.0 | **Merged into `main` via pull request #1**; branch retention is optional |

Version 1 is preserved by its release tag and associated commit, **not** by keeping `main` at Version 1. Version 2 was developed separately and merged after manual testing. The release tags are fixed snapshots; later documentation commits to `main` do not automatically change the contents of the V2.0 release archive.

## Learning content

The application introduces three interconnected topics:

1. **Cell Signaling Fundamentals:** ligands, receptors, signal reception, transduction, and cellular responses.
2. **Receptor Tyrosine Kinases (RTKs):** receptor activation, tyrosine phosphorylation, and recruitment of signaling proteins.
3. **Ras/MAPK Signaling:** the simplified EGFR → Grb2/SOS → Ras-GTP → Raf → MEK → ERK signaling cascade.

The content is introductory and uses simplified canonical examples; it does not cover all receptor types, feedback loops, or context-dependent signaling outcomes.

## Features

### Version 1 — initial prototype (retained in V2.0)

- Three selectable lessons with mechanisms, terminology, and biological examples.
- Nine multiple-choice questions (three per lesson).
- Immediate answer feedback and one recorded answer per question until reset.
- Overall answered count, correct count, accuracy percentage, progress bar, and review suggestion.
- Quiz reset functionality.

### Version 2 — current release

All Version 1 features are retained, plus:

- **Interactive pathway explorer:** eight selectable stages in a simplified EGFR–Ras/MAPK pathway and a conceptual MEK-inhibition reasoning question.
- **Lesson-specific analytics:** answered questions, correct answers, and accuracy for each lesson.
- **Terminology flashcards:** 12 distinct revealable cards with a hide-all control.
- **Improved navigation and layout:** Learn, Quiz, Pathway, Flashcards, Progress, and Sources sections, with a responsive layout and accessibility-oriented elements.
- **Sources and content notes:** suggested scientific reading and explicit limitations of the simplified teaching model.

## How to run

**Online:** Open the [live GitHub Pages application](https://jesseicaj2.github.io/BioLearn-ai/).

**Locally:** No installation, account, server, build tools, or API key is required.

1. Download the current `index.html` from [`main`](../../tree/main), or download the V2.0 release source archive and extract it.
2. Open `index.html` in a modern browser.
3. Use the navigation buttons to explore lessons and study activities.

The application is a self-contained HTML file designed to operate offline for its core interactions. External scientific reference links require internet access. A dedicated airplane-mode/offline test remains on the checklist; successful online deployment alone is not proof of that test.

To inspect Version 1, use the `V1.0` release rather than the current `main` branch.

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
4. Preserve the initial prototype under the `V1.0` GitHub release.
5. Create `develop-v2` and implement the enhanced learning tools.
6. Conduct manual Version 2 functionality testing on an Android tablet and document the observations.
7. Merge `develop-v2` into `main` through [pull request #1](../../pull/1).
8. Deploy the application through GitHub Pages and confirm the live website functions.
9. Publish the `V2.0` GitHub release as the Week 9 midterm prototype.

Human review remains necessary: AI-assisted code and explanations should be inspected and tested rather than assumed correct.

## Testing status

- **Version 1:** screenshot-supported manual checks of the nine-question quiz, scoring, review prompt, and reset were successful.
- **Version 2:** manual testing on an Android tablet confirmed lesson selection, quiz feedback, the pathway reasoning interaction, flashcard operation and hide-all reset, lesson-specific progress display, sources display, and quiz reset. The user also confirmed successful operation from the live GitHub Pages website.
- **Not fully verified:** exhaustive pathway-stage coverage, every quiz/scoring edge case, offline testing with internet deliberately disabled, cross-browser and keyboard-accessibility coverage, and independent line-by-line scientific content verification.

See [TESTING_CHECKLIST.md](TESTING_CHECKLIST.md) for itemized evidence, confirmed observations, and outstanding checks. These are **manual tests**, not an automated test suite.

## Scientific reading and limitations

Suggested references (links require internet):

- [OpenStax Biology 2e](https://openstax.org/details/books/biology-2e) — cell communication and signal transduction.
- [NCBI Bookshelf](https://www.ncbi.nlm.nih.gov/books/) — molecular and cell biology reference material.
- [Cell Signaling Technology: Signaling Pathways](https://www.cellsignal.com/learn-and-support/pathways) — pathway-oriented educational material.

These are **suggested readings**, not a claim that every sentence has already been verified against them. RTK activation, Ras signaling, ERK output, and pathway regulation vary by biological context. The pathway explorer is a conceptual teaching diagram, **not** a computational simulation or clinical decision tool.

## Repository documents

- [CHANGELOG.md](CHANGELOG.md) — version history, release milestones, and feature changes.
- [TESTING_CHECKLIST.md](TESTING_CHECKLIST.md) — manual acceptance tests, observed evidence, and remaining checks.

## Academic context

Created for an Introduction to Artificial Intelligence midterm to demonstrate AI-assisted software creation, iterative improvement, human judgment, and Git-based version control. The project is an educational prototype, not a commercial product.
