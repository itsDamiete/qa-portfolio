# Test Case Execution Report — E-Learning Mobile App (Android)

**Report ID:** TC-001
**Date:** 20 March 2026
**Tester:** Damiete Amachree
**Product:** E-learning mobile app — Android *(name withheld — NDA)*
**Build:** [redacted]
**Platform:** Android Mobile App (Native)
**Test Type:** Functional Smoke Test
**Test Case:** [Smoke] Quiz
**Overall Result:** ❌ Failed (1 step failed, 4 steps passed)

---

## Environment

| Field | Details |
|---|---|
| **Device** | Xiaomi Redmi 14C |
| **OS** | Android 16 |
| **Network** | Airtel (Nigeria) |
| **App Type** | Native (no mobile browser) |
| **Build** | [redacted] |

---

## Test Case Overview

This smoke test covered the core Quiz functionality within a course on the e-learning platform. Five key quiz user flows were validated across a single test run.

---

## Step-by-Step Results

---

### Step 1 — Complete Quiz ❌ FAILED

**Precondition:** User is logged in and enrolled in a course that contains a Quiz.

**Steps:**
1. Launch the app
2. Open the course
3. Take the Quiz and complete it

**Expected Result:**
A completed checkmark (✓) appears next to the quiz in the curriculum list immediately after the user finishes the quiz.

**Actual Result:**
The completed quiz tick mark does **not** appear immediately after the user completes the quiz. The curriculum list does not update to reflect the completed status in real time.

**Severity:** 🟠 High
**Issue:** Raised and Approved ✅

---

### Step 2 — Resume Incomplete Quiz ✅ PASSED

**Precondition:** User is logged in and enrolled in a course that contains a Quiz.

**Steps:**
1. Launch the app
2. Open the course
3. Begin the quiz, answer a few questions, then navigate away
4. Navigate back to the same quiz

**Expected Result:**
The user is taken directly to the first unanswered question so they can continue from where they left off.

**Actual Result:**
Behaved as expected. User was correctly resumed at the first unanswered question.

---

### Step 3 — Confetti on Completed Quiz ✅ PASSED

**Precondition:** User is logged in and enrolled in a course that contains a Quiz.

**Steps:**
1. Launch the app
2. Open the course
3. Complete the quiz with a passing score

**Expected Result:**
A confetti animation appears and the "Next Lecture" button turns purple upon successful quiz completion with a passing score.

**Actual Result:**
Behaved as expected. Confetti animation displayed correctly and the "Next Lecture" button turned purple as designed.

---

### Step 4 — View Completed Quiz Performance ✅ PASSED

**Precondition:** User is logged in and has already completed a quiz.

**Steps:**
1. Launch the app
2. Open the course
3. Complete the quiz
4. Re-open the quiz to view results

**Expected Result:**
The user can re-enter the completed quiz and view their performance and results across all questions.

**Actual Result:**
Behaved as expected. Quiz performance and results page displayed correctly.

---

### Step 5 — Retake Quiz ✅ PASSED

**Precondition:** User is logged in and has already completed a quiz.

**Steps:**
1. Launch the app
2. Navigate to the completed quiz
3. Locate and use the retake option

**Expected Result:**
A retake option is available and the user can restart the quiz from the beginning.

**Actual Result:**
Behaved as expected. Retake quiz button was present and functional.

---

## Summary

| Step | Description | Result |
|---|---|---|
| Step 1 | Complete Quiz — tick mark visibility | ❌ Failed |
| Step 2 | Resume incomplete Quiz | ✅ Passed |
| Step 3 | Confetti on completed Quiz | ✅ Passed |
| Step 4 | View Quiz performance/results | ✅ Passed |
| Step 5 | Retake Quiz | ✅ Passed |

---

## Bug Raised

**Issue:** Completed quiz tick mark does not appear in the curriculum list immediately after the user finishes the quiz.
**Severity:** High
**Type:** Functional
**Status:** ✅ Approved

---

## Notes
- All 5 steps were executed within a single 30-minute test session
- Evidence collected for each step: screenshots for Steps 1, 3, 4, and 5; screen recording for Step 2
- Smoke test status set to **Failed** due to Step 1 failure — a core curriculum progress indicator not updating is considered a blocking issue for this smoke cycle

---

> 📝 *This report is based on a real approved test case execution from a professional test cycle. Client and product identities, internal build details, course names, and tester account information have been redacted in compliance with NDA obligations. The documentation format, structure, and write-up are entirely my own work.*
