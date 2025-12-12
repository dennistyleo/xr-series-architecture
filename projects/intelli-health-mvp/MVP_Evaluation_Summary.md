# Technical Issues — Intelli-Health MVP Evaluation  
**Author:** Dennis T.Y. Leo  
**Date:** 2025  
**Project Path:** `/projects/intelli-health-mvp/`

---

## Overview

A total of **9 technical issues** were identified during the MVP evaluation. These issues limit system stability, AI consistency, integration readiness, and user flow reliability. Addressing them is essential for reaching TRL 6 (pilot-ready).

---

## 1. Unstable AI Inference Output
- Model output changes under identical input conditions  
- No deterministic inference mode  
- *Impact:* Users cannot trust system results  
- **Recommendation:** Introduce input normalization + deterministic inference pipeline

---

## 2. Missing Evidence Traceability
- AI decisions have no linked evidence or reasoning trails  
- Cannot support medical/clinical review  
- **Recommendation:** Add structured vector logging + explainability layer

---

## 3. Workflow State Inconsistency
- Page-to-page transitions lose internal state values  
- Results mismatch with user expectations  
- **Recommendation:** Centralized workflow controller with persistent state

---

## 4. UI/UX Logic Gaps
- Buttons with unclear behavior  
- Navigation loops or dead ends  
- **Recommendation:** Rationalize UX with a unified flow map

---

## 5. Dataset Validation Gap
- MVP does not validate user inputs  
- Risk of corrupted or incompatible data entering the AI pipeline  
- **Recommendation:** Strict input schema validation

---

## 6. Missing Error Handling Framework
- No unified error message format  
- Silent failures possible  
- **Recommendation:** Introduce structured error codes + logging framework

---

## 7. API Integration Instability
- Backend endpoint behavior inconsistent  
- No versioning  
- **Recommendation:** API versioning + regression testing

---

## 8. No Testing Infrastructure
- No automated test cases  
- Manual validation only  
- **Recommendation:** Build test harness + unit/integration test coverage

---

## 9. Lack of Performance Benchmarking
- Inference latency and throughput unknown  
- Cannot predict scaling cost  
- **Recommendation:** Basic benchmarking under real workloads

---

## Summary

These technical gaps are all solvable within a structured engineering cycle. Once addressed, Intelli-Health can transition from prototype-level behavior to a stable, scalable healthcare SaaS platform.

