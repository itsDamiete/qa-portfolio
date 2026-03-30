# Test Case Execution Report — E-Learning Mobile App (Android) — API & Proxy Testing

**Report ID:** TC-003
**Date:** 06 February 2026
**Tester:** Damiete Amachree
**Product:** E-learning mobile app — Android *(name withheld — NDA)*
**Build:** [redacted]
**Platform:** Android Mobile App (Native)
**Test Type:** Functional Smoke Test — API Testing (Charles Proxy + Logcat)
**Overall Result:** ❌ Failed (1 step failed, 7 steps passed)
**Time Spent:** 3 hours

---

## Environment

| Field | Details |
|---|---|
| **Device** | Xiaomi Redmi 14C |
| **OS** | Android 15 |
| **Network** | Airtel (Nigeria) |
| **App Type** | Native (no mobile browser) |
| **Build** | [redacted] |
| **Proxy Tool** | Charles Proxy |
| **Log Tool** | Android Logcat |

---

## Test Case Overview

This was an API-focused smoke test requiring Charles Proxy and Logcat setup to intercept and validate network calls made by the app during specific user interactions. The test covered API call verification across core app features including search, course progress tracking, offline playback behaviour, playback speed synchronisation, and engagement event tracking. Evidence was collected in the form of Charles session files (.chlz), logcat files (.txt), and annotated screenshots for each step.

---

## Step-by-Step Results

---

### Step 1 — Device OS and App Version ✅ PASSED

Captured and submitted screenshots confirming the device OS version and the app build number. Both the device About page and the app's account tab (showing version info) were documented before testing began.

---

### Step 2 — Verify /funnel-logs on Logcat ❌ FAILED

**Steps executed:**
1. Launched the app as a logged-in user and waited for the Featured page to load fully
2. Scrolled to the end of the Featured tab
3. Tapped on the My Learning tab and waited for at least 20 seconds

**Expected Result:**
`/funnel-logs` API calls should appear in the logcat output and be searchable via Ctrl+F.

**Actual Result:**
`/funnel-logs` were **not called** in the logcat files during the test session. The expected API call was absent entirely.

**Evidence:** Logcat file captured and attached (approx. 1MB). Issue raised and approved. ✅

**Severity:** High
**Issue Status:** Approved ✅

---

### Step 3 — Verify /search-courses/mobile on Charles Proxy ✅ PASSED

**Steps executed:**
1. Launched the app
2. Tapped on the Search field
3. Searched for a course

**Expected Result:**
`/search-courses/mobile` API call is fired and visible in Charles Proxy when a course search is performed.

**Actual Result:**
`/search-courses/mobile` was confirmed present in Charles Proxy. Call verified using Ctrl+F search within the proxy session.

**Evidence:** Charles session file (.chlz) and annotated screenshot captured and submitted.

---

### Step 4 — Verify /completed-lectures on Charles Proxy ✅ PASSED

**Steps executed:**
1. Launched the app
2. Opened an enrolled course
3. Completed all video lectures in the course

**Expected Result:**
`/completed-lectures` API call is fired in Charles Proxy upon completing all video lectures in a course.

**Actual Result:**
`/completed-lectures` call was confirmed present and firing correctly in Charles Proxy after lecture completion.

**Evidence:** Charles session file (.chlz — approx. 20MB) and annotated screenshot captured and submitted.

---

### Step 5 — Verify /progress-logs on Charles Proxy (Fast Forward) ✅ PASSED

**Steps executed:**
1. Launched the app as a logged-in user
2. Opened an enrolled course
3. Played a lecture video for a few seconds
4. Tapped the video player to display controls
5. Fast-forwarded the lecture and allowed it to play for at least 90 seconds

**Expected Result:**
`/progress-logs` API calls are fired in Charles Proxy after the lecture plays for 90 seconds.

**Actual Result:**
`/progress-logs` calls were confirmed present and firing at the expected interval after 90 seconds of playback.

**Evidence:** Charles session file (.chlz — approx. 20MB) and annotated screenshot captured and submitted.

---

### Step 6 — Verify /progress-logs Frequency vs Playback Speed on Charles Proxy ✅ PASSED

