# Integration Guide

## Overview
This guide explains how to connect TheHive, Cortex, MISP, and Shuffle in this lab.

---

## 1️⃣ Shuffle → TheHive
- Use Shuffle's TheHive app to automate case creation, updates, and closures.
- Trigger workflows based on case events or external alerts.
- Example: Automatically assign cases or add observables.

---

## 2️⃣ TheHive → Cortex
- Define analyzers in Cortex.
- Add Cortex connection settings in TheHive.
- Test observable analysis from cases.

---

## 3️⃣ Cortex → MISP
- Configure analyzers to enrich data with MISP.
- Share indicators back to MISP from Cortex.

---

## 4️⃣ Shuffle → All
- Design workflows to automate actions across all services.
- Example playbook:
  - Trigger: New case in TheHive.
  - Actions:
    - Analyze observables in Cortex.
    - Enrich with MISP.
    - Post updates back to TheHive.

---

## Tips:
- Ensure API keys are properly configured.
- Check Shuffle apps are installed and connected.
- Use logs (`docker logs <service>`) to debug any issues.

