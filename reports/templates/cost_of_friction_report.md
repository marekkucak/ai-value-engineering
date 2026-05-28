# Cost of Friction Report Template

## Learner Information

- **Name:** ___________________________
- **Company/Case Study:** ___________________________
- **Date Completed:** ___________________________

---

## Instructions

### Your Task

Measure **friction cost** (preventable waste + opportunity cost) for workflows in your company or a case study. Break each workflow into 3 cost layers: base (necessary), rework (preventable), and expert interruptions (opportunity).

### Success Criteria

✓ Calculated friction for 3-5 workflows

✓ Each calculation includes all 3 friction layers with justification

✓ Ranked workflows by friction % to identify highest-priority opportunities

✓ Connected friction findings to L05 PE value levers (labor productivity)

✓ Identified which workflows are best targets for AI intervention

---

## Worked Example 1: Invoice Approval (€4,928 Annual Cost)

### Workflow Description
- **Process:** Analyst reviews supplier invoices for amount, vendor, GL code accuracy
- **Volume:** 4,200 invoices per year
- **Current cost (from Lesson 02):** €4,928/year

### Friction Analysis

| Friction Layer | Metric | Calculation | Cost |
|---|---|---|---|
| **Base Manual** | Touch time | 4,200 × 12 min ÷ 60 × €55/hr | €4,620 |
| **Rework** | Missing GL code | 4,200 × 5% × 10 min ÷ 60 × €55/hr | €231 |
| **Expert Interruption** | Manager approval | 4,200 × 2% × 20 min ÷ 60 × €75/hr | €77 |
| **TOTAL** | | | €4,928 |
| **Friction (Rework + Expert)** | | | **€308** |
| **Friction %** | | | **6.2%** |

### Cost Per Transaction
- Total: €1.17 per invoice
- Friction: €0.07 per invoice

### Interpretation
- Base cost (€4,620) is necessary — we still need to review invoices
- Friction (€308) is preventable through:
  - **Data quality:** Supplier pre-fills GL code (prevents 5% rework)
  - **Automation:** AI extracts fields from PDF, auto-flags non-standard vendors (prevents manager approvals)
- **Scale consideration:** At 4,200 volume, €308 is small. At 1M invoices, this becomes €73k — then it's a priority

### AI Opportunity
- **Lever 1 (Labor Productivity):** Reduce rework from 5% → 1% = €186 savings
- **Lever 6 (Better Pricing & Margin):** Detect missing GL codes that understate charges = margin recovery
- **Estimated value:** €300-400k if scaling to multi-entity invoice volume

---

## Worked Example 2: Support Triage (€35,073 Annual Cost)

### Workflow Description
- **Process:** Support analyst triages incoming tickets, routes to correct team (technical, billing, general)
- **Volume:** 18,000 tickets per year
- **Current cost (from Lesson 02):** €35,073/year

### Friction Analysis

| Friction Layer | Metric | Calculation | Cost |
|---|---|---|---|
| **Base Manual** | Triage & route | 18,000 × 14 min ÷ 60 × €55/hr | €15,400 |
| **Rework** | Misrouted (re-triage) | 18,000 × 8% × 18 min ÷ 60 × €55/hr | €3,528 |
| **Expert Interruption** | Specialist escalation | 18,000 × 15% × 30 min ÷ 60 × €75/hr | €6,075 |
| **TOTAL** | | | €25,003 |
| **Friction (Rework + Expert)** | | €{3,528 + 6,075} | **€9,603** |
| **Friction %** | | | **38.4%** |

### Cost Per Transaction
- Total: €1.39 per ticket
- Friction: €0.53 per ticket (38% is waste!)

### Interpretation
- Base cost (€15,400) is necessary — we still need triage
- Friction (€9,603) is high due to:
  - **Rework:** Misrouting happens 8% of the time (complex tickets, ambiguous categories)
  - **Expert time:** 15% of tickets need specialist review = manager/expert time (€6,075)
- **This is a high-friction workflow.** Friction is 27% of total portfolio friction (€9,603 of €13,933)

### Root Causes of Friction
- **Rework:** Unclear ticket descriptions, ambiguous categorization rules
- **Expert time:** Complex issues that analyst can't confidently route

### AI Opportunity
- **Lever 1 (Labor Productivity):** AI learns routing patterns; improves accuracy 92% → 98% = €1,764 saved
- **Lever 4 (Lower Support Cost):** Reduce escalation 15% → 5% = €4,050 saved
- **Lever 10 (Working Capital):** Faster resolution → lower DSO, fewer repeat contacts
- **Estimated value:** €5,814k + customer satisfaction improvement (NPS +5 points = retention uplift €200k)

