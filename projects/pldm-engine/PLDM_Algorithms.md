# PLDM Engine — Algorithms  
**Author:** Dennis T.Y. Leo  
**Project Path:** `/projects/pldm-engine/`

---

## 1. Definitions

- **Profit (P)**  
  Measurable positive outcome created by the system  
  e.g. revenue, uptime value, SLA achievement, saved cost

- **Liability (L)**  
  Accumulated risk, degradation, or future cost  
  e.g. unresolved incidents, technical debt, unstable components

- **Dividend (D)**  
  Realized gain from reducing Liability while protecting Profit  
  e.g. improved MTBF, reduced incident count, higher customer retention

- **Management (M)**  
  The control plane that assigns work, sets priorities, and enforces actions

---

## 2. Basic PLDM Loop

At each evaluation cycle *t*:

1. Collect signals from XR-Series and business systems  
2. Compute current Profit `P(t)`  
3. Compute current Liability `L(t)`  
4. Estimate possible Dividend `D(t)` from resolving parts of `L(t)`  
5. Generate Management actions `M(t)` to realize `D(t)`  

Informally:

> **M(t)** = function of **P(t), L(t), D(t)**

---

## 3. Example Scoring Model (Conceptual)

- Each incident or failure from XRAD / XRST is assigned:  
  - **ImpactWeight** (business impact)  
  - **FrequencyWeight** (how often it occurs)  
  - **LatencyWeight** (time to detect / fix)

- Liability Score:

  ```text
  L(t) = Σ [ImpactWeight × FrequencyWeight × LatencyWeight]
