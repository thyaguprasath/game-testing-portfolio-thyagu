# Game QA Portfolio: Bug Reporting & Analysis
**Candidate:** M Thyagu Prasath  
**Role:** Junior QA Tester / Intern  
**Focus:** Functional, Logic, and Visual Regression Testing

## 📌 Overview
This repository contains a collection of professional bug reports for various titles, including **F1 25**, **Valorant**, **Marvel Future Fight**, and **Uncharted 4**. These reports demonstrate my ability to identify reproduction steps, analyze root causes, and provide user-side workarounds.

---

## 🏎️ Bug Report 1: F1 25 (Steam/PC)
**Title:** Gameplay / Logic — Mechanical State Regression via Flashback

* **Type:** Logic / State Persistence
* **Severity:** High
* **Summary:** A mechanical fault (e.g., DRS stuck closed) repaired in the pits returns immediately if a Flashback is used to a point after the repair.
* **System Info:** Intel i5-11300H | GTX 1650 | 16GB RAM | Report Code: `LDHL-HGX2-HZHK-LZGG`
* **Key Finding:** The flashback snapshot fails to update the `isMechanicalFaultActive` flag after a pit event.
* **Workaround:** Avoid using Flashback immediately following a pit stop repair.

---

## 🔫 Bug Report 2: Valorant (PC)
**Title:** Gameplay / Visual — Low-Poly Character Model LOD Failure

* **Type:** Visual / Asset Streaming
* **Severity:** Low
* **Summary:** Character models intermittently fail to transition from low-resolution (LOD) to high-resolution versions at close range, resulting in "melted" textures.
* **System Info:** Intel i5-11300H | GTX 1650 (Running at 82°C during occurrence)
* **Key Finding:** Asset streaming budget is likely capped or throttled due to system thermals, preventing the high-detail mesh from loading.
* **Workaround:** Enable "Multithreaded Rendering" and ensure the game is on an SSD.

---

## 🗺️ Bug Report 3: Uncharted 4 (PC)
**Title:** Gameplay / Visual — Rossi Estate Animation State Desync

* **Type:** Visual / Scripting
* **Severity:** Medium
* **Summary:** During the Chapter 6 balcony transition, character models lock into a "squat" pose instead of triggering the scripted walking animation.
* **System Info:** Industry Standard (Intel i7-4770 | GTX 1060 | 16GB RAM)
* **Key Finding:** A failure in the animation trigger logic during the transition from player-controlled "crouch" to cinematic "walk."
* **Workaround:** Pausing the game for 10 seconds allows the animation buffer to refresh.

---

## 🦸 Bug Report 4: Marvel Future Fight (Mobile)
**Title:** Gameplay / Logic — Mission #48 Reward Trigger Block

* **Type:** Logic / Progression
* **Severity:** Medium
* **Summary:** The "Agent Growth" mission does not clear if the player has exhausted their 5/5 daily World Boss entries, even if the stage is successfully cleared.
* **Key Finding:** Mission completion is tied to the `OnRewardClaimed` event rather than the `OnStageVictory` event.
* **Workaround:** Complete mission tasks before using all daily entries.

---

## 🛠️ Technical Skills Demonstrated
* **Reproduction Testing:** 100% success rate in defining clear, actionable steps.
* **Environment Logging:** Capturing hardware specs, temperatures, and unique session IDs.
* **Root Cause Analysis:** Hypothesizing on memory leaks, state deadlocks, and LOD streaming.
* **Communication:** Writing clear Expected vs. Actual results for developer hand-off.