### Why AI Works Here
- **High volume (18,000):** Even 1% improvement = €138k value
- **Clear categorization:** Routing is deterministic (X keywords → Y team)
- **Labeled history:** 18,000 historical tickets provide training data for ML classifier

---

## Worked Example 3: Management Reporting (€9,067 Annual Cost)

### Workflow Description
- **Process:** Analyst gathers data, builds monthly/quarterly management reports, stakeholders review and approve
- **Volume:** 52 reports per year (52 = 12 monthly + 4 quarterly + 36 ad-hoc)
- **Current cost (from Lesson 02):** €9,067/year

### Friction Analysis

| Friction Layer | Metric | Calculation | Cost |
|---|---|---|---|
| **Base Manual** | Data + analysis | 52 × 180 min ÷ 60 × €55/hr | €5,181 |
| **Rework** | Revision cycles | 52 × 30% × 120 min ÷ 60 × €55/hr | €2,860 |
| **Expert Interruption** | Executive review | 52 × 5% × 30 min ÷ 60 × €90/hr | €1,162 |
| **TOTAL** | | | €9,203 |
| **Friction (Rework + Expert)** | | €{2,860 + 1,162} | **€4,022** |
| **Friction %** | | | **43.7%** |

### Cost Per Transaction
- Total: €177 per report
- Friction: €77 per report (44% is waste!)

### Interpretation
- Base cost (€5,181) is necessary — we still need analysis and presentation
- Friction (€4,022) is HIGHEST of 3 workflows (44% vs 38% support, 6% invoice) due to:
  - **Rework:** 30% of reports require revision cycles (data changes, format requests, analysis pushed back)
  - **Expert time:** 5% escalated to executive for sign-off (executive review adds time/approval bottleneck)
- **Knowledge work has high friction** because of iterative cycles and subjective review

### Root Causes of Friction
- **Rework:** Changing business priorities, late data arrivals, stakeholder feedback requires full re-analysis
- **Expert review:** Executive questions during review require analyst to rebuild sections
- **Lack of clarity:** Report specs not defined upfront (vs transactional processes like invoice which are standardized)

### AI Opportunity
- **Lever 1 (Labor Productivity):** AI auto-generates standard sections (executive summary, variance analysis); analyst reviews/customizes = 50% time savings = €2,590
- **Lever 3 (Faster Sales):** AI dashboards replace monthly reports; stakeholders self-serve = eliminates revision cycles = €2,860 friction eliminated
- **Lever 6 (Better Pricing):** AI detects pricing anomalies/opportunities in reports
- **Estimated value:** €5,450+ (this is the highest-ROI workflow for automation)

### Why AI Works Here
- **High friction percentage (44%):** Even 50% reduction = €2,000 value
- **Repetitive structure:** Monthly reports have same sections; templating works
- **Data availability:** Source systems stable; data quality main issue
- **Subjective review:** Large language models (LLMs) can draft narratives, reduce revision cycles

---

## Your Analysis: Blank Template

**Complete this section with your own workflow analysis. Use the worked examples as reference.**

---

### Workflow 1: ___________________________

#### Workflow Description
- **Process:** _____________________________________________________
- **Volume:** ___________________________
- **Current cost:** ___________________________

#### Friction Analysis

| Friction Layer | Metric | Calculation | Cost |
|---|---|---|---|
| **Base Manual** | | | € |
| **Rework** | | | € |
| **Expert Interruption** | | | € |
| **TOTAL** | | | €_____ |
| **Friction** | | | **€_____** |
| **Friction %** | | | **_____% ** |

#### Cost Per Transaction
- Total: €_____ per _____ (unit)
- Friction: €_____ per unit

#### Interpretation
[Your analysis: What is the friction? Why does it exist? Is it preventable?]

