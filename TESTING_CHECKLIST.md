# BioLearn AI — Manual Testing Checklist

**Testing policy:** Check a box only after performing the test and observing the expected result. The unchecked Version 2 items are **pending**, not failures. Record the device/browser and screenshots used as evidence.

## Test environment

- Tester: ____________________
- Date: ____________________
- Device and operating system: ____________________
- Browser and version (if known): ____________________
- Branch/commit tested: ____________________
- Network status (online/offline): ____________________

## Version 1 — previously observed on tablet

- [x] All nine quiz questions could be answered.
- [x] Dashboard displayed **9 answered, 8 correct, 89% accuracy**.
- [x] Dashboard displayed a full completion bar and a topic review suggestion.
- [x] Reset returned quiz statistics to **0 answered, 0 correct, 0% accuracy**.
- [x] Quiz questions appeared unanswered after reset.

Evidence: screenshots shared during the Version 1 prototype review. These checks do not establish full cross-browser compatibility or source-code correctness.

## Version 2 — pending acceptance tests

### A. Navigation and learning content

- [ ] All six tabs open: Learn, Quiz, Pathway, Flashcards, Progress, Sources.
- [ ] Three original lessons can be selected and display their intended content.
- [ ] No content overlaps or becomes inaccessible on a tablet/mobile screen.

### B. Interactive pathway

- [ ] All eight pathway stages can be selected.
- [ ] Component detail text changes to match the selected stage.
- [ ] The MEK-inhibition reasoning question shows appropriate feedback for both choices.
- [ ] The diagram and explanation clearly indicate they are a simplified model.

### C. Flashcards

- [ ] All 12 flashcards appear.
- [ ] Tapping a card reveals its definition; tapping again hides it.
- [ ] The revealed-card counter updates correctly.
- [ ] **Hide all cards** restores 0/12 revealed.

### D. Quiz and analytics

- [ ] All nine questions can be answered.
- [ ] Correct and incorrect selections show appropriate feedback.
- [ ] An answered question cannot be scored a second time without reset.
- [ ] Overall score and accuracy are calculated correctly (example: 8/9 → 89%).
- [ ] Per-lesson answered and correct counts agree with the three questions in each lesson.
- [ ] Review recommendation identifies a lesson containing an incorrect answer.
- [ ] Reset returns quiz answers and all overall/per-lesson statistics to zero.

### E. Offline operation and usability

- [ ] Download `index.html`, disable internet, and open it locally.
- [ ] Lessons, pathway, flashcards, quiz, and analytics work without internet.
- [ ] External source links are correctly identified as requiring internet.
- [ ] Page remains usable in portrait and landscape orientations.
- [ ] Keyboard Tab and Enter/Space operate interactive controls where applicable.
- [ ] Reloading the page resets in-memory progress (expected limitation).

### F. Scientific and academic integrity

- [ ] Verify ligand/receptor/transduction descriptions against course lectures or a reliable textbook.
- [ ] Verify RTK activation and phosphorylation descriptions, including receptor-specific differences.
- [ ] Verify Ras-GTP, Raf, MEK, and ERK relationships and terminology.
- [ ] Confirm the app and report do not imply a live AI model or experimentally validated simulation.
- [ ] Confirm no personal identifiers appear in the public repository or screenshots.

## Evidence to collect

- [ ] Screenshot: Version 2 home/lessons.
- [ ] Screenshot: selected pathway component and its explanation.
- [ ] Screenshot: flashcard before/after reveal.
- [ ] Screenshot: completed quiz with correct/incorrect feedback.
- [ ] Screenshot: per-lesson analytics and overall score.
- [ ] Screenshot: reset dashboard.
- [ ] Screenshot: GitHub `develop-v2` branch and commit history.

## Issues and fixes

| Test / issue | Expected | Actual result | Fix or follow-up | Retested? |
| --- | --- | --- | --- | --- |
| _Add an entry after testing_ | | | | |

## Final acceptance

- [ ] All critical functional tests passed.
- [ ] Any remaining limitations are disclosed in the report.
- [ ] Version 2 is ready to be demonstrated or released.

**Status at document creation:** Version 1 screenshot-based checks completed; Version 2 browser acceptance testing postponed.
