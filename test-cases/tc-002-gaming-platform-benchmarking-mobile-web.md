# Test Case Execution Report — Online Gaming & Betting Platform (Mobile Web)

**Report ID:** TC-002
**Date:** 17 February 2026
**Tester:** Damiete Amachree
**Product:** Online gaming & betting platform — Mobile Web *(name withheld — NDA)*
**Build:** [redacted]
**Platform:** Mobile Web (Android — Chrome)
**Test Type:** Exploratory with Test Cases — Global Benchmarking
**Overall Result:** ✅ Passed
**Time Spent:** 4 hours

---

## Environment

| Field | Details |
|---|---|
| **Device** | Samsung Galaxy S23 FE |
| **OS** | Android 16 |
| **Browser** | Google Chrome |
| **Network** | Glo Mobile (Nigeria) |
| **Country** | Nigeria |
| **Build** | [redacted] |

---

## Test Case Overview

This was a competitive benchmarking test case evaluating the end-to-end user experience of an online gaming platform across six key functional areas: environment setup, consent signing, registration, account verification (KYC), payments, and account balance reconciliation. Real deposits and withdrawals were made as part of the payment testing flow. All steps were executed using the mobile web browser on an Android device.

---

## Step-by-Step Results

---

### Step 1 — Environment Information ✅ PASSED

Captured and submitted a screenshot confirming the test environment — device model, OS version, and browser. Evidence was documented prior to beginning any functional testing steps.

---

### Step 2 — Consent Signing ✅ PASSED

Reviewed and signed the required tester consent agreement before proceeding with the test. Signed consent document was uploaded as evidence. This step ensured compliance with platform and client requirements before any live testing activity.

---

### Step 3 — Registration Flow ✅ PASSED

**Scope tested:**
- Full registration flow via email
- Social login option availability and provider identification
- Mobile number requirement during registration
- OTP/confirmation delivery to mobile number and email address
- Mobile number uniqueness validation (duplicate registration attempt)

**Observations documented:**
- Social login options were present; providers were identified and noted
- Mobile number field behaviour (mandatory/optional) was recorded
- OTP confirmation behaviour on both mobile and email was captured with screenshots
- Mobile uniqueness check was performed by attempting re-registration with the same number — platform response was documented
- Full video recording captured the unbroken registration flow end-to-end

---

### Step 4 — Account Verification (KYC) ✅ PASSED

**Scope tested:**
- KYC trigger point — whether verification was required at registration or post-registration
- Availability of docless KYC options (e.g. digital ID, tax credentials)
- eKYC provider availability and identification
- Identity document upload requirements
- Proof of address document requirements
- Time taken to complete KYC from submission to confirmation
- Face authentication / liveness check requirement
- Rejection reason clarity (negative testing on document quality)

**Observations documented:**
- All KYC steps were executed and responses recorded in the required survey form
- Document upload flow, provider logos, and confirmation methods were captured via screenshot and video
- KYC completion time was tracked from submission to confirmation notification

---

### Step 5 — Payment Flow (Deposit & Withdrawal) ✅ PASSED

**Scope tested:**
- All available deposit methods identified and documented
- One deposit transaction completed using minimum amount
- Withdrawal attempted using a different payment method than the deposit method
- If cross-method withdrawal was blocked, withdrawal retried using the original deposit method
- Withdrawal processing time tracked from initiation to completion

**Observations documented:**
- Available deposit options catalogued
- Cross-method withdrawal behaviour recorded (permitted or blocked)
- Two screenshots captured: withdrawal initiation and withdrawal completion
- Full payment flow recorded on video without breaks

**Transaction Summary:**

| Transaction | Amount |
|---|---|
| Total deposited | $0.82 USD |
| Amount withdrawn | $0.82 USD |
| Amount not withdrawable | $0.00 USD (0 NGN) |

---

### Step 6 — Account Balance Reconciliation ✅ PASSED

All remaining funds in the account were withdrawn following the completion of payment testing. Full balance reconciliation was documented confirming zero unrecoverable funds at end of cycle.

| Field | Amount |
|---|---|
| Total deposited | $0.82 USD |
| Amount withdrawable | $0.82 USD |
| Amount not withdrawable | $0.00 USD / 0 NGN |

---

## Summary

| Step | Description | Result |
|---|---|---|
| Step 1 | Environment setup | ✅ Passed |
| Step 2 | Consent signing | ✅ Passed |
| Step 3 | Registration flow | ✅ Passed |
| Step 4 | Account verification (KYC) | ✅ Passed |
| Step 5 | Payment flow (deposit & withdrawal) | ✅ Passed |
| Step 6 | Account balance reconciliation | ✅ Passed |

---

## Notes
- This benchmarking cycle required live financial transactions using real payment methods — all deposits were made with the minimum permissible amount
- Test evidence including screenshots and screen recordings was uploaded to an external drive as required by the cycle
- Survey/Google Form responses were completed and submitted in full alongside step execution
- Full 4-hour session executed without interruption across all 6 steps
- Cycle approved with full payout

---

> 📝 *This report is based on a real approved test case execution from a professional benchmarking test cycle. Client and product identities, brand names, internal build details, external links, consent documents, tester account information, and survey form details have been redacted in compliance with NDA obligations. The documentation format, structure, and write-up are entirely my own work.*
