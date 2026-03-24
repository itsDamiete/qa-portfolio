# Bug Report — Art Marketplace Mobile App (Android)

**Bug ID:** BUG-003
**Date:** 15 April 2024
**Tester:** Damiete Amachree
**Product:** Art marketplace mobile app — Android *(name withheld — NDA)*
**Build:** [redacted]
**Platform:** Android Mobile App (Native)
**Test Type:** Exploratory with Test Cases
**Source:** Exploratory

---

## Summary
Credit card and billing address details are completely cleared when the user edits their Max Bid amount during the auction bidding flow, forcing them to re-enter all payment information from scratch.

---

## Severity
🟠 **High**

---

## Issue Type
Functional

---

## Frequency
Every Time (100% reproducible)

---

## Environment

| Field | Details |
|---|---|
| **Device** | Google Pixel 5a |
| **OS** | Android 14 |
| **App Type** | Native (no mobile browser) |
| **Network** | Airtel (Nigeria) |
| **App Build** | [redacted] |
| **Staging** | Reproducible on both staging and production |

---

## Preconditions
- User is logged in to the app
- User has access to active auction lots
- User has a valid credit card and billing address to enter

---

## Steps to Reproduce
1. Open the app
2. Scroll down to **"Auction Lots for You Ending Soon"**
3. Tap on any available auction lot
4. Tap on **"Bid"**
5. Select a Max Bid amount
6. Tap **"Next"**
7. Tap **"Add"** to add a credit card
8. Enter credit card details and tap **"Add credit card"**
9. Tap **"Add"** to add a billing address
10. Fill out the billing address form and tap **"Add billing address"**
11. In the Max Bid field, tap **"Edit"**
12. Choose a different max bid amount
13. Tap **"Next"**

---

## Expected Result
The user is returned to the **"Confirm your bid"** page with all previously entered credit card and billing address information still intact and displayed correctly.

---

## Actual Result
When the user is returned to the **"Confirm your bid"** page after editing their max bid, all credit card and billing address information has been completely cleared. The user is forced to re-enter their full payment details before they can proceed.

---

## Impact
This is a high-severity bug in a revenue-critical flow — the auction bidding and payment process. Users who edit their max bid after entering payment details lose all that information and must start over. In a time-sensitive auction environment where lots are ending soon, this friction is likely to cause users to abandon their bids entirely, resulting in direct loss of transactions. The fact that it is reproducible on both staging and production increases the urgency significantly.

---

## Status
✅ Approved — Rated **Exceptionally Valuable**
🔧 Resolution: Resolved

---

> 📝 *This bug report is based on a real approved submission from a professional test cycle. Client and product identities, internal build details, and app-specific identifiers have been redacted in compliance with NDA obligations. The documentation format, structure, and write-up are entirely my own work.*
