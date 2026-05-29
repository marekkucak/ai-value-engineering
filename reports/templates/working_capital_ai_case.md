# Working Capital AI Business Case

**Prepared by:** [Analyst Name]  
**Date:** [YYYY-MM-DD]  
**Company / Business Unit:** [Name]  
**Scope:** [Order-to-Cash / Procure-to-Pay / Both]  
**Data period:** [Q1/Q2/Q3/Q4 YYYY]

---

## 1. Executive Summary

| Item | Current State | Target State | Annual Value |
|------|--------------|-------------|-------------|
| DSO | [n] days | [n] days | EUR [n,nnn] cash released |
| Overdue AR rate | [n]% | [n]% | EUR [n,nnn] write-off saving |
| EPD capture rate | [n]% | [n]% | EUR [n,nnn] discount saving |
| DPO | [n] days | [n] days | EUR [n,nnn] cash extended |
| **Total annual value** | | | **EUR [n,nnn]** |
| Implementation cost | | | EUR [n,nnn] |
| Payback period | | | [n] months |

**Recommended first intervention:** [Name] — [one-sentence rationale]

---

## 2. Accounts Receivable Analysis

### AR Aging Profile

| Bucket | Invoice Count | Total EUR | % of AR | At-Risk EUR | Recovery % |
|--------|--------------|-----------|---------|------------|-----------|
| 0–30 days | [n] | EUR [n,nnn] | [n]% | EUR [n,nnn] | [n]% |
| 31–60 days | [n] | EUR [n,nnn] | [n]% | EUR [n,nnn] | [n]% |
| 61–90 days | [n] | EUR [n,nnn] | [n]% | EUR [n,nnn] | [n]% |
| >90 days | [n] | EUR [n,nnn] | [n]% | EUR [n,nnn] | [n]% |
| **Total** | **[n]** | **EUR [n,nnn]** | **100%** | **EUR [n,nnn]** | |

**Current DSO:** [n] days  
**Target DSO:** [n] days  
**DSO improvement:** [n] days  

**Formula:**
```
DSO = (AR balance / annual revenue) × 365
Cash released = (annual revenue / 365) × DSO_improvement_days
```

### DSO Improvement — AI Intervention

| AI Solution | Invoice Intake Assistant / [custom name] |
|-------------|----------------------------------------|
| Root cause addressed | [rework rate / escalation rate / manual routing / other] |
| Current processing time | [n] hours |
| Target processing time | [n] hours |
| Rework rate before | [n]% |
| Rework rate after | [n]% |
| Expected DSO improvement | [n] days |
| Cash released | EUR [n,nnn] |

---

## 3. Collections Prioritisation

### Current State

| Metric | Value |
|--------|-------|
| Total AR balance | EUR [n,nnn] |
| Overdue AR (>30 days) | [n]% = EUR [n,nnn] |
| Average days overdue | [n] days |
| Write-off rate (% of overdue) | [n]% |
| Annual write-off cost | EUR [n,nnn] |
| Collections FTE | [n] FTE |
| Hours per overdue invoice | [n] hours |

### Priority Scoring Model

Score each overdue invoice as:

```
priority_score = invoice_value × days_overdue × customer_risk_factor / 1000
```

| Priority Tier | Score Range | Invoices | Total EUR | Action |
|--------------|------------|---------|----------|--------|
| Critical | >2,000 | [n] | EUR [n,nnn] | Senior collector calls today |
| High | 500–2,000 | [n] | EUR [n,nnn] | Call within 48 hours |
| Medium | 100–500 | [n] | EUR [n,nnn] | Automated reminder + follow-up |
| Low | <100 | [n] | EUR [n,nnn] | Automated reminder only |

### AI Collections Agent — Expected Impact

| Metric | Before | After | Saving |
|--------|--------|-------|--------|
| Overdue rate | [n]% | [n]% | EUR [n,nnn] cash released |
| Write-off rate | [n]% | [n]% | EUR [n,nnn]/year |
| Hours per invoice | [n]h | [n]h | [n] FTE equivalent |
| Staff cost saving | | | EUR [n,nnn]/year |

---

## 4. Accounts Payable: Early Payment Discounts

### AP Spend Profile

| Vendor Tier | Count | Annual Spend | Avg Pay Day | Standard Terms | EPD Eligible |
|-------------|-------|-------------|------------|----------------|-------------|
| Strategic | [n] | EUR [n,nnn] | Day [n] | [n] days | Yes / No |
| Operational | [n] | EUR [n,nnn] | Day [n] | [n] days | Yes / No |
| Tail spend | [n] | EUR [n,nnn] | Day [n] | [n] days | Yes / No |

