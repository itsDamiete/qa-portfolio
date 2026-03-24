# Bug Report — Social Media Advertising Platform

**Bug ID:** BUG-002
**Date:** 16 March 2024
**Tester:** Damiete Amachree
**Product:** Social media advertising platform *(name withheld — NDA)*
**Build:** [redacted]
**Platform:** Desktop Web
**Test Type:** Exploratory with Test Cases
**Source:** Structured (Test Case)

---

## Summary
[Naira Cards — Local Payment Method] en_NG — "Couldn't add funds" error message appears when attempting to add funds using a Naira payment method on the advertising platform.

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
| **OS** | Windows 10 Pro 22H2 / Windows Feature Experience Pack 1000.19053.1000.0 |
| **Browser** | Google Chrome Version 122.0.6261.112 |
| **Device** | HP ProBook 650 G2 |
| **Language** | English (en_NG) |
| **Country** | Nigeria |
| **Payment Method** | Naira Cards — Local Payment Method (PayU) |
| **Bank** | Guaranty Trust Bank (Nigeria) — Savings — Naira (NGN) |
| **Date & Time Found** | 13:02 GMT+1, 16 March 2024 |

---

## Preconditions
- User is logged in to the advertising platform
- A Naira Card (Local Payment Method) has been assigned to the account
- User has an existing post ready to boost
- Budget is set to at least $10 USD equivalent

---

## Steps to Reproduce
1. Launch the advertising platform's Business Suite
2. Create a post and select **"Boost Post"**
3. Proceed through the boost post setup
4. Accept the Non-Discrimination policy if prompted
5. Adjust the budget to at least $10 USD equivalent
6. Scroll down and select **"Add Payment Method"**
7. Select the assigned payment method (Naira Cards — Local Payment Method)
8. Enter the payment amount
9. Click the **"Next"** button

---

## Expected Result
The assigned Naira payment method is displayed correctly in the Payment Method popup. The payment flow completes successfully and the post is boosted without errors.

---

## Actual Result
On the Add Funds page, the user receives the following error message after selecting the Naira payment method and clicking Next:

> **"Couldn't add funds. Please try again or select a different payment method."**

The payment cannot be completed and the post cannot be boosted using the Naira local payment method.

---

## Impact
This is a payment-blocking bug that directly prevents Nigerian advertisers from funding their accounts using a locally assigned Naira payment method. Users attempting to boost posts or run ads via the Naira (NGN) payment flow are completely unable to complete transactions, effectively locking out a Nigerian market segment from using the platform's advertising features. Given that local payment method support is critical for market adoption in Nigeria, this bug has significant business and revenue implications.

---

## Status
✅ Approved — Rated **Exceptionally Valuable**
🔧 Resolution: Resolved

---

> 📝 *This bug report is based on a real approved submission from a professional test cycle. Client and product identities, internal account details, user IDs, platform URLs, and build information have been redacted in compliance with NDA obligations. The documentation format, structure, and write-up are entirely my own work.*
