# Investment Decision Template

**Lesson 04 Deliverable**

## Learner Information

**Name:** _________________________  
**Date:** _________________________  
**Workflow(s):** _________________________

---

## Instructions

For this exercise, you will build a complete investment case for an AI workflow, including payback period, ROI, NPV, and a go/no-go recommendation.

**Steps:**
1. Define one workflow (from Lesson 02 or your own)
2. Estimate implementation cost (one-time)
3. Identify annual net benefit (from Lesson 03)
4. Calculate: Payback, ROI, NPV
5. Assess execution risk with confidence adjustment
6. Make recommendation using decision framework

---

## Completed Example 1: Support Triage (from Lesson 04)

### Workflow Profile

| Metric | Value |
|--------|-------|
| Workflow | Support Ticket Triage |
| Current annual cost | €35,073 |
| AI savings (conservative) | €11,751 |
| AI platform cost | €900 |
| Support/maintenance | €800 |
| Quality risk buffer | €300 |
| **Net annual benefit** | **€9,751** |

### Implementation Estimate

| Cost Category | Amount |
|---------------|--------|
| AI model development/training | €12,000 |
| Ticketing system integration | €8,000 |
| Staff training | €5,000 |
| Testing & validation | €3,000 |
| **Total implementation cost** | **€28,000** |

### Investment Metrics Calculation

```
Payback Period (months):
= Implementation Cost ÷ (Annual Benefit ÷ 12)
= €28,000 ÷ (€9,751 ÷ 12)
= €28,000 ÷ €812.58
= 34.4 months ≈ 2.9 years

ROI (%):
= (Annual Benefit ÷ Implementation Cost) × 100
= (€9,751 ÷ €28,000) × 100
= 34.8%

NPV (5-year, 10% discount rate):
Year 1: €9,751 ÷ 1.10¹ = €8,864
Year 2: €9,751 ÷ 1.10² = €8,058
Year 3: €9,751 ÷ 1.10³ = €7,326
Year 4: €9,751 ÷ 1.10⁴ = €6,660
Year 5: €9,751 ÷ 1.10⁵ = €6,054
Total PV = €36,962
NPV = €36,962 - €28,000 = €8,962
```

### Assessment Against Decision Framework

| Criterion | Assessment | Threshold | Result |
|-----------|------------|-----------|--------|
| Payback < 24 months? | 34.4 months | < 24 mo preferred | ✗ Moderate |
| Payback < 36 months? | 34.4 months | < 36 mo acceptable | ✓ Pass |
| ROI > 20%? | 34.8% | > 20% hurdle | ✓ Exceeds |
| NPV > 0? | €8,962 | > €0 | ✓ Positive |

### Confidence Adjustment

```
Risk Factors:
• Adoption rate: 85% (users learn to trust AI routing)
• AI accuracy: 90% (model works well, some edge cases)
• Execution: 95% (integration straightforward)

Combined confidence: 0.85 × 0.90 × 0.95 = 0.727 ≈ 73%

Adjusted ROI: 34.8% × 73% = 25.4%
Adjusted NPV: €8,962 × 73% = €6,542
```

### Recommendation

**✓ BUILD THIS WORKFLOW**

**Rationale:**
- Payback 2.9 years is acceptable (< 36 months threshold)
- ROI 34.8% significantly exceeds 20% hurdle rate
- NPV €8,962 is solidly positive
- Even with 73% confidence adjustment, adjusted ROI 25.4% remains strong
- This workflow alone justifies implementation; bundling with others increases value

**Key Success Factors:**
- Strong change management (help teams trust AI routing)
- Iterative model improvement (feedback loop to increase accuracy)
- Early wins communication (show high-quality routings early)

---

## Completed Example 2: Multi-Workflow Portfolio

### Bundled Case: All 3 Workflows

| Workflow | Annual Benefit |
|----------|-----------------|
| Invoice Approval | €1,702 |
| Support Triage | €9,751 |
| Management Reporting | €3,860 |
| **Total** | **€15,313** |

| Cost Category | Amount |
|---------------|--------|
| Invoice development | €15,000 |
| Support integration | €28,000 |
| Reporting automation | €12,000 |
| **Total implementation** | **€55,000** |

### Investment Metrics

```
Payback: €55,000 ÷ (€15,313 ÷ 12) = 43.0 months ≈ 3.6 years
ROI: (€15,313 ÷ €55,000) × 100 = 27.8%
NPV (5-year @ 10%): €11,872
```

### Assessment

| Criterion | Value | Status |
|-----------|-------|--------|
| Payback < 36 months? | 43 months | ✗ Slightly over |
| ROI > 20%? | 27.8% | ✓ Exceeds |
| NPV > 0? | €11,872 | ✓ Strong |
| Confidence-adjusted ROI | 20.3% | ✓ Marginal but acceptable |

### Recommendation

**✓ BUILD (with strategic consideration)**

**Notes:**
- Payback slightly exceeds 36-month preferred threshold (43 months)
- However, ROI 27.8% is strong and justifies the wait
- Portfolio approach (3 workflows) provides risk diversification
- Shared infrastructure (ticketing platform, data pipeline) creates economies
- Consider phased rollout to compress timeline

