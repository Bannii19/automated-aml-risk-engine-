# Automated AML Risk Scoring Engine (Python) 🛡️

## 📌 Project Overview
This repository contains a light, modular Anti-Money Laundering (AML) screening engine written in Python. The system processes transaction telemetry data against multi-vector risk indicators—including value triggers, transactional velocity rules, and jurisdictional corridors—to assign a weighted risk score and automate compliance sorting.

---

## 🛠️ Operational Rules & Risk Vectors
The engine parses data using customizable logic models that mirror actual regulatory frameworks:

1. **Structuring & Threshold Detection:** Transactions matching or crossing 80% of major regulatory reporting limits (£10,000) are flagged for potential structural splitting.
2. **Velocity Analytics:** Evaluates customer transaction logs across a rolling 24-hour window to catch systemic asset churning or placement techniques.
3. **Corridor Assessment:** Automatically applies risk weights if funds move directly into highly monitored liquidity corridors (e.g., high-volume commercial nodes like USD or EUR).

---

## 💻 Technical Highlights
* **Architecture:** Object-Oriented Programming (OOP) using clean Python classes and state-dependent logic.
* **Integrations:** Designed to ingest JSON/Dictionary data schemas matching typical transaction webhooks.
* **Outputs:** Yields an actionable evaluation payload including a normalized score (0–100), explicit compliance flags, and automated action tiers (`PASS`, `ENHANCED_DUE_DILIGENCE`, or `FREEZE`).