#### AI Opportunity
[Your analysis: Which PE value levers apply? What's the potential value?]

---

### Workflow 2: ___________________________

#### Workflow Description
- **Process:** _____________________________________________________
- **Volume:** ___________________________
- **Current cost:** ___________________________

#### Friction Analysis

| Friction Layer | Metric | Calculation | Cost |
|---|---|---|---|
| **Base Manual** | | | € |
| **Rework** | | | € |
| **Expert Interruption** | | | € |
| **TOTAL** | | | €_____ |
| **Friction** | | | **€_____** |
| **Friction %** | | | **_____% ** |

#### Cost Per Transaction
- Total: €_____ per _____ (unit)
- Friction: €_____ per unit

#### Interpretation
[Your analysis]

#### AI Opportunity
[Your analysis]

---

### Workflow 3: ___________________________

#### Workflow Description
- **Process:** _____________________________________________________
- **Volume:** ___________________________
- **Current cost:** ___________________________

#### Friction Analysis

| Friction Layer | Metric | Calculation | Cost |
|---|---|---|---|
| **Base Manual** | | | € |
| **Rework** | | | € |
| **Expert Interruption** | | | € |
| **TOTAL** | | | €_____ |
| **Friction** | | | **€_____** |
| **Friction %** | | | **_____% ** |

#### Cost Per Transaction
- Total: €_____ per _____ (unit)
- Friction: €_____ per unit

#### Interpretation
[Your analysis]

#### AI Opportunity
[Your analysis]

---

## Summary & Prioritization

### Total Friction Across All Workflows

| Workflow | Total Cost | Friction (€) | Friction % | Priority |
|---|---|---|---|---|
| 1. | €_____ | €_____ | _____% | HIGH / MED / LOW |
| 2. | €_____ | €_____ | _____% | HIGH / MED / LOW |
| 3. | €_____ | €_____ | _____% | HIGH / MED / LOW |
| **TOTAL** | **€_____** | **€_____** | **_____% ** | |

### Highest-Priority Workflow for AI Intervention

**Workflow:** ___________________________

**Why:** [Friction %, root cause, scale, impact potential]

**Recommended AI Intervention:** [Which PE value levers? What technology? (AI classifier, chatbot, RPA, LLM, etc.)]

**Estimated Value:** €_____ per year + [secondary benefits: time savings, satisfaction improvement, etc.]

---

## Connection to PE Value Levers (Lesson 05)

**Which levers apply to your workflows?** (Check all that apply)

- [ ] **Lever 1: Labor Productivity** — Reduce touch time, rework, or escalations
- [ ] **Lever 3: Faster Sales Cycles** — Reduce DSO through faster processing
- [ ] **Lever 4: Lower Support Cost** — Reduce support team cost
- [ ] **Lever 6: Better Pricing & Margin** — Margin recovery from data quality improvements
- [ ] **Lever 7: Reduced Compliance Cost** — Compliance workflow efficiency
- [ ] **Lever 8: Faster Onboarding** — Reduce employee/customer onboarding time
- [ ] **Lever 10: Working Capital** — Reduce DSO or inventory through process speed

**Total Potential Value (All Levers):** €_______ per year

---

## Completion Checklist

**Before submitting, verify:**

- [ ] Analyzed 3+ workflows (your own company or provided case study)
- [ ] All 3 friction layers calculated for each (base, rework, expert)
- [ ] Calculations include all parameters: volume, time, cost, rates
- [ ] Ranked by friction % to identify highest-priority opportunity
- [ ] Connected to PE value levers from Lesson 05
- [ ] Total friction makes sense (typically 15-50% of total cost)
- [ ] Identified root causes of friction (data quality, routing, revision cycles, etc.)
- [ ] Proposed AI solutions with estimated value
- [ ] Summary is clear enough to present to management

---

## Extensions & Advanced

### For Executives: Build a Business Case

If your highest-priority workflow has €10k friction:
1. **Baseline friction:** €10k/year
2. **AI solution:** Deploy classifier to reduce rework 50%
3. **Value:** €5k/year in labor cost saved
4. **Cost:** €50k/year SaaS + €20k implementation
5. **Payback:** (€70k ÷ €5k) = 14 years — NOT VIABLE

→ **Reframe:** Find workflows with €100k+ friction, or combine multiple workflows to hit €500k+ total value (then AI ROI works)

### For Data Teams: Prepare Input Data

Friction analysis requires:
- **Process logs** with timestamp, case ID, step, assignee (for wait time calculation)
- **Rework indicators:** Tickets reopened, invoices rejected, documents revised
- **Escalation data:** Who escalated, to whom, for what reason
- **Cost data:** Hourly rates by role

Build these metrics into your data warehouse **before** designing AI solutions.

### For Portfolio Managers

If you manage 5-10 companies:
1. **Calculate friction for each company** (use this template)
2. **Build a heatmap:** Companies × workflows showing friction % and opportunities
3. **Identify patterns:** "All manufacturing companies have 40% reporting friction" → Platform solution
4. **Prioritize:** Which company's highest-friction workflow has best ROI?
5. **Scale playbook:** Automate highest-impact workflows across portfolio

---

## Resources

- **Lesson 06 Notebook:** Detailed `cost_of_friction()` calculations for all worked examples
- **Lesson 05 (PE Levers):** Understand which AI interventions matter most
- **Lesson 02 (Cost Models):** Source data for volumes, touch times, rework rates
- **Lesson 07 (Value Stream):** Find ROOT CAUSES of friction you measured here
