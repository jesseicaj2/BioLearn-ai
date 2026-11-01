# Changelog — BioLearn AI

This file records the development of the BioLearn AI educational prototype. It distinguishes implemented features from independently verified behavior.

## Version 2 — `develop-v2` (development; browser testing pending)

### Added

- Eight-stage clickable EGFR/Ras/MAPK pathway explorer, including component explanations and a conceptual MEK-inhibition reasoning check.
- Per-lesson quiz statistics: answered count, correct count, and percentage accuracy.
- Twelve interactive terminology flashcards with reveal/hide behavior and a hide-all control.
- Six navigation sections: Learn, Quiz, Pathway, Flashcards, Progress, and Sources.
- Responsive layout and accessibility-oriented enhancements, including visible focus states and a skip link.
- Scientific reading suggestions, limitations, and an explicit statement that the app is AI-assisted rather than powered by a live AI model.

### Retained from Version 1

- Three lessons: Cell Signaling Fundamentals, RTKs, and Ras/MAPK Signaling.
- Nine multiple-choice quiz questions with immediate feedback.
- One recorded answer per question until the quiz is reset.
- Overall score, accuracy, progress indicator, review recommendation, and reset control.
- Standalone HTML operation without external libraries, server, or API key.

### Known limitations

- Quiz and flashcard states are not saved between page reloads.
- The pathway explorer is a simplified conceptual representation, not a quantitative simulation.
- Reference hyperlinks require internet access; core application interactions do not.
- The scientific explanations and references still require final verification against course materials and authoritative sources.
- Version 2 has been committed to GitHub, but full browser testing is not yet documented as complete.

## Version 1 — `main` (original baseline)

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

These observations are based on the screenshots shared during development, not an automated test suite.

## Version control approach

- `main` retains the original Version 1 baseline.
- `develop-v2` contains the enhanced Version 2 implementation.
- The development branch should not be merged into `main` until Version 2 acceptance tests and scientific review are completed.
