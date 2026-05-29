# Value Stream Analysis Report

## Learner Information

- **Name:** ___________________________
- **Company/Case Study:** ___________________________
- **Workflow(s) Analyzed:** ___________________________
- **Date Completed:** ___________________________

---

## Instructions

### Your Task

Analyze the **lead time decomposition** and **bottleneck identification** for 1-3 workflows. Break down total lead time into process time (actual work) and wait time (delays). Identify where cases get stuck, and connect findings back to L06 friction measurements.

### Success Criteria

✓ Calculated all 5 value stream metrics for each workflow

✓ Lead time decomposition shows process time vs wait time (% breakdown)

✓ Identified the bottleneck step for each workflow with quantified impact

✓ Connected L06 friction findings to L07 lead time delays

✓ Analyzed lead time variance and SLA impact

✓ Recommended prioritized improvements based on cost × time × ease

✓ Process logs included (CSV or summary table) for L08 graph analysis

---

## The 5 Value Stream Metrics

Before analyzing, here's a quick reference for the metrics you'll calculate:

| Metric | Formula | Example | Why It Matters |
|--------|---------|---------|----------------|
| **Lead Time** | max(timestamp) - min(timestamp) | Invoice submitted Mon 9am, approved Fri 11am = 4 days | Customer perception, SLA, cash conversion |
| **Process Time** | sum(duration_minutes) for all steps | Review 12 min + GL entry 3 min + approve 2 min = 17 min | Actual work efficiency |
| **Wait Time** | Lead Time - Process Time | 4 days - 17 min ≈ 3.99 days (99.5% waiting!) | Identifies queues/bottlenecks |
| **First-Pass Yield** | (1 - rework_rate) × 100 | 95% (5% rejected) | Quality/validation issues |
| **Bottleneck** | Step with highest avg wait | Manager approval queue: 20-hour avg wait | Where to intervene first |

---

## Worked Example 1: Invoice Approval (Detailed)

### Workflow Overview

- **Volume:** 4,200 invoices/year (1,050 in Q1)
- **Process:** Submit → Review (analyst) → Approve (manager if >$X or unusual) → Complete
- **L06 Context:** 5% rework (missing GL), 2% escalation, €308 friction (6%)

### Analysis

#### Lead Time Distribution
| Metric | Value |
|--------|-------|
| Average | 1.3 days |
| Median | 1.1 days |
| 90th percentile | 2.5 days |
| 99th percentile | 7.0 days |
| Min / Max | 0.2 / 8.1 days |

#### Process Time vs Wait Time

- **Average process time:** 12 minutes (0.008 days)
- **Average wait time:** 1.29 days (1,860 minutes)
- **Wait as % of lead time:** 99.4%

**Insight:** Almost 100% of invoice lead time is WAITING, not working. The bottleneck is a queue, not processing speed.

#### Bottleneck Identification

| Step | Avg Wait Before | Root Cause |
|------|-----------------|-----------|
| Submit | 0 min | Start of process |
| Review | 30 min | Analyst triaging other invoices |
| **Approve** | **20 hours** | **Manager unavailable/overloaded** |
| Complete | 30 min | System processing |

**Bottleneck Step:** APPROVE (manager step)
- 20-hour average queue
- 2% of invoices (84 total) go through manager
- But when they do, they wait 20 hours

#### L06 Connection

- L06 friction: €308 (€77 manager time + €231 rework)
- L07 finding: €77 manager cost = 20-hour queue delay
- Implication: Manager approval bottleneck causes both friction cost AND lead time variance
- Solution: Automate manager approval (rule-based routing) → eliminate queue → save €77 + reduce lead time 90%

### What-If Analysis

**Scenario:** Automate manager approval for standard cases (98% of invoices)

- Current avg lead time: 1.3 days
- Process time: 0.008 days (stays same)
- New wait time: 0.3 days (only residual handoff delays)
- **New average lead time: 0.3 days (77% reduction)**
- SLA impact: 0% exceed 3-day SLA (vs 15% currently)

---

## Worked Example 2: Support Triage (Medium Detail)

### Workflow Overview

- **Volume:** 18,000 tickets/year (4,500 in Q1)
- **Process:** Submit → Triage → Assign → Resolve (analyst or specialist) → Close
- **L06 Context:** 8% misroute rework, 15% specialist escalation, €9,603 friction (27%)

