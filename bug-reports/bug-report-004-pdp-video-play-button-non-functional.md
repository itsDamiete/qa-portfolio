# Bug Report — Retail E-Commerce Website (Beauty & Fragrance)

**Bug ID:** BUG-004
**Date:** 01 July 2024
**Tester:** Damiete Amachree
**Product:** Retail e-commerce website — Beauty & Fragrance *(name withheld — NDA)*
**Build:** [redacted]
**Platform:** Desktop Web
**Test Type:** Exploratory with Test Cases
**Source:** Exploratory

---

## Summary
PDP — The Play button on a brand product video is completely non-functional; clicking it produces no reaction and the video does not play.

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
| **OS** | Windows 10 Pro |
| **Browser** | Google Chrome (latest) |
| **Device** | HP ProBook 650 G2 |
| **Connection** | Wi-Fi |
| **Country/Locale** | Nigeria |
| **Login Required** | No (guest user) |
| **Date & Time Found** | 15:30, 01 July 2024 |
| **Console Errors** | None observed |

---

## Preconditions
- User is not required to be logged in
- User is on the Product Detail Page (PDP) of a specific fragrance product that contains an embedded brand video

---

## Steps to Reproduce
1. Navigate to the retail website
2. Scroll down to the **"Our Favourites"** section on the homepage
3. Click on the featured fragrance product
4. On the Product Detail Page (PDP), scroll down to the embedded video section
5. Click the **Play** button on the video

---

## Expected Result
The video begins playing when the user clicks the Play button. Video playback resumes as expected.

---

## Actual Result
Nothing happens when the user clicks the Play button. There is no visual feedback, no loading indicator, and no video playback. The button appears functional but is completely unresponsive.

---

## Impact
This bug affects the Product Detail Page — a key conversion touchpoint in the e-commerce journey. Brand video content on PDPs is used to drive purchase decisions, particularly for premium fragrance products. A broken Play button means users cannot engage with this content, which directly undermines the product storytelling experience and may negatively impact conversion rates on affected product pages. With 3 community reproductions confirmed, this is not an isolated or device-specific issue.

---

## Component
Product Detail Page (PDP) — Product Information / Media

---

## Status
✅ Approved — Rated **Exceptionally Valuable**
🔧 Resolution: Resolved

---

> 📝 *This bug report is based on a real approved submission from a professional test cycle. Client and product identities, internal build details, exact URLs, and platform-specific identifiers have been redacted in compliance with NDA obligations. The documentation format, structure, and write-up are entirely my own work.*
