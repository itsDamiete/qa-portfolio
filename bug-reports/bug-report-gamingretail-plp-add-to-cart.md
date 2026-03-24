# Bug Report — Gaming Retail Web Platform

**Bug ID:** BUG-001
**Date:** 02 December 2023
**Tester:** Damiete Amachree
**Product:** Gaming retail web platform *(name withheld — NDA)*
**Build:** [redacted]
**Platform:** Desktop Web
**Test Type:** Exploratory

---

## Summary
PLP — User is unable to add products to cart; add-to-cart pop-up window loops indefinitely instead of completing the action.

---

## Severity
🔴 **Critical**

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
| **OS** | Windows 10 Pro |
| **Browser** | Google Chrome (latest) |
| **Device** | Desktop PC |
| **URL** | [redacted — NDA] |

---

## Preconditions
- User is logged in to the platform

---

## Steps to Reproduce
1. Navigate to the platform's homepage
2. Hover over the hamburger menu
3. Click on **"Gaming Laptop"** from the dropdown menu
4. Scroll down to the first product on the Product Listing Page (PLP)
5. Click the **"Add to Cart"** button on the product
6. Click **"Add to Cart"** again in the pop-up window that appears

---

## Expected Result
The product is successfully added to the cart when the user clicks "Add to Cart" in the pop-up window. The cart count updates to reflect the newly added item.

---

## Actual Result
The pop-up window reappears every time the user clicks "Add to Cart" — creating an indefinite loop. The product is never added to the cart and the action cannot be completed.

---

## Impact
This is a checkout-blocking bug on the Product Listing Page. Users are completely unable to add products to their cart through the standard PLP flow, which directly prevents purchases and impacts revenue. Any user attempting to shop via the Gaming Laptop category will encounter this issue on every attempt.

---

## Status
✅ Approved — Rated **Exceptionally Valuable**
🔧 Resolution: Resolved

---

> 📝 *This bug report is based on a real approved submission from a professional test cycle. Client and product identities, internal URLs, and build details have been redacted in compliance with NDA obligations. The documentation format, structure, and write-up are entirely my own work.*