### Lead Time Comparison: Escalated vs Non-Escalated

| Group | Volume | Avg Lead Time | Avg Wait Time | % of Lead Time Waiting |
|-------|--------|---------------|---------------|----------------------|
| Non-Escalated | 85% (3,825) | 2.1 days | 2.0 days | 95% |
| Escalated | 15% (675) | 8.2 days | 8.1 days | 99% |
| **Escalation Impact** | - | **+6.1 days** | **+6.1 days** | - |

**Key Finding:** Each escalation adds 6+ days to lead time. This is where specialists queue up waiting to be available.

### Bottleneck Identification

- **Non-escalated bottleneck:** Analyst assignment queue (1-2 hours)
- **Escalated bottleneck:** Specialist queue (8 hours average) — **PRIMARY BOTTLENECK**

### L06 Connection

- L06 friction: €9,603 total (€3,528 rework + €6,075 specialist time)
- L07 finding: Escalations add 6 days + specialist queue bottleneck
- Implication: 15% of tickets waiting 8 hours for specialist = customer dissatisfaction + SLA misses
- Solution: Reduce escalation rate (better initial routing) → 15% → 5% = eliminate queue

### What-If Analysis

**Scenario:** Improve initial routing accuracy, reduce escalation 15% → 5%

- Current portfolio avg lead time: 3.5 days
- New portfolio avg lead time: 2.7 days (23% reduction)
- Cases avoiding 8-hour queue: 10% of volume (450 tickets)
- Value: 450 tickets × 6 days × €55/hr ÷ 8 ≈ €18,500 analyst time saved

---

## Worked Example 3: Management Reporting (Brief)

### Key Finding: Revision Cycles Drive Lead Time Variance

| Revision Count | % of Reports | Avg Lead Time | Days Added |
|---|---|---|---|
| No revisions | 70% | 12 days | 0 |
| 1 revision | 25% | 18 days | +6 days |
| 2+ revisions | 5% | 28 days | +16 days |

**Lead time variance (std dev): 5.2 days (highest of 3 workflows!)**

### Bottleneck

- **Executive review cycle:** Multi-day turnaround + feedback → rework → re-review
- Each revision cycle = 6 days

### L06 Connection

- L06 friction: €4,022 (44% of cost, highest %)
- L07 finding: 30% revision rate creates high unpredictability (11–35 day range)
- Implication: Unpredictable lead times hurt DSO + planning
- Solution: Reduce revision rate (clear upfront requirements, template-driven drafting, LLM review)

---

## Your Analysis: Blank Template

**Complete this section with your own workflow analysis.**

---

### Workflow 1: ___________________________

#### Workflow Overview

- **Volume:** ___________________________
- **Process steps:** ___________________________
- **L06 Context (friction %):** ___________________________
- **Key metrics from L06:** ___________________________

#### Lead Time Analysis

| Metric | Value |
|--------|-------|
| Average lead time | _____ days |
| Median lead time | _____ days |
| 90th percentile | _____ days |
| Min / Max | _____ / _____ days |

#### Process Time vs Wait Time

- **Average process time:** _____ minutes (_____ days)
- **Average wait time:** _____ days
- **Wait as % of lead time:** _____% 

**Interpretation:** [Your analysis: Is it mostly waiting or mostly working?]

#### Bottleneck Identification

| Step | Avg Wait Before | Root Cause |
|------|---|---|
| | | |
| | | |

**Primary Bottleneck:** ___________________________
- **Average wait:** _____ hours/days
- **% of cases affected:** ____%

#### L06 Connection

- **L06 friction €:** _____
- **L06 friction %:** _____% 
- **L07 lead time variance:** _____ days
- **Implication:** [How does friction cost manifest as lead time delays?]

#### What-If Analysis

**Scenario:** [Describe an intervention to reduce bottleneck impact]

- **Current average lead time:** _____ days
- **New average lead time:** _____ days
- **Improvement:** _____ days (_____%)

---

### Workflow 2: ___________________________

[Repeat template with new workflow details]

---

### Workflow 3: ___________________________

[Repeat template with new workflow details]

---

## Cross-Workflow Comparison & Prioritization