**Phased Approach (Alternative):**
- **Phase 1 (Q1):** Support Triage alone (payback 34 months, ROI 35%)
- **Phase 2 (Q2):** Add Invoice + Reporting (incremental ROI calculation)
- **Result:** Faster initial payback, proven success before full rollout

---

## Your Turn: Build an Investment Case

### Step 1: Define Your Workflow

**Workflow Name:** _________________________________________________________

**Description:** ___________________________________________________________

---

### Step 2: Cost & Benefit Estimates

#### Current State Cost (from Lesson 02)

| Metric | Value |
|--------|-------|
| Annual volume | ________________ |
| Touch time per case | ________________ min |
| Current annual cost | €________________ |

#### AI Improvement & Benefits

| Metric | Value |
|--------|-------|
| Touch time reduction | ________ % |
| Rework reduction | ________ % |
| Estimated AI savings | €________________ |
| AI platform cost | €________________ |
| Support/maintenance | €________________ |
| Quality risk buffer | €________________ |
| **Net annual benefit** | **€________________** |

#### Implementation Cost Estimate

| Category | Amount |
|----------|--------|
| Development/training | €________________ |
| Integration | €________________ |
| Testing | €________________ |
| Change management | €________________ |
| **Total** | **€________________** |

---

### Step 3: Calculate Investment Metrics

#### Payback Period (months)

```
Payback = Implementation Cost ÷ (Annual Benefit ÷ 12)
        = €________________ ÷ (€________________ ÷ 12)
        = €________________ ÷ €________________
        = ________________ months
```

**Assessment:** 
- ✓ < 24 months (excellent) 
- ✓ 24-36 months (acceptable)
- ✗ > 36 months (too long)

#### ROI (%)

```
ROI = (Annual Benefit ÷ Implementation Cost) × 100
    = (€________________ ÷ €________________) × 100
    = ________________ %
```

**Assessment:** 
- ✓ > 20% (meets hurdle rate)
- ✗ < 20% (below hurdle)

#### NPV (5-year, 10% discount rate)

```
Year 1: €________________ ÷ 1.10¹ = €________________
Year 2: €________________ ÷ 1.10² = €________________
Year 3: €________________ ÷ 1.10³ = €________________
Year 4: €________________ ÷ 1.10⁴ = €________________
Year 5: €________________ ÷ 1.10⁵ = €________________
─────────────────────────────────────
Total PV (sum above) = €________________

NPV = Total PV - Implementation Cost
    = €________________ - €________________
    = €________________
```

**Assessment:** 
- ✓ > 0 (creates value)
- ✗ < 0 (destroys value)

---

### Step 4: Confidence Adjustment

#### Risk Factors

| Factor | Confidence | Reasoning |
|--------|-----------|-----------|
| Adoption rate | _____% | (How readily will users adopt?) |
| AI accuracy | _____% | (How well will model work in production?) |
| Execution | _____% | (Can we stay on time/budget?) |
| **Combined** | **_____% ** | (Product of above) |

#### Adjusted Returns

```
Confidence-adjusted ROI = ____%  × ____% = ____%
Confidence-adjusted NPV = €_____ × ____% = €_____
```

---

### Step 5: Decision & Recommendation

#### Decision Framework Check

```
Payback < 24 months? [YES / NO]
  └─ ROI > 20%? [YES / NO]
      └─ Recommendation: ________________

Payback 24-36 months? [YES / NO]
  └─ ROI > 25%? [YES / NO]
      └─ Recommendation: ________________

Payback > 36 months? [YES / NO]
  └─ Recommendation: SKIP
```

#### Final Recommendation

**GO / NO-GO / MAYBE**

**Rationale:** 

_________________________________________________________________

_________________________________________________________________

_________________________________________________________________

**Key Success Factors:**

1. _________________________________________________________________
2. _________________________________________________________________
3. _________________________________________________________________

**Risks & Mitigation:**

| Risk | Mitigation |
|------|-----------|
| | |
| | |

---

## Completion Checklist

To pass Lesson 04, you must demonstrate:

- [ ] I calculated payback, ROI, and NPV using correct formulas
- [ ] I understood why bundled workflows often make more sense than individual ones
- [ ] I adjusted returns downward for realistic confidence factors
- [ ] I ran sensitivity analysis on key cost/benefit assumptions
- [ ] I made a clear GO/NO-GO recommendation with business rationale

---

## Extensions

If you want to go deeper:

1. **Phased rollout analysis:** How does a staged implementation (Q1, Q2, Q3) affect payback?
2. **Learning curve adjustment:** Assume Year 1 = 70% benefit, ramping to 100% by Year 3. Recalculate.
3. **Build vs. buy:** Compare custom AI (high impl. cost) vs. third-party SaaS (lower upfront, higher recurring). Which has better ROI?
4. **Portfolio optimization:** You have 5 workflows. Which ones should you prioritize? (Lesson 11)
5. **Multi-year cumulative:** Show 5-year cumulative EBITDA from all workflows combined.

---

## Next: Lesson 05 — Private Equity Value Creation Playbook

Investment metrics tell you if **this one project** is worth doing.

Lesson 05 teaches how PE managers create value across **entire company portfolios**:
- 10 AI value levers (beyond just labor savings)
- Cost structure optimization
- Operating leverage and scale
- Value creation plans
- 100-day rapid transformation

🚀 Ready?
