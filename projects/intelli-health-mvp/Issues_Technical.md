# Technical Issues — Intelli-Health MVP Evaluation  
**Author:** Dennis T.Y. Leo  
**Date:** 2025  
**Project Path:** `/projects/intelli-health-mvp/`

---

## Overview

A total of **9 technical issues** were identified during the MVP evaluation. These issues limit system stability, AI consistency, integration readiness, and user flow reliability. Addressing them is essential for reaching TRL 6 (pilot-ready).

---

## 1. Unstable AI Inference Output
- The AI engine produces different outputs even when the same inputs are provided.  
- No deterministic mode or reproducibility constraints.  
- **Impact:** Low trust from users; unpredictable quality.  
- **Recommendation:** Implement deterministic inference mode, input normalization, and enforced reproducibility controls.

---

## 2. Missing Evidence Traceability  
- The system provides results without a transparent explanation path.  
- No feature attribution or evidence linking for clinical reasoning.  
- **Impact:** Not suitable for healthcare environments requiring auditability.  
- **Recommendation:** Add traceable vector logs, model explainability, and reasoning-output linkage.

---

## 3. Workflow State Inconsistency  
- Navigating between screens causes loss of input data or context.  
- Some transitions reset internal variables unexpectedly.  
- **Impact:** Users get confused; results may not match expectations.  
- **Recommendation:** Implement centralize
