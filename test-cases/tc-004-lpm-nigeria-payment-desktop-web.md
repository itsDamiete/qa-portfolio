# Test Case Execution Report — Social Media Advertising Platform (Desktop Web)
# Local Payment Method — Nigeria

**Report ID:** TC-004
**Date:** 02 November 2025
**Tester:** Damiete Amachree
**Product:** Social media advertising platform — Desktop Web *(name withheld — NDA)*
**Build:** Production
**Platform:** Desktop Web (macOS — Chrome)
**Test Type:** Exploratory with Test Cases — Local Payment Method (LPM) Validation
**Overall Result:** ✅ Passed
**Time Spent:** 30 minutes

---

## Environment

| Field | Details |
|---|---|
| **Device** | MacBook (macOS Catalina 10.15.7) |
| **Browser** | Google Chrome (latest) |
| **Country** | Nigeria |
| **Language** | English |
| **Payment Method** | Naira Cards — Local Payment Method (Verve/Visa/Mastercard) |
| **Flow Type** | Add Payment / Add Funds via Payment Settings |
| **Build** | Production |

---

## Test Case Overview

This test case validated the end-to-end Local Payment Method (LPM) flow for Nigerian advertisers on a major social media advertising platform. The objective was to confirm that Naira-denominated payment methods (Verve/Visa/Mastercard via local payment gateway) are available, functional, and correctly reflect in the platform's billing section after a successful transaction. The test was executed on desktop web from Nigeria using a live advertising account with NGN billing currency.

---

## Step-by-Step Results

---

### Step 1 — Environment & Account Setup ✅ PASSED

Confirmed and documented the following prior to testing:

| Field | Value |
|---|---|
| **Testing location** | Nigeria |
| **Payment method** | Naira Payment (Verve/Visa/Mastercard) |
| **Language** | English |
| **Environment** | Desktop Web — Chrome |
| **Account type** | Ads billing account with LPM support (prepaid, non-postpaid) |
| **Account currency** | NGN (Nigerian Naira) |

Screenshots of browser version and device OS captured and attached as evidence.

---

### Step 2 — Slot Environment Confirmation ✅ PASSED

Confirmed the correct test environment as per slot assignment:
- **Platform:** Instagram Desktop Web (Mac)
- **Browser:** Chrome

Environment selection verified and documented.

---

### Step 3 — Pre-Testing Setup ✅ PASSED

Browser updated to the latest available version prior to commencing the test flow. Account was confirmed active and accessible with the correct billing configuration.

---

### Step 4 — Flow Type Selection ✅ PASSED

Selected flow type:
> **Add Payment / Add Fund flow — via Payment Settings**

Navigated to Payment Settings via the platform's billing and payments section on desktop web.

---

### Step 5 — Add Payment / Add Funds via Payment Settings ✅ PASSED

**Steps executed:**
1. Logged in to the assigned account on desktop web
2. Navigated to **Settings → Ad Payments → Payment Settings**
3. Clicked on **"Add a Payment Method / Add Funds"**
4. Selected **Naira Payment (Verve/Visa/Mastercard)** as the payment method
5. Entered payment amount equivalent to USD $5 in NGN
6. Completed the payment flow
7. Verified the **"Success"** confirmation screen was displayed
8. After a delay, returned to the Billing page on desktop to confirm the prepaid balance was reflected in the account

**Expected Result:**
- Naira LPM available in the payment method popup
- Transaction completes successfully
- Ad account prepaid balance is topped up and visible in billing

**Actual Result:**
All expected outcomes confirmed. Naira payment method was available, transaction completed successfully, and balance was updated in the billing section.

---

### Step 6 — Evidence Collection ✅ PASSED

The following evidence was captured and submitted:

| Evidence | Description |
|---|---|
| Screen recording (MP4) | Full end-to-end payment flow from login to success screen |
| Payment Method popup screenshot | Confirmed Naira LPM visible and selectable |
| Add Payment Details screenshot | Payment details entry screen captured |
| Transaction Confirmation screenshot | Success confirmation popup captured |
| Billing Transaction screenshot | Billing page showing updated prepaid balance (captured from desktop) |
| Transaction receipt screenshot | Email receipt confirming transaction |

---

### Step 7 — Transaction Details ✅ PASSED

| Field | Details |
|---|---|
| **Transaction status** | Successful |
| **Transaction date** | 02 November 2025 |
| **Transaction time** | 11:40 AM |
| **Transaction amount** | NGN 7,500 |

---

### Step 8 — Issues & Feedback

> No errors or bugs were encountered during the execution of this flow. The payment flow was seamless from start to finish.

---

## Summary

| Step | Description | Result |
|---|---|---|
| Step 1 | Environment & account setup | ✅ Passed |
| Step 2 | Slot environment confirmation | ✅ Passed |
| Step 3 | Pre-testing browser setup | ✅ Passed |
| Step 4 | Flow type selection | ✅ Passed |
| Step 5 | Add payment / add funds via Payment Settings | ✅ Passed |
| Step 6 | Evidence collection | ✅ Passed |
| Step 7 | Transaction details & receipt | ✅ Passed |
| Step 8 | Issues & feedback | ✅ No issues found |

---

## Notes
- This test involved a live financial transaction of NGN 7,500 on a production advertising account
- Reimbursement form submitted following successful transaction as required by the cycle
- All evidence files were named and submitted per cycle conventions
- Full video recording captured the unbroken payment flow end-to-end in MP4 format
- Billing page verification was performed from a desktop computer as required

---

> 📝 *This report is based on a real approved test case execution from a professional test cycle. Client and product identities, internal build details, account IDs, phone numbers, email addresses, social media handles, and all personal account information have been fully redacted in compliance with NDA obligations. The documentation format, structure, and write-up are entirely my own work.*