**Steps executed:**
1. Launched the app as a logged-in user
2. Opened an enrolled course
3. Played a lecture at default speed (1.0x) for at least 90 seconds
4. Searched for `/progress-logs` in Charles Proxy
5. Opened a request and verified `playback_speed` value = 1 in JSON view
6. Inspected multiple `time` fields — confirmed consistent ~15 second intervals
7. Changed playback speed to 2.0x and continued playing
8. Located new `/progress-logs` requests in Charles Proxy
9. Verified `playback_speed` value = 2 in JSON view
10. Confirmed `time` field intervals were now approximately twice as frequent (~7 seconds apart)

**Expected Result:**
`/progress-logs` frequency doubles when playback speed changes from 1.0x to 2.0x. JSON payload reflects the correct `playback_speed` value at both speeds.

**Actual Result:**
Behaviour confirmed as expected. `playback_speed` values were accurate and log frequency correctly corresponded to playback speed changes at both 1.0x and 2.0x.

**Evidence:** Charles session file (.chlz — approx. 23MB) and 5 annotated screenshots captured and submitted showing JSON payload at both speeds.

---

### Step 7 — Verify /progress-logs for Offline Video Playback ✅ PASSED

**Steps executed:**
1. Pre-condition: A lecture was already downloaded to the device
2. Switched OFF internet connection
3. Launched the app as a logged-in user
4. Opened the downloaded lecture and played it for at least 90 seconds
5. Killed the app
6. Switched ON internet connection
7. Relaunched the app

**Expected Result:**
Progress logs are saved locally every 90 seconds while offline. Once the user reconnects and restarts the app, the locally saved progress logs are dispatched and appear in Charles Proxy.

**Actual Result:**
`/progress-logs` calls were confirmed firing in Charles Proxy after the app was relaunched with internet restored. Offline-to-online sync behaviour functioned as expected.

**Evidence:** Charles session file (.chlz) and annotated screenshot captured and submitted.

---

### Step 8 — Verify Weekly Streak Events on Charles Proxy ✅ PASSED

**Steps executed:**
1. Navigated to the Weekly Streaks section on the Featured page
2. Tapped the **"i"** icon on the Weekly Streaks section

**Expected Result:**
- `WeeklyStreakImpressionEvent` is fired and visible in Charles Proxy
- `WeeklyStreakInfoClickEvent` is fired and visible in Charles Proxy

**Actual Result:**
Both `WeeklyStreakImpressionEvent` and `WeeklyStreakInfoClickEvent` were confirmed present and firing correctly in Charles Proxy.

**Evidence:** 2 annotated screenshots captured and submitted confirming both event calls.

---

## Summary

| Step | Description | Result |
|---|---|---|
| Step 1 | Device OS and app version | ✅ Passed |
| Step 2 | /funnel-logs on Logcat | ❌ Failed |
| Step 3 | /search-courses/mobile on Charles Proxy | ✅ Passed |
| Step 4 | /completed-lectures on Charles Proxy | ✅ Passed |
| Step 5 | /progress-logs on Charles Proxy (fast forward) | ✅ Passed |
| Step 6 | /progress-logs frequency vs playback speed | ✅ Passed |
| Step 7 | /progress-logs for offline playback | ✅ Passed |
| Step 8 | Weekly streak events on Charles Proxy | ✅ Passed |

---

## Bug Raised

**Issue:** `/funnel-logs` are not called in logcat when navigating the Featured tab and My Learning tab.
**Severity:** High
**Type:** Functional
**Status:** ✅ Approved

---

## Notes
- Charles Proxy was configured and active throughout the entire test session
- Logcat was running and captured during Step 2
- All Charles session files (.chlz) and logcat files were attached as evidence per cycle requirements
- Test cycle status set to **Failed** due to Step 2 failure — absence of expected `/funnel-logs` API call
- All 8 steps executed within a single 3-hour session

---

> 📝 *This report is based on a real approved test case execution from a professional test cycle. Client and product identities, internal build details, course names, approver names, academy links, and tester account information have been redacted in compliance with NDA obligations. The documentation format, structure, and write-up are entirely my own work.*
