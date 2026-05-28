# Workflow Cost Model Template

**Lesson 02 Deliverable**

## Learner Information

**Name:** _________________________  
**Date:** _________________________  
**Workflow:** _________________________

---

## Instructions

For each workflow, calculate the complete cost model including:
1. **Base cost** — Volume × (Touch Time ÷ 60) × Hourly Cost
2. **Rework cost** — Volume × Rework Rate × (Touch Time ÷ 60) × Hourly Cost  
3. **Escalation cost** — Volume × Escalation Rate × (Escalation Time ÷ 60) × Escalation Hourly Cost
4. **Total cost of friction** — Base + Rework + Escalation
5. **Cost per transaction** — Total ÷ Volume

---

## Completed Examples (from Lesson 02)

### Example 1: Invoice Approval

**Metrics:**
- Annual volume: 4,200 invoices
- Touch time: 12 minutes per invoice
- Rework rate: 5% (missing fields, amount mismatches)
- Escalation rate: 2% (complex → manager approval)
- AP Analyst cost: €55/hr
- AP Manager cost: €75/hr

**Calculation:**
- Base cost: 4,200 × (12 ÷ 60) × €55 = €4,620
- Rework cost: 4,200 × 0.05 × (12 ÷ 60) × €55 = €231
- Escalation cost: 4,200 × 0.02 × (12 ÷ 60) × €75 = €77
- **Total Cost: €4,928/year**
- **Cost per invoice: €1.17**

**AI Impact:** 50% touch time reduction, 80% rework reduction, 80% escalation reduction
- **New cost: €2,800/year**
- **Savings: €2,128/year (43%)**

---

### Example 2: Support Ticket Triage

**Metrics:**
- Annual volume: 18,000 tickets
- Touch time: 14 minutes per ticket
- Rework rate: 8% (misrouted)
- Escalation rate: 15% (complex → specialist, 30 min)
- L1 Analyst cost: €55/hr
- L2 Specialist cost: €75/hr

**Calculation:**
- Base cost: 18,000 × (14 ÷ 60) × €55 = €9,240
- Rework cost: 18,000 × 0.08 × (14 ÷ 60) × €55 = €1,749
- Escalation cost: 18,000 × 0.15 × (30 ÷ 60) × €75 = €4,725
- **Total Cost: €15,714/year**
- **Cost per ticket: €0.87**

**AI Impact:** 45% touch time reduction, 90% rework reduction, 85% escalation reduction
- **New cost: €8,286/year**
- **Savings: €7,428/year (47%)**

---

### Example 3: Management Reporting

**Metrics:**
- Annual volume: 52 reports (weekly)
- Touch time: 180 minutes per report
- Rework rate: 30% (revisions after review)
- Escalation rate: 5% (executive director review)
- Finance Manager cost: €45/hr
- Executive Director cost: €90/hr

**Calculation:**
- Base cost: 52 × (180 ÷ 60) × €45 = €5,850
- Rework cost: 52 × 0.30 × (180 ÷ 60) × €45 = €1,755
- Escalation cost: 52 × 0.05 × (180 ÷ 60) × €90 = €1,462
- **Total Cost: €9,067/year**
- **Cost per report: €174.37**

**AI Impact:** 60% touch time reduction, 90% rework reduction, 70% escalation reduction
- **New cost: €3,627/year**
- **Savings: €5,440/year (60%)**

---

## Your Answers: Build 3 Cost Models

### 1. Your Chosen Workflow

**Workflow Name:** _____________________________________________________

**Metrics:**
- Annual volume: ____________
- Touch time: ____________ minutes per transaction
- Rework rate: ____________ % (describe why)
- Escalation rate: ____________ % (describe escalation resource)
- Base hourly cost: €____________ /hr (what role?)
- Escalation hourly cost: €____________ /hr (what role?)
- Escalation time (if different): ____________ minutes

**Your Calculations:**
```
Base cost = __________ × (__________ ÷ 60) × €__________ = €__________

Rework cost = __________ × __________ × (__________ ÷ 60) × €__________ = €__________

Escalation cost = __________ × __________ × (__________ ÷ 60) × €__________ = €__________

TOTAL COST = €__________ + €__________ + €__________ = €__________

Cost per transaction = €__________ ÷ __________ = €__________
```

**Verification:**
- [ ] All metrics are realistic for this workflow
- [ ] Calculations are mathematically correct
- [ ] Total cost makes sense relative to baseline (Lesson 01)
- [ ] Cost per transaction is in reasonable range

---

### 2. Bonus: Estimate AI Impact

**AI Improvements:**
- Touch time reduction: _______ %
- Rework reduction: _______ %
- Escalation reduction: _______ %
- AI platform cost: €____________ per transaction

**New Cost Calculation:**
```
New touch time = __________ × (1 - ________) = __________ min
New rework rate = __________ × (1 - ________) = __________
New escalation rate = __________ × (1 - ________) = __________

Recalculate base + rework + escalation with new rates:

New base cost = €__________
New rework cost = €__________
New escalation cost = €__________
AI platform cost = €__________
TOTAL NEW COST = €__________

Annual Savings = €__________ - €__________ = €__________
Percentage Savings = _______ %
```

---

### 3. Sensitivity: What If?

Pick ONE assumption that could change and show impact:

**Assumption Change:**
```
Base case: __________
What if: __________

New total cost: €__________
Change from base: €__________ (__________%)
```

**Business implication:**
_________________________________________________________________
_________________________________________________________________

---

## Completion Checklist

To pass Lesson 02, you must demonstrate:

- [ ] I calculated base cost + rework cost + escalation cost for at least one workflow
- [ ] My total cost matches the formula: Volume × Time ÷ 60 × Cost + Rework + Escalation
- [ ] I correctly identified which resources have different hourly costs (analyst vs manager vs specialist)
- [ ] I estimated realistic rework and escalation rates (not pulled from thin air)
- [ ] I ran a sensitivity check showing how cost changes with different assumptions
- [ ] I can explain why €45k/year salary = €55/hour loaded cost (5+ factors)

---

## Extensions

If you want to go deeper:

1. **Queue time modeling:** How long does work wait before being processed? Add this to cycle time.
2. **Error cost quantification:** What's the downstream cost when someone makes a mistake? (rework + customer impact)
3. **Capacity release calculation:** If AI frees 45% of time, can that team handle new volume? Calculate freed headcount value.
4. **Bottleneck identification:** Which step in the workflow is the most costly? Where should AI intervention focus?

---

## Next: Lesson 03 — EBITDA Basics and the EBITDA Bridge

Once you master cost models, you'll learn how to:
1. Convert cost savings into EBITDA impact
2. Build EBITDA bridges showing "before" → "after"
3. Calculate enterprise value impact (EBITDA × Multiple)

🚀 Ready for Lesson 03?
