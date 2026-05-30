# Human/AI Task Split Assessment

## Executive Summary

| Metric | Value |
|---|---|
| **Workflow Name** | [Name of workflow being analyzed] |
| **Current Annual Volume** | [# cases/year] |
| **Current Manual Touch Time** | [# minutes per case] |
| **Annual Manual Cost (L06)** | EUR [amount]/year |
| **AI Time-Saving Opportunity** | [% of cycle time that can be automated] |
| **Expected Annual Value** | EUR [time_saved - approval_overhead - risk_cost]/year |
| **Key Decision Gates** | [# of approval gates required] |
| **Approval Overhead (net)** | EUR [amount]/year |
| **Failure-Mode Risk Level** | [LOW / MEDIUM / HIGH] |
| **Recommendation** | [IMPLEMENT / IMPLEMENT_WITH_CONTROLS / PILOT_FIRST / NOT_RECOMMENDED] |

---

## Part 1: Workflow Overview

### Current Process

**Process name:** [Workflow name]

**Primary business impact:** [e.g., "Invoice approval cycle time", "Support escalation rate", "Reporting revision cycles"]

**Baseline friction cost (from L06):** EUR [amount]/year

**Baseline lead time (from L07):** [# days average] with [#] days in queue

**Bottleneck node (from L08):** [Node name], betweenness centrality [#.##]

**Current pain points:**
1. [Pain point 1]
2. [Pain point 2]
3. [Pain point 3]

---

## Part 2: AI Task-Split Matrix

### All Tasks in Workflow

Define each task that can be performed by AI or human:

| Task # | Task Name | AI Capability | AI Reads | AI Writes | Human Gate | Decision Right | Approval Time (min) | Failure Mode | Mitigation |
|---|---|---|---|---|---|---|---|---|---|
| 1 | [Task name] | [Retrieve/Summarize/Extract/Classify/Draft/Compare/Recommend/Prepare] | [Data sources AI accesses] | [Output AI produces] | [Yes/No] | [AUTOMATED/SUPERVISED/APPROVED/HUMAN_DECIDES] | [# min] | [What can go wrong] | [How we prevent/recover] |
| 2 | ... | ... | ... | ... | ... | ... | ... | ... | ... |

**Totals:**
- AUTOMATED tasks: [#] ([%] of workflow)
- SUPERVISED tasks: [#] ([%] of workflow)
- APPROVED tasks: [#] ([%] of workflow)
- HUMAN_DECIDES tasks: [#] ([%] of workflow)

---

## Part 3: Decision-Rights Classification

### Rationale for Each Classification

For each APPROVED or HUMAN_DECIDES task, explain **why** human approval is necessary:

**Task: [Task name]**
- **Decision Right:** [APPROVED / HUMAN_DECIDES]
- **Frequency:** [# per year]
- **Reversibility:** [Reversible / Irreversible]
- **Consequence Severity:** [1-5, where 1=low, 5=critical]
- **Human Gate Rule:** 
  - If [condition], then [human action required]
  - If confidence < [threshold], then [escalation path]
  - If [exception type], then [human decides]

**Example:**

**Task: Compare PO vs Invoice (Invoice workflow)**
- **Decision Right:** APPROVED
- **Frequency:** 4,200/year
- **Reversibility:** Reversible (can correct within 24 hours)
- **Consequence Severity:** 3 (financial discrepancy)
- **Human Gate Rule:** 
  - If variance > 5%, analyst must review and approve before payment
  - If variance is within acceptable range (2-3%), auto-approve
  - If variance > 20%, escalate to manager for manual investigation

---

## Part 4: Failure-Mode Register

### Seven AI Failure Modes

For each failure mode, assess **likelihood** and **impact** in this workflow:

| Failure Mode | Definition | Risk Level | Likelihood | Impact | Control Point |
|---|---|---|---|---|---|
| **Hallucination** | AI generates false information (e.g., wrong amount) | [LOW/MED/HIGH] | [RARE/LIKELY/CERTAIN] | [Financial/Operational/Governance] | [Gate that prevents this] |
| **Context Drift** | AI uses outdated rules or policies | [LOW/MED/HIGH] | [RARE/LIKELY/CERTAIN] | [Financial/Operational/Governance] | [Gate that prevents this] |
| **Data Poisoning** | Corrupted input data leads to wrong output | [LOW/MED/HIGH] | [RARE/LIKELY/CERTAIN] | [Financial/Operational/Governance] | [Gate that prevents this] |
| **Permission Escalation** | AI escalates task above required threshold | [LOW/MED/HIGH] | [RARE/LIKELY/CERTAIN] | [Financial/Operational/Governance] | [Gate that prevents this] |
| **Audit Loss** | Critical decision is not logged or logged incorrectly | [LOW/MED/HIGH] | [RARE/LIKELY/CERTAIN] | [Financial/Operational/Governance] | [Gate that prevents this] |
| **Cascading Error** | One AI mistake triggers downstream failures | [LOW/MED/HIGH] | [RARE/LIKELY/CERTAIN] | [Financial/Operational/Governance] | [Gate that prevents this] |
| **User Override** | Human bypasses AI gate without justification | [LOW/MED/HIGH] | [RARE/LIKELY/CERTAIN] | [Financial/Operational/Governance] | [Gate that prevents this] |

**Example (Invoice workflow):**

| Failure Mode | Definition | Risk Level | Likelihood | Impact | Control Point |
|---|---|---|---|---|---|
| **Hallucination** | OCR misreads invoice amount (EUR 1,000 as EUR 10,000) | HIGH | LIKELY (if OCR conf < 95%) | Financial (payment error) | Analyst spot-checks extracted fields before processing (5% sample monthly) |
| **Data Poisoning** | Duplicate invoice in system (AI flags but analyst misses) | MEDIUM | LIKELY | Financial (duplicate payment) | Duplicate-check confidence threshold: if conf < 0.80, require manual verification |

---

## Part 5: Control Points and Approval Gates

### Critical Decision Gates

Map each control point where AI hands off to human, or where human can override:

**Control Point #1: [Name]**
- **Which tasks go through this gate:** [Task A, Task B, Task C]
- **Approval rule:** [If X, then Y happens; if Z, then escalate to A]
- **Approver role:** [Analyst / Manager / Security Officer / etc.]
- **Approval time (typical):** [# minutes]
- **Logging requirement:** [Yes / No] → Log: [what gets logged]
- **Rollback mechanism:** [Can be undone? Within how long?]
- **Escalation path (if rejected):** [What happens if approver rejects]

**Example (Invoice workflow):**

**Control Point #1: Variance Gate**
- **Which tasks go through this gate:** Compare PO vs Invoice
- **Approval rule:** If variance > 5%, require analyst approval; if variance 2–5%, auto-approve; if variance > 20%, escalate to manager
- **Approver role:** Analyst
- **Approval time (typical):** 3–5 minutes
- **Logging requirement:** Yes → Log: variance %, analyst name, approval decision, timestamp
- **Rollback mechanism:** Yes, within 24 hours (invoice not yet paid)
- **Escalation path (if rejected):** Return to submitter with variance details; requester can request exception or resubmit corrected invoice

---

### Approval Gate Decision Tree

```
[AI detects variance]
  ↓
  Is variance < 2%? → YES → [AUTO-APPROVE] → Log + proceed to payment
  ↓ NO
  Is variance 2–5%? → YES → [AUTO-APPROVE] → Log + proceed to payment
  ↓ NO
  Is variance 5–20%? → YES → [ANALYST APPROVAL] → If approved, proceed; if rejected, return to submitter
  ↓ NO
  Variance > 20%? → YES → [MANAGER ESCALATION] → Manager investigates; proceed only if approved
```

---

## Part 6: Value Quantification

### Cost-Benefit Model

| Component | Value | Notes |
|---|---|---|
| **Current Annual Friction Cost** | EUR [X]/year | From L06 analysis |
| **Annual Volume** | [# cases/year] | |
| **Manual Time per Case** | [# minutes] | Baseline from L07 |
| | | **AI AUTOMATION** |
| **Time Saved per Case (AI automates)** | [# minutes] | Automated + supervised tasks |
| **% of Cycle Time Saved** | [X%] | (Time saved / Manual time) × 100 |
| **Annual Time Saved (value)** | EUR [Y]/year | (Annual volume) × (Time saved min) / 60 × (loaded hourly rate) |
| | | **APPROVAL OVERHEAD** |
| **Approval Time per Case (humans reviewing AI decisions)** | [# minutes] | Sum of APPROVED task times |
| **Annual Approval Overhead (cost)** | EUR [Z]/year | (Annual volume) × (Approval time min) / 60 × (loaded hourly rate) |
| | | **RISK MITIGATION** |
| **Logging Infrastructure Cost** | EUR [A]/year | Database, audit trail maintenance |
| **Model Monitoring & Retraining** | EUR [B]/year | Detect drift, retrain monthly |
| **Compliance Review (periodic)** | EUR [C]/year | Quarterly audit sampling |
| **Total Risk Mitigation Cost** | EUR [D]/year | A + B + C |
| | | **NET VALUE** |
| **Net Annual Benefit** | EUR [Y - Z - D]/year | Time saved minus overhead minus risk |
| **Annual ROI** | [%] | (Net benefit) / (Implementation cost) × 100 |
| **Payback Period** | [# months] | (Implementation cost) / (Monthly net benefit) |

**Example (Invoice workflow):**

| Component | Value | Notes |
|---|---|---|
| Current Annual Friction Cost | EUR 1,294,000 | 4,200 invoices × EUR 308 friction per invoice |
| Annual Volume | 4,200 cases/year | |
| Manual Time per Case | 30 minutes | Current baseline |
| | | **AI AUTOMATION** |
| Time Saved per Case | 21 minutes | OCR (auto), classification (auto), duplicate check (supervised), routing (auto) |
| % of Cycle Time Saved | 70% | (21 / 30) × 100 |
| Annual Time Saved (value) | EUR 411,300 | 4,200 × (21/60) × EUR 55/hr |
| | | **APPROVAL OVERHEAD** |
| Approval Time per Case | 16 minutes | Variance check (5 min) + manager approval (8 min) + pack review (3 min) |
| Annual Approval Overhead | EUR 61,600 | 4,200 × (16/60) × EUR 55/hr |
| | | **RISK MITIGATION** |
| Logging Infrastructure Cost | EUR 1,000 | Database for decision logs |
| Model Monitoring & Retraining | EUR 800 | Monthly model quality checks |
| Compliance Review (periodic) | EUR 200 | Quarterly audit sampling |
| Total Risk Mitigation Cost | EUR 2,000 | |
| | | **NET VALUE** |
| Net Annual Benefit | EUR 347,700 | EUR 411,300 - EUR 61,600 - EUR 2,000 |
| Annual ROI | 2900% | EUR 347,700 / EUR 12,000 implementation cost |
| Payback Period | 0.4 months | EUR 12,000 / (EUR 347,700 / 12) |

---

## Part 7: Governance & Compliance

### Audit & Regulatory Requirements

**Applicable frameworks:**
- [ ] SOX (financial transaction controls) — **Required if:** Payment, discount, amount change
- [ ] GDPR (data privacy) — **Required if:** Customer personal data in workflow
- [ ] ISO 27001 (access control) — **Required if:** Permission-related decisions
- [ ] Internal Control Framework — **Always required**

### Logging & Auditability

**Every decision must log:**
1. **Timestamp** — When decision was made (ISO 8601)
2. **Decision maker** — Who made decision (AI system name or human user ID)
3. **Decision type** — [AUTOMATED / APPROVED / ESCALATED / OVERRIDDEN]
4. **Input data** — What information was used to decide
5. **Decision outcome** — Route approved / Escalated to manager / Returned for correction
6. **Confidence/Reason** — AI confidence score (if AI decision) or human reason (if human decision)
7. **Approver ID** — If human approval was required, who signed off
8. **Audit trail** — Immutable log entry; cannot be edited post-facto

**Example log entry (Invoice):**
```
{
  "timestamp": "2026-05-30T14:32:18Z",
  "workflow": "invoice_approval",
  "task": "variance_check",
  "decision_type": "APPROVED",
  "input": {"po_amount": "EUR 10,250", "invoice_amount": "EUR 10,000", "variance_pct": "2.4%"},
  "decision": "auto_approve",
  "confidence": 0.94,
  "approver_id": "SYSTEM_VARIANCE_GATE",
  "timestamp_logged": "2026-05-30T14:32:20Z",
  "audit_status": "immutable"
}
```

---

## Part 8: PE Investment Committee Summary

### One-Page Recommendation Memo

**TO:** Investment Committee  
**FROM:** [Portfolio Company Transformation Team]  
**RE:** AI Task-Split Implementation: [Workflow Name]  
**DATE:** [Date]  

---

**SITUATION**

[Workflow Name] processes [# cases/year] with [# minutes] manual touch per case, costing EUR [friction cost]/year in friction (L06 analysis). Bottleneck node [node name] (betweenness centrality [#.##]) delays [% of cases] by [# hours average] (L08 graph analysis). Opportunity score [#/100] (L11 assessment).

**FRICTION OBSERVED**

| Source | Impact | Cause |
|---|---|---|
| Manual data entry | EUR [X] lost annually | Invoices must be manually entered; OCR not trusted without human verification |
| Rework loop | EUR [Y] lost annually | 5% of invoices returned for correction; back-and-forth adds 3 days to cycle |
| Manager bottleneck | EUR [Z] lost annually | Manager approval gate; 20 h average wait; 2% of cases need escalation |
| **Total** | **EUR [Total]** | |

**AI OPPORTUNITY**

Deploy AI task-split framework with [# AUTOMATED + # APPROVED + # SUPERVISED] task structure:

- **AUTOMATED tasks** (no human gate): OCR extraction, vendor classification, duplicate detection, routing → Save [# minutes] per case
- **APPROVED tasks** (human gates): Variance check, manager approval, pack assembly → Approval overhead [# minutes] per case
- **SUPERVISED tasks** (human spot-check): Analyst reviews 1% sample monthly for drift detection
- **Result:** EUR [net annual value] expected run-rate savings in Year 1

**HUMAN/AI GOVERNANCE**

Human gates protect value:
- **Variance approval gate:** If PO-to-invoice variance > 5%, analyst must review (prevents EUR [X] payment errors)
- **Manager escalation gate:** If amount > EUR 10k, manager approves (maintains authorization control)
- **Audit logging:** Every decision logged with timestamp, approver, confidence score (supports SOX compliance)
- **Rollback mechanism:** Any auto-approved invoice can be recalled within 24 hours if issue detected

Control points ensure: (1) No AI decision is irreversible, (2) Every decision is logged for audit, (3) Approvers have full visibility into AI confidence + reasoning.

**EXPECTED EBITDA IMPACT**

- **Year 1 run-rate savings:** EUR [net annual value]
- **Implementation cost:** EUR [cost] (training, system integration, 2 months analyst time for tuning)
- **Payback:** [# months]
- **3-year cumulative value:** EUR [3 × run-rate]
- **Confidence level:** [HIGH / MEDIUM / LOW] — Justified by [reason]

**RISKS & MITIGATIONS**

| Risk | Likelihood | Impact | Mitigation |
|---|---|---|---|
| False positive (variance gate flags legitimate variance) | MEDIUM | Operational (delayed payment) | Analyst reviews; manager override available within 2 hours |
| Approval overhead > time savings | LOW | Negative ROI | Approval times monitored monthly; streamline if >20% of saved time |
| Audit gap (decision not logged) | VERY LOW | Compliance violation | Immutable database logs; quarterly audit sample; 100% compliance target |
| User override without justification | MEDIUM | Control degradation | Override logged + flagged for compliance review; monthly audit of overrides |

**RECOMMENDATION**

✓ **APPROVE IMPLEMENTATION**

Begin with 2-month pilot on [sample size] invoices (representing [% of annual volume]), targeting:
- Zero audit findings in transaction logs
- < 5% manager override rate
- Measurable time savings (capture timestamps)
- Team feedback on usability

Gate to full rollout (4,200 invoices/year): Pilot demonstrates [specific KPI] and zero fraud incidents.

---

## Part 9: Detailed Task Profiles

### Task-By-Task Implementation Guidance

For each APPROVED task, define:

**Task: [Task Name]**

**What it does:**  
[Description of the task]

**Current process (manual):**  
[How it's done today; who does it; how long it takes]

**AI contribution:**  
[What AI reads and analyzes]

**Human approval requirement:**  
- **Approval rule:** [If X, then Y]
- **Approver role:** [Who must approve]
- **Approval checklist:** [What approver looks for]
- **Confidence threshold:** [If AI confidence < [#], require manual review]

**Failure modes & controls:**  
| Failure | Cause | Detection | Recovery |
|---|---|---|---|
| [Mode] | [Why it happens] | [How we know it happened] | [How we fix it] |

**Audit logging:**
- **Log entry structure:** [What gets logged]
- **Retention period:** [How long do we keep logs]
- **Audit frequency:** [When do we review logs]

---

### Example: Invoice Variance Check

**Task: Compare PO vs Invoice**

**What it does:**  
Compare purchase order amount to invoice amount; flag if discrepancy > threshold; route decision to analyst

**Current process (manual):**  
Analyst manually looks up PO from system, compares to invoice amount, calculates variance %, and decides whether to flag for manager or approve. Takes 5–8 minutes per invoice; error rate ~2% (misses real discrepancies or flags false positives).

**AI contribution:**  
- AI reads: PO data from ERP, invoice amount, vendor historical pricing
- AI analyzes: Variance percentage, probability of error, historical variance pattern for this vendor
- AI outputs: Variance %, confidence score (0.0–1.0), recommendation (auto-approve / escalate to analyst / escalate to manager)

**Human approval requirement:**  
- **Approval rule:**  
  - If variance < 2% AND confidence > 0.95 → AUTO-APPROVE
  - If variance 2–5% → AUTO-APPROVE (within tolerance)
  - If variance 5–10% AND confidence > 0.85 → ANALYST REVIEWS (can approve or reject)
  - If variance 5–10% AND confidence ≤ 0.85 → MANAGER REVIEWS (required approval)
  - If variance > 10% → MANAGER + PROCUREMENT REVIEWS (dual approval)
- **Approver role:** Analyst (routine), Manager (escalation), Procurement (high variance)
- **Approval checklist:**  
  - Does the variance make sense given order? (customer order vs supplier shipment discrepancy?)
  - Is there a prior dispute history with this vendor?
  - Is this a recurring pattern or one-time variance?
  - If approved, is the payment timeline acceptable?
- **Confidence threshold:** If AI confidence < 0.80, require human review (do not auto-approve)

**Failure modes & controls:**

| Failure | Cause | Detection | Recovery |
|---|---|---|---|
| **False negative (miss real discrepancy)** | AI confidence too high; invoice fraud | Payment processed incorrectly; discovered in reconciliation | Audit sampling catches error within 30 days; reverse payment + interest recovery attempt |
| **False positive (flag legitimate variance)** | Approved change orders not in AI training data | Analyst sees legitimate reason during review | Approve and add change order to training data; retrain model |
| **Confidence miscalibration** | Model drift (new vendor type not in training set) | Analyst overrides AI decision > 5% of cases | Monthly model quality review; trigger retraining if drift detected |

**Audit logging:**
- **Log entry structure:** timestamp, invoice_id, po_amount, invoice_amount, variance_%, ai_confidence, approval_decision, approver_id, approver_role, approval_timestamp
- **Retention period:** 7 years (SOX requirement)
- **Audit frequency:** Monthly automated check for anomalies (e.g., override rate > 10%); quarterly manual sample audit (5% of decisions)

---

## Implementation Timeline

| Phase | Duration | Key Deliverables | Success Criteria |
|---|---|---|---|
| **Phase 1: Design & Pilots** | Weeks 1–4 | Finalize task-split matrix; train team on gates; run 100-case pilot | Zero audit findings; time savings > [X]% |
| **Phase 2: Soft Launch** | Weeks 5–8 | Deploy to [50%] of volume; monitor error rates & approval times | Approval overhead < [X]% of saved time; user satisfaction > [X]% |
| **Phase 3: Full Rollout** | Weeks 9–12 | Deploy to 100% of volume; establish monitoring dashboard | Operational targets met; audit compliance 100% |
| **Phase 4: Optimization** | Weeks 13+ | Monitor model drift; refine approval thresholds; plan next workflow | Continuous improvement feedback loop |

---

## Next Steps

1. **Week 1:** Schedule approval meeting with CFO, COO, and Compliance Officer
2. **Week 2:** Conduct risk assessment workshop (identify failure modes specific to this company)
3. **Week 3:** Build pilot dataset (100–200 representative cases)
4. **Week 4:** Train team on approval gates and audit logging
5. **Week 5:** Launch pilot; monitor closely; adjust thresholds as needed
6. **Week 9:** Go/no-go decision on full rollout

**Sponsor:** [Name, Title]  
**Project Manager:** [Name, Title]  
**Legal/Compliance Lead:** [Name, Title]  
**Target Launch Date:** [Date]
