# BioLearn AI — Manual Testing Checklist

**Release under review:** [V2.0 — Week 9 Midterm Prototype](https://github.com/jesseicaj2/BioLearn-ai/releases/tag/V2.0) (November 1, 2026)

**Testing policy:** A checked box means a test was supported by a screenshot or explicit user confirmation. Unchecked items are **not yet verified**, not failures. Partial evidence is described rather than treated as a complete pass. Testing was manual, not automated.

## Test environment

- **Tester:** Project author (manual user testing)
- **Date:** November 1, 2026
- **Device and operating system:** Android tablet; exact device model and OS version not recorded
- **Browser and version:** Chrome interface visible in screenshots; exact version not recorded
- **Version tested:** Local Version 2 HTML file, followed by the live V2.0 GitHub Pages deployment
- **Repository:** [`main`](https://github.com/jesseicaj2/BioLearn-ai/tree/main); [V2.0 release](https://github.com/jesseicaj2/BioLearn-ai/releases/tag/V2.0)
- **Network status:** Local `content://` file opened and tested; live GitHub Pages tested online. A controlled offline/airplane-mode test was not documented.
- **Evidence:** Screenshots and confirmations supplied during project testing; not yet uploaded as a formal test-evidence folder in the repository

## Version 1 — previously observed on tablet

- [x] All nine quiz questions could be answered.
- [x] Dashboard displayed **9 answered, 8 correct, 89% accuracy**.
- [x] Dashboard displayed a full completion bar and a topic review suggestion.
- [x] Reset returned quiz statistics to **0 answered, 0 correct, 0% accuracy**.
- [x] Quiz questions appeared unanswered after reset.

Evidence: screenshots shared during the Version 1 prototype review. These checks do not establish full cross-browser compatibility or source-code correctness.

## Version 2 — manual acceptance testing

### A. Navigation and learning content

- [x] All six tabs open: Learn, Quiz, Pathway, Flashcards, Progress, Sources.
- [x] Three original lessons can be selected and display their intended content.
- [x] Screenshots show the core sections readable on the tested Android tablet screen.
- [ ] Confirm no overlap or inaccessible content at additional narrow screen widths and orientations.

### B. Interactive pathway

- [x] The pathway explorer displays selectable stages and component detail information (EGF shown in the supplied screenshot).
- [x] The MEK-inhibition reasoning check shows appropriate feedback for the **ERK activation decreases** choice.
- [x] The interface describes the diagram as a simplified canonical pathway rather than a quantitative simulation.
- [ ] Individually select and verify the detail text for **all eight** pathway stages.
- [ ] Verify the feedback for the alternative **ERK activation increases** choice.

### C. Flashcards

- [x] All 12 distinct flashcards appear in the final clarified screenshot.
- [x] Tapping cards reveals definitions; the author confirmed the flip-back behavior.
- [x] The revealed-card counter displays an observed state of 3/12 and returns to 0/12 after hiding cards.
- [x] **Hide all cards** restores 0/12 revealed.
- [ ] Systematically verify both sides of every card and the counter for all possible reveal counts.

### D. Quiz and analytics

- [x] Quiz questions and answer choices render in the V2.0 interface.
- [x] Correct and incorrect answer selections show immediate feedback in the observed examples.
- [x] The progress dashboard displays an observed partial result of **2 answered, 1 correct, 50% accuracy**.
- [x] Lesson-specific analytics show **1 correct / 2 answered** for Cell Signaling Fundamentals in that attempt; the other two lessons were not attempted.
- [x] The review recommendation identifies Cell Signaling Fundamentals for the observed partial attempt.
- [x] The author confirmed **Reset quiz and try again** works.
- [ ] Complete and document a full nine-question V2.0 attempt, including a verified final overall score.
- [ ] Confirm an answered question cannot be scored again without reset.
- [ ] Independently check per-lesson counts for all three lessons and multiple scoring combinations.
- [ ] Capture before/after screenshots verifying every overall and per-lesson statistic returns to zero on reset.

### E. Deployment, offline operation, and usability

- [x] GitHub Pages build and deployment reported success.
- [x] The author confirmed the live application works smoothly at https://jesseicaj2.github.io/BioLearn-ai/.
- [x] The application was opened and interacted with as a local HTML file on Android (as shown by the `content://` browser address).
- [x] The Sources section is visible and identifies suggested external references.
- [ ] Disable internet deliberately, open the downloaded HTML file, and verify lessons, pathway, flashcards, quiz, and analytics.
- [ ] Verify external links behave as expected without internet access.
- [ ] Test portrait and landscape orientations explicitly.
- [ ] Test keyboard Tab, Enter, and Space operation of interactive controls, including any skip link.
- [ ] Reload the page and confirm that in-memory quiz/flashcard progress resets as documented.
- [ ] Test another browser or device and document the result.

### F. Scientific and academic integrity

- [x] The Sources screen discloses that the application is AI-assisted and does not run a live AI model.
- [x] The Sources screen states limitations of the simplified signaling model.
- [ ] Independently verify ligand/receptor/transduction descriptions against course lectures or a reliable textbook.
- [ ] Independently verify RTK activation and phosphorylation descriptions, including receptor-specific differences.
- [ ] Independently verify Ras-GTP, Raf, MEK, and ERK relationships and terminology.
- [ ] Review the midterm report and demonstration script for consistent AI-use and simulation claims.
- [ ] Review the public repository and submitted screenshots for unintended personal information.

## Evidence to collect or organize

- [x] Screenshot: Version 2 lessons (all three selections).
- [x] Screenshot: pathway component explanation and the observed reasoning-check feedback.
- [x] Screenshot: flashcards revealed and hidden, including 0/12 counter.
- [x] Screenshot: correct and incorrect quiz feedback for observed questions.
- [x] Screenshot: per-lesson analytics and overall partial-attempt score.
- [x] Screenshot: GitHub release pages showing V1.0 and V2.0.
- [x] Screenshot: successful GitHub Pages build and deployment.
- [ ] Capture a complete V2.0 nine-question quiz result and reset evidence.
- [ ] Save selected evidence screenshots to a clearly named repository folder or midterm submission package.
- [ ] Document a controlled offline test and additional browser/accessibility testing if required.

**Evidence note:** Checked screenshot items refer to images shared during the development conversation, not necessarily files already committed to GitHub.

## Issues and follow-ups

| Item | Observation | Status / follow-up |
| --- | --- | --- |
| Apparent duplicate flashcards in an earlier screenshot | The author clarified this was a screenshotting error; the final screenshot shows 12 distinct cards. | **Resolved; no application defect established.** |
| Full pathway coverage | A selected component and one reasoning response were observed. | Verify remaining stages and alternative response. |
| Offline behavior | Local file interactions observed, but no controlled network-disabled test recorded. | Perform airplane-mode test before claiming verified offline behavior. |
| Scientific verification | Suggested sources and limitations are displayed, but no line-by-line verification record supplied. | Cross-check with course lectures and authoritative references. |

## Final acceptance

- [x] Core manually observed functionality supports the Week 9 V2.0 prototype demonstration.
- [x] V2.0 was merged into `main`, published as a GitHub release, and deployed through GitHub Pages.
- [x] Known limitations are disclosed in the README and changelog.
- [ ] All acceptance-test cases above have been executed and passed.
- [ ] Independent scientific content review has been completed and documented.

**Current status:** **Released and demonstrated as a functioning midterm prototype**, with documented manual test evidence and explicitly outstanding verification items. Do not interpret release status as exhaustive quality assurance.
