# Changelog — BioLearn AI

This file records the development and release history of the BioLearn AI educational prototype. It distinguishes implemented features, observed manual testing, and checks that remain outstanding.

## [V2.0](https://github.com/jesseicaj2/BioLearn-ai/releases/tag/V2.0) — November 1, 2026

**Status:** Published Week 9 midterm prototype; merged into `main` and deployed through GitHub Pages.

### Added

- Eight-stage clickable EGFR/Ras/MAPK pathway explorer, including component explanations and a conceptual MEK-inhibition reasoning check.
- Per-lesson quiz statistics: answered count, correct count, and percentage accuracy.
- Twelve distinct interactive terminology flashcards with reveal/hide behavior and a hide-all control.
- Six navigation sections: Learn, Quiz, Pathway, Flashcards, Progress, and Sources.
- Responsive layout and accessibility-oriented enhancements, including visible focus states and a skip link.
- Scientific reading suggestions, limitations, and an explicit statement that the app is AI-assisted rather than powered by a live AI model.

### Retained from Version 1

- Three lessons: Cell Signaling Fundamentals, RTKs, and Ras/MAPK Signaling.
- Nine multiple-choice quiz questions with immediate feedback.
- One recorded answer per question until the quiz is reset.
- Overall score, accuracy, progress indicator, review recommendation, and reset control.
- Standalone HTML operation without external libraries, server, or API key.

### Development and release milestones

- Developed Version 2 on the `develop-v2` branch, preserving the original prototype under the `V1.0` tag.
- Merged Version 2 into `main` through [pull request #1](https://github.com/jesseicaj2/BioLearn-ai/pull/1).
- Configured GitHub Pages to deploy from `main` at the repository root.
- GitHub Pages build and deployment completed successfully; the live application was subsequently checked by the project author.
- Published the `V2.0` release for the Week 9 midterm.

### Observed manual testing

- Android tablet screenshots and user confirmations support navigation among the six sections and selection of the three lessons.
- Quiz answer selection showed immediate correct/incorrect feedback; the progress view displayed 2 answered, 1 correct, and 50% accuracy for the observed partial attempt.
- The pathway explorer displayed component information, and the MEK-inhibition reasoning check showed appropriate feedback for the observed correct choice.
- Twelve distinct flashcards were displayed; card flipping and the **Hide all cards** control were confirmed to work.
- The quiz reset control was confirmed to restore a fresh attempt.
- The author confirmed the application worked smoothly from the live GitHub Pages website.

These are observed **manual** checks, not comprehensive automated or cross-browser verification. See [TESTING_CHECKLIST.md](TESTING_CHECKLIST.md).

### Known limitations and outstanding verification

- Quiz and flashcard states are not saved between page reloads.
- The pathway explorer is a simplified conceptual representation, not a quantitative simulation.
- Reference hyperlinks require internet access; core interactions are designed to work offline, but a deliberate no-network test remains to be documented.
- Exhaustive testing of every pathway stage, both reasoning choices, all scoring edge cases, keyboard navigation, and multiple browsers remains outstanding.
- Scientific explanations and references still require independent verification against course materials and authoritative sources.

## [V1.0](https://github.com/jesseicaj2/BioLearn-ai/releases/tag/V1.0) — November 1, 2026

**Status:** Preserved initial prototype release, anchored to the original Version 1 commit.

### Implemented

- Three educational lessons with descriptions, mechanisms, key terms, and examples.
- Nine-question quiz with immediate correct/incorrect feedback.
- Learning progress dashboard with total answered, correct, accuracy, review prompt, and reset.
- Responsive single-file HTML prototype.

### Observed manual testing

- All nine questions were answered in a tablet browser.
- Dashboard displayed eight correct out of nine and 89% accuracy.
- Review suggestion identified Cell Signaling Fundamentals.
- Reset returned the dashboard to zero and restored the unanswered quiz state.

These observations are based on screenshots shared during development, not an automated test suite.

## Version control approach

- `main` contains the current V2.0 application following the merge of pull request #1.
- The `V1.0` tag preserves the original Version 1 snapshot; the `V2.0` tag preserves the Week 9 release snapshot.
- `develop-v2` was the development branch for Version 2. It has been merged and need not remain the active deployment branch.
- Documentation commits made after V2.0 publication update `main` but do **not** retroactively modify the published tag or its source archive.
