# Bug Report — Fitness Tracking Mobile App (Android)

**Bug ID:** BUG-005
**Date:** 23 January 2024
**Tester:** Damiete Amachree
**Product:** Fitness tracking mobile app — Android *(name withheld — NDA)*
**Build:** [redacted]
**Platform:** Android Mobile App (Native)
**Test Type:** Exploratory with Test Cases
**Source:** Exploratory

---

## Summary
Community — App crashes when the user attempts to select a challenge history item for the second time; first tap navigates away incorrectly, second tap causes a full app crash.

---

## Severity
🟠 **High**

---

## Issue Type
Crash

---

## Frequency
Every Time (100% reproducible)

---

## Environment

| Field | Details |
|---|---|
| **Device** | Infinix Smart 5 |
| **OS** | Android 10 |
| **Network** | Glo Mobile (Nigeria) |
| **App Type** | Native Android |
| **Build** | [redacted] |

---

## Preconditions
- User is logged in to the app
- User has existing challenge history visible under their community group

---

## Steps to Reproduce
1. Open the app
2. Tap on the **"Community"** tab
3. Tap on the **"Groups"** tab
4. Tap on the **three-dot icon** at the top-right of the screen
5. Tap on **"Challenge History"**
6. Tap on any item in the challenge history list
7. Observe the result — user is navigated away from the page
8. Navigate back and tap the same item a **second time**

---

## Expected Result
On the first tap, the user is shown the full details of the selected challenge history item. The app remains stable and responsive throughout.

---

## Actual Result
**First tap:** Instead of displaying the challenge history item details, the user is unexpectedly navigated back to the Community page. No details are shown.

**Second tap:** When the user navigates back to the Challenge History list and taps the same item again, the app crashes completely.

---

## Impact
This is a two-stage bug with escalating severity. The first tap produces incorrect navigation behaviour, which alone is a functional failure. The second tap causes a full app crash — making this a High severity issue that completely prevents users from accessing their challenge history. For a fitness app where community engagement and challenge tracking are core features, losing access to challenge history damages user trust and retention. With 3 community reproductions confirmed, this affects multiple devices and is not environment-specific.

---

## Status
✅ Approved — Rated **Very Valuable**
🔧 Resolution: Resolved

---

> 📝 *This bug report is based on a real approved submission from a professional test cycle. Client and product identities, internal build details, and platform-specific identifiers have been redacted in compliance with NDA obligations. The documentation format, structure, and write-up are entirely my own work.*
