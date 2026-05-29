# SaaS Rationalization Scan
**Portfolio Company:** [Company Name]  
**Date:** [YYYY-MM-DD]  
**Analyst:** [Name]  
**Engagement Stage:** [100-Day Plan / Pre-Acquisition / Annual Review]

---

## Executive Summary

| KPI | Value |
|-----|-------|
| Total SaaS tools reviewed | |
| Total annual SaaS spend | EUR |
| Identified rationalization saving | EUR /year |
| % of current SaaS spend | % |
| EBITDA multiple (assumed) | x |
| Implied enterprise value impact | EUR |
| Recommended actions this quarter | |

---

## 1. SaaS Inventory Overview

> Complete this table from SSO/IAM logs, finance system contracts, or IT asset register.

| Tool | Category | Licensed Seats | Active Users (30d) | Utilization % | Annual Cost (EUR) | Owner Dept | Contract Renewal | Risk Flag |
|------|----------|---------------|-------------------|--------------|-------------------|------------|-----------------|-----------|
| | | | | | | | | |

**Data sources used:**
- [ ] SSO provider (Okta, Azure AD, Google Workspace) — login activity logs
- [ ] Finance system — vendor invoices, contract register
- [ ] IT asset management — license inventory
- [ ] Vendor portals — seat utilization dashboards (if available)

---

## 2. Seat Utilization Analysis

**Threshold definitions:**
- LOW UTIL: < 40% seat utilization → immediate review candidate
- WATCH: 40–60% utilization → monitor, review at renewal
- OK: > 60% utilization → no action needed

### Low Utilization Tools (< 40%)

| Tool | Utilization | Licensed | Active | Excess Seats | Cost/Seat | Potential Saving | Renewal In |
|------|------------|---------|--------|-------------|-----------|-----------------|-----------|
| | | | | | EUR | EUR | months |

**Total seat reduction opportunity:** EUR ________/year

**Key actions:**
- [ ] Validate low-utilization tools with tool owners (onboarding gap vs genuine redundancy?)
- [ ] For confirmed redundant seats: renegotiate at contract renewal
- [ ] Priority: tools renewing within 3 months

---

## 3. Duplicate Tool Analysis

> Tools serving the same function in the same category.

| Category | Tools Present | Overlap Score | Recommended To Keep | Recommended To Retire | Potential Saving |
|----------|--------------|--------------|--------------------|-----------------------|-----------------|
| | | | | | EUR |

**Assessment criteria used:**
- Functional overlap score (0–1): number of shared features / total feature union
- User adoption: which tool has higher utilization?
- Strategic fit: which tool has executive sponsorship?
- Integration depth: which tool has more native integrations to other stack?

**Total duplicate consolidation opportunity:** EUR ________/year

### Consolidation Decisions

| Tool to Retire | Kept Tool | Migration Complexity | Migration Cost Est. | Payback (months) | Contract Renewal |
|---------------|-----------|---------------------|--------------------|-----------------:|-----------------|
| | | Low / Med / High | EUR | | |

---

## 4. System Dependency Analysis

> Which tools are most central to critical workflows? High betweenness = high rationalization risk.

### Critical Workflows

| Workflow | Systems Involved | Manual Bridges | Transfer Minutes | Annual Bridge Cost |
|----------|----------------|---------------|-----------------|-------------------|
| | | | min | EUR |

### Manual Bridge Summary

| From System | To System | Workflow | Transfers/Year | Min/Transfer | Hourly Rate | Annual Cost |
|------------|-----------|---------|---------------|-------------|-------------|------------|
| | | | | | EUR | EUR |

**Total manual bridge cost:** EUR ________/year

**Automation options evaluated:**
| Bridge | Automation Option | One-Time Cost | Annual Saving | Payback |
|--------|-----------------|--------------|--------------|---------|
| | iPaaS / Custom API / AI extraction | EUR | EUR | months |

---

## 5. Rationalization Opportunity Scorecard

| # | Opportunity | Lever | Annual Saving | Impl Effort (1–5) | Risk (1–5) | Opp Score | Renewal Urgency | Priority |
|---|------------|-------|--------------|-------------------|-----------|----------|----------------|---------|
| 1 | | Seat Reduction | EUR | | | | months | High |
| 2 | | Consolidation | EUR | | | | months | |
| 3 | | Bridge Automation | EUR | | | | — | |
| 4 | | Point Solution | EUR | | | | months | |