**Current DPO:** [n] days  
**Target DPO:** [n] days  

### Early Payment Discount (EPD) Analysis

| Metric | Value |
|--------|-------|
| Annual AP spend | EUR [n,nnn] |
| EPD-eligible spend | EUR [n,nnn] ([n]%) |
| EPD terms | [n]% / [n] days net [n] |
| Annualised ROI on EPD | ~[n]% |
| Currently captured | EUR [n,nnn]/year ([n]% of eligible) |
| Uncaptured opportunity | EUR [n,nnn]/year |
| Target capture rate | [n]% |
| Expected annual saving | EUR [n,nnn]/year |

**Formula:**
```
Annualised ROI = discount_pct / (discount_window_days / 365)
Annual EPD saving = eligible_spend × capture_rate × discount_pct
```

**AI Solution:** Payment term anomaly detector  
- Reads vendor invoice terms on ingestion  
- Flags EPD-eligible invoices and routes to fast-pay queue  
- Alerts AP team before EPD window closes  

---

## 5. Combined Working Capital Business Case

### Value Summary

| Intervention | Type | Annual Value (EUR) | One-time Cash (EUR) | Confidence |
|-------------|------|-------------------|---------------------|-----------|
| Invoice intake assistant | DSO improvement | [n,nnn] | [n,nnn] | High / Medium / Low |
| Collections prioritisation agent | Write-off + staff | [n,nnn] | [n,nnn] | High / Medium / Low |
| Payment term detector | EPD capture | [n,nnn] | 0 | High / Medium / Low |
| **Total** | | **[n,nnn]** | **[n,nnn]** | |

### Investment and Returns

| Item | Value |
|------|-------|
| Implementation cost (one-time) | EUR [n,nnn] |
| Annual recurring AI cost | EUR [n,nnn] |
| Annual net value | EUR [n,nnn] |
| ROI | [n]x ([n]%) |
| Payback period | [n] months |

**Payback formula:**
```
Payback months = implementation_cost / (annual_net_value / 12)
```

### Cash Conversion Cycle Impact

| Metric | Before | After | Change |
|--------|--------|-------|--------|
| DSO | [n] days | [n] days | −[n] days |
| DPO | [n] days | [n] days | +[n] days (EPD = pay earlier) |
| Inventory days | [n] days | [n] days | 0 (not in scope) |
| CCC | [n] days | [n] days | −[n] days |

---

## 6. Implementation Sequence

Ranked by annual value (highest first):

1. **[Intervention 1]** — EUR [n,nnn]/year
   - Implementation time: [n weeks]
   - Data required: [list]
   - Dependencies: none / [dependency]

2. **[Intervention 2]** — EUR [n,nnn]/year
   - Implementation time: [n weeks]
   - Data required: [list]
   - Dependencies: [dependency on Intervention 1 if any]

3. **[Intervention 3]** — EUR [n,nnn]/year
   - Implementation time: [n weeks]
   - Data required: [list]

### Risk Factors

| Risk | Likelihood | Impact | Mitigation |
|------|-----------|--------|-----------|
| Customer disputes delay DSO improvement | Medium | Medium | Validate with dispute resolution SLA data |
| EPD terms not systematically recorded | High | Low | Run one-time vendor invoice audit |
| Collections agent rejects by sales team | Low | High | Align with sales on escalation rules |

---

## 7. Connection to L06/L07/L08 Evidence

| Evidence Source | Finding | Cash Implication |
|----------------|---------|-----------------|
| L06 Friction model | Invoice friction = EUR [n] ([n]% of cost) | Processing delays extend DSO |
| L07 Value stream | Invoice lead time [n]d avg, [n]d escalated | Each escalation day adds to DSO |
| L08 Graph centrality | [Node] betweenness = [x.xx] | Bottleneck node is the DSO driver |
| L09 Working capital | DSO = [n] days, [n]% overdue | EUR [n,nnn] cash releasable |

**Key message:** Friction EUR measures OpEx waste. Cash metrics measure balance sheet impact. Both must be included in the AI investment case.

---

## 8. Glossary

| Term | Definition |
|------|-----------|
| **DSO** | Days Sales Outstanding — average days to collect cash after invoicing |
| **DPO** | Days Payable Outstanding — average days to pay vendors |
| **CCC** | Cash Conversion Cycle = DSO + Inventory Days − DPO |
| **AR aging** | Categorisation of receivables by how long they have been outstanding |
| **EPD** | Early Payment Discount — discount offered by vendor for paying before due date |
| **Write-off** | AR balance deemed uncollectable and removed from the balance sheet |
| **Priority score** | `invoice_value × days_overdue × customer_risk_factor` — higher = collect first |