### Summary Matrix

| Workflow | L06 Friction % | L06 Friction € | L07 Avg Lead Time | L07 Lead Time Variance | Primary Bottleneck | Recommended Action |
|----------|---|---|---|---|---|---|
| | % | € | days | days (σ) | [Step] | [Intervention] |
| | % | € | days | days (σ) | [Step] | [Intervention] |
| | % | € | days | days (σ) | [Step] | [Intervention] |

### Prioritization Framework

For each workflow, score by **Cost Impact × Volume × Ease:**

| Workflow | Cost Impact | Volume | Ease | Priority Score | Rank |
|----------|---|---|---|---|---|
| | € | % | Easy/Med/Hard | [Score] | 1/2/3 |
| | € | % | Easy/Med/Hard | [Score] | 1/2/3 |
| | € | % | Easy/Med/Hard | [Score] | 1/2/3 |

### Recommendation

**First Priority:** ___________________________

**Why:** [Cost impact, volume, ease justification]

**Expected outcome:** 
- Cost savings: €_____
- Lead time reduction: _____ days
- Variance reduction: _____ days

---

## Business Impact Analysis

### SLA Compliance

| Workflow | SLA Target | % Currently Met | % After Fix |
|----------|---|---|---|
| | _____ days | _____% | _____% |
| | _____ days | _____% | _____% |

### DSO & Cash Conversion Impact

[Calculate working capital impact of lead time reduction]

- Current lead time variance: _____ days
- DSO impact: ~_____ days
- At €_____ in annual receivables, working capital impact: €_____

### Customer Satisfaction

[How does lead time variance affect NPS/satisfaction?]

---

## Data for L08 Graph Analysis

### Process Log Summary

[Export or summarize your process logs for L08]

- **Number of cases:** _____
- **Date range:** _____ to _____
- **Number of steps in workflow:** _____
- **Number of unique actors:** _____
- **Handoff frequency:** _____ handoffs per case (average)

### Handoff Matrix (for L08)

[Create a handoff matrix showing which step hands off to which step, which actor hands off to whom]

| From Step | To Step | Frequency | Avg Wait |
|---|---|---|---|
| | | | |
| | | | |

---

## Completion Checklist

Before submitting, verify:

- [ ] Calculated lead time, process time, wait time for each workflow
- [ ] Identified primary bottleneck for each workflow with quantified impact (days/hours of wait)
- [ ] Lead time variance (standard deviation) calculated
- [ ] L06 friction findings explicitly connected to L07 lead time delays
- [ ] What-if analysis shows lead time improvement potential
- [ ] Prioritized workflows by cost × volume × ease
- [ ] SLA compliance impact analyzed
- [ ] DSO/working capital impact calculated (even if roughly)
- [ ] Process logs prepared for L08 graph analysis
- [ ] All 5 value stream metrics explained and calculated

---

## Advanced Extensions

### For Operations Teams

**SLA-Driven Prioritization:**
- Calculate cost of SLA violations (lost margin, penalties)
- Use L07 lead time data to predict SLA compliance
- Prioritize bottleneck fixes that move needle on SLA %

### For Finance Teams

**DSO & Working Capital Impact:**
- Lead time variance drives DSO variance
- High variance = forecast uncertainty = safety stock requirement
- Quantify cash conversion cycle benefit of reducing lead time/variance

### For Executives

**Business Case Building:**
- Cost savings from labor efficiency (€)
- Revenue protection from SLA improvements (€)
- Cash flow improvement from DSO reduction (€)
- Total value: [Add all three] = payback timeline for AI investment

### For Data Teams

**Process Mining Setup:**
- Export process logs in standard format (OCEL, CSV with case/step/timestamp/actor)
- Prepare for L08: Add handoff edges (which step → which step, which actor → which actor)
- Quality checks: Are there cases with gaps in steps? Out-of-order timestamps?

---

## Resources

- **Lesson 07 Notebook:** Detailed calculations and visualizations for all worked examples
- **Lesson 06 (Friction):** Reference L06 friction data (rework rates, escalation rates)
- **Lesson 08 (Graph):** Prepare process logs for handoff graph construction
- **Lesson 05 (PE Levers):** Understand labor productivity lever (this is about labor redeployment from queue to strategy)