**Scoring formula:** `Opportunity Score = Annual Saving / (Implementation Effort × Risk)`

**Total portfolio value:**

| Lever | Annual Saving | % of Total |
|-------|-------------|-----------|
| Seat Reduction | EUR | % |
| Duplicate Consolidation | EUR | % |
| Manual Bridge Automation | EUR | % |
| Point Solution Deprecation | EUR | % |
| **TOTAL** | **EUR** | **100%** |

---

## 6. Implementation Roadmap

### This Quarter (0–3 months) — Quick Wins

> Renewals due, seat negotiations, low-risk deprecations.

| Action | Tool | Owner | Deadline | Expected Saving |
|--------|------|-------|----------|----------------|
| Renegotiate seats at renewal | | IT / Procurement | | EUR |
| Deprecate point solution | | IT | | EUR |

### Next Quarter (3–6 months) — Consolidation Projects

> Tool migrations requiring project plan, change management, data migration.

| Project | Tools | Lead | Duration | Migration Cost | Annual Saving |
|---------|-------|------|----------|---------------|--------------|
| | | | weeks | EUR | EUR |

### H2 (6–12 months) — Integration Automation

> Bridge automation, iPaaS setup, API integrations.

| Bridge | Solution | Lead | Duration | Setup Cost | Annual Saving |
|--------|---------|------|----------|-----------|--------------|
| | | | weeks | EUR | EUR |

---

## 7. Risk Register

| Risk | Probability | Impact | Mitigation |
|------|------------|--------|-----------|
| Tool owner resistance to consolidation | Med | Med | Executive sponsor, change management plan |
| Data migration failure | Low | High | Parallel run period, data backup before cutover |
| Integration breakage after tool retirement | Med | High | Dependency mapping before retirement, test in staging |
| Contract renewal missed — saving lost for 12 months | Med | Med | Renewal calendar in IT governance process |
| AI hype — business case overstated | Low | High | Use conservative assumptions, avoid replacing complex SaaS with unproven AI agent |

---

## 8. PE Investment Committee Summary

> 3–5 bullet points suitable for IC memo or portfolio review.

- **Total SaaS rationalization opportunity of EUR ______/year** identified across [X] tools, representing [X]% of current software spend, achievable within 12 months through seat rightsizing, [X] tool consolidations, and [X] integration automations.

- **Implementation cost of EUR ______** delivers a [X]-month payback with 12-month ROI of [X]% — within 100-day plan horizon with zero headcount reduction required.

- **At [X]x EBITDA multiple**, annual saving equates to EUR ______ in enterprise value creation; contract renewal calendar tracking unlocks the majority of savings within the current fiscal year.

- **System dependency analysis** identified [X] manual bridges costing EUR ______/year in analyst time; automating the top [X] bridges eliminates [X]% of avoidable operational friction (L06 connection).

- **Critical path:** [X] tool contracts renew within 90 days — seat renegotiation and cancellation decisions must be made immediately to capture EUR ______ in this renewal cycle.

---

## Appendix A — Data Sources and Methodology

| Data Source | Accessed Via | Data Freshness | Limitations |
|------------|-------------|---------------|------------|
| Login activity | SSO provider API / export | Last 30 days | Does not capture API-only usage |
| Contract data | Finance system / spreadsheet | | May not include auto-renewed contracts |
| Feature overlap | Manual review / product comparison | | Subjective; validate with tool owners |
| Bridge cost | L06 friction model (time × volume × rate) | | Based on sample interviews |

## Appendix B — Tools Reviewed but Excluded

| Tool | Reason for Exclusion |
|------|---------------------|
| | Regulatory requirement — cannot be retired |
| | Strategic initiative dependency |
| | Data not available for analysis |

---

*Template: AI Value Engineering Masterclass — Lesson 10 (SaaS Rationalization)*  
*Methodology: Seat Utilization Analysis + Duplicate Detection + System Dependency Graph + Manual Bridge Cost (L06)*
