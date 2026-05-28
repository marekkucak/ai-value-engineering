# Private Equity Value Masterclass for AI / Graph Engineers

> A practical curriculum for AI engineers, graph analysts, Databricks/Google-stack builders, and remote AI value-creation architects who need to connect workflow analytics, graph intelligence, AI agents, and financial value creation.

This course is the **value-calculation counterpart** to a graph-analysis masterclass. The graph course teaches how to model and analyze corporate systems as graphs. This course teaches how to translate those findings into **business value, EBITDA impact, ROI, payback, valuation impact, and PE-style value creation proposals**.

---

## 0. Course philosophy

Most AI engineers can say:

```text
This workflow can be automated.
```

A PE-grade AI value architect must say:

```text
This workflow runs 18,000 times per year.
Median manual touch time is 14 minutes.
The current process cost is €720k/year.
The AI workflow can reduce touch time by 45% with human approval.
Expected annual run-rate value is €324k.
Implementation cost is €90k.
Payback is 3.3 months.
At an 8x EBITDA multiple, this can support €2.6M enterprise value.
```

The purpose of this course is to train that thinking.

---

## 1. Target learner

This course is for:

- AI engineers
- graph data analysts
- Databricks engineers
- Google Cloud / Gemini builders
- workflow automation engineers
- AI consultants
- PE portfolio transformation analysts
- remote AI value-creation architects
- software engineers moving into business-value-driven AI work

The learner should already be comfortable with basic Python. Graph lessons use `pandas`, `networkx`, and optionally `neo4j`.

---

## 2. Learning outcomes

By the end of the course, the learner should be able to:

1. Read basic financial statements well enough to understand operational value.
2. Explain EBITDA and why PE managers care about it.
3. Translate workflow friction into cost, margin, cash-flow, and valuation impact.
4. Build ROI, payback, run-rate savings, and EBITDA bridge calculations.
5. Use process and graph analysis to identify where value is trapped.
6. Design AI interventions that improve cost, speed, risk, productivity, or working capital.
7. Evaluate whether an AI workflow is financially worth implementing.
8. Create PE-style executive value memos.
9. Connect graph findings to value propositions.
10. Package reusable value-calculation templates for AI transformation projects.

---


## 3. Recommended repository layout

```text
pe-ai-value-masterclass/
├── README.md
├── MASTER_LESSONS.md
├── requirements.txt
├── pyproject.toml
├── Makefile
├── notebooks/
│   ├── 00_foundations_environment_and_value_thinking.ipynb
│   ├── 01_finance_for_ai_engineers.ipynb
│   ├── 02_operating_metrics_to_pnl.ipynb
│   ├── 03_ebitda_basics_and_bridge.ipynb
│   ├── 04_roi_payback_npv.ipynb
│   ├── 05_pe_value_creation_playbook.ipynb
│   ├── 06_cost_of_friction_model.ipynb
│   ├── 07_value_stream_metrics.ipynb
│   ├── 08_graph_bottlenecks_to_value.ipynb
│   ├── 09_working_capital_and_cash.ipynb
│   ├── 10_saas_rationalization_value.ipynb
│   ├── 11_ai_opportunity_scoring.ipynb
│   ├── 12_human_ai_task_split_value.ipynb
│   ├── 13_capstone_approval_flow_acceleration.ipynb
│   ├── 14_capstone_process_knowledge_graphrag.ipynb
│   ├── 15_capstone_procurement_invoice_optimizer.ipynb
│   ├── 16_capstone_access_risk_audit_assistant.ipynb
│   ├── 17_capstone_saas_system_dependency_scan.ipynb
│   └── 18_portfolio_value_creation_playbook.ipynb
├── src/
│   ├── data_generation/
│   ├── value_models/
│   ├── graph_value/
│   ├── reporting/
│   └── utils/
├── data/seed/
├── reports/templates/
├── skills/
│   ├── value_thesis.md
│   ├── ebitda_bridge.md
│   ├── cost_of_friction.md
│   ├── graph_to_value.md
│   ├── ai_opportunity_scorecard.md
│   └── executive_value_memo.md
└── tests/
```

---

## 4. Core concepts map

```text
Workflow evidence
→ process metrics
→ graph bottlenecks
→ operational friction
→ financial value lever
→ AI intervention
→ implementation cost
→ ROI / payback / EBITDA impact
→ executive recommendation
```

---

## 4.1 Before implementing Lesson 01

This course treats Lesson 00 as a mandatory gate before Lesson 01.

### Implementation checklist

Complete all items before building or teaching Lesson 01:

1. Define Lesson 01 entry criteria in writing.
2. Create a pass/fail readiness scorecard for Lesson 00.
3. Add deterministic synthetic datasets for Lesson 00 exercises.
4. Confirm Python environment setup instructions work end-to-end.
5. Confirm all Lesson 00 notebooks run top-to-bottom without manual edits.
6. Add minimum validation checks for core formulas:
    - annual manual cost
    - expected run-rate value
    - payback
7. Create a one-page glossary for finance terms used in Lessons 01-04.
8. Add a workflow-to-P&L mapping exercise with answer key.
9. Add one mini case that converts workflow metrics to EBITDA and enterprise value impact.
10. Add progression rule: learners cannot start Lesson 01 until Lesson 00 is passed.

### Lesson 01 readiness gate (must pass)

Learner must demonstrate all of the following:

1. Environment readiness:
    - Python and notebook runtime working
    - required packages import successfully
2. Value calculation readiness:
    - can compute baseline annual manual cost from volume, minutes, and loaded cost
    - can compute expected run-rate value using reduction, adoption, and confidence
3. Finance readiness:
    - can explain EBITDA in plain language
    - can map at least three workflow impacts to the correct P&L line item
4. Decision readiness:
    - can produce a short recommendation using ROI/payback logic with assumptions

---

# Part I — Finance foundations for AI engineers

## Lesson 00 — Mandatory onboarding and readiness gate

### Purpose

Standardize technical setup and value-thinking foundations so all learners start Lesson 01 with a shared baseline.

### Target duration

3.5 to 4.0 hours.

### Five Integrated Modules (comprehensive 4-hour lesson)

**Module 00A (30 min):** Environment and tooling verification
- Imports for pandas, numpy, matplotlib, networkx
- Simple DataFrame operations
- Baseline annual cost calculation
- Graph construction and analysis

**Module 00B (45 min):** Value-thinking mindset shift
- Time saved vs money saved concept
- annual_manual_cost() and expected_run_rate_value() functions
- Five workflow examples with risk-adjusted calculations

**Module 00C (60 min):** Finance crash course for builders
- P&L structure (Revenue → OpEx → EBITDA)
- Workflow-to-P&L line-item mapping
- EBITDA multiple and enterprise value concept

**Module 00D (60 min):** Evidence → cost → impact framework
- Complete mini-case: Support Triage Automation
- From baseline cost to EBITDA delta to enterprise value impact
- ROI, payback, and recommendation logic

**Module 00E (30 min):** Course dependency map and learning path
- Lesson dependencies and prerequisites
- Mandatory vs optional paths
- Total time investment visualization

### Single Deliverable

`notebooks/00_foundations_environment_and_value_thinking.ipynb` — Comprehensive notebook combining all five modules with exercises, calculations, and completion checklist.

---

## Lesson 01 — Financial intelligence for AI engineers

### Goal
Understand how operational work appears in financial statements.

### Concepts
Revenue, COGS, gross margin, operating expenses, EBITDA, capex vs opex, cash flow basics, why “time saved” is not automatically “money saved”.

### Why this matters
An AI workflow may save time but not create EBITDA unless it affects headcount, outsourcing cost, software cost, throughput, revenue, churn, error/rework, working capital, or management capacity.

### Exercise
Given a simple company P&L, identify which line items could be affected by support automation, invoice processing automation, SaaS rationalization, sales research copilot, and finance close assistant.

### Deliverable
`finance_line_item_impact_matrix.md`

---

## Lesson 02 — From operating metrics to P&L impact

### Goal
Connect workflow metrics to business financials.

### Concepts
Volume, touch time, cycle time, queue time, loaded labor cost, error rate, rework rate, cost per transaction, capacity release, run-rate savings.

### Formulas

```text
Annual manual cost = annual volume × manual minutes per case ÷ 60 × loaded hourly cost
Annual run-rate value = annual manual cost × expected reduction percentage × adoption percentage × confidence factor
```

### Sample code

```python
def annual_manual_cost(volume_per_year, minutes_per_case, loaded_hourly_cost):
    return volume_per_year * (minutes_per_case / 60) * loaded_hourly_cost


def expected_run_rate_value(
    volume_per_year,
    minutes_per_case,
    loaded_hourly_cost,
    reduction_pct,
    adoption_pct=1.0,
    confidence=0.8,
):
    baseline = annual_manual_cost(volume_per_year, minutes_per_case, loaded_hourly_cost)
    return baseline * reduction_pct * adoption_pct * confidence

baseline = annual_manual_cost(18000, 14, 55)
value = expected_run_rate_value(18000, 14, 55, reduction_pct=0.45, adoption_pct=0.8)

print("Baseline cost:", round(baseline, 2))
print("Expected run-rate value:", round(value, 2))
```

### Exercise
Build a cost model for invoice approval, support ticket triage, and weekly management reporting.

### Deliverable
`workflow_cost_model.xlsx`

---

## Lesson 03 — EBITDA basics and the EBITDA bridge

### Goal
Understand EBITDA and build a simple bridge from AI intervention to EBITDA impact.

### Concepts
EBITDA, revenue growth, cost reduction, gross margin improvement, operating leverage, run-rate adjustment, one-time implementation cost, recurring AI/compute cost, EBITDA bridge.

### EBITDA bridge structure

```text
Current EBITDA
+ labor productivity savings
+ SaaS cost reduction
+ outsourcing reduction
+ revenue margin uplift
- AI platform cost
- support / maintenance cost
= Pro forma EBITDA
```

### Sample code

```python
def ebitda_bridge(
    current_ebitda,
    labor_savings=0,
    saas_savings=0,
    outsourcing_savings=0,
    revenue_margin_uplift=0,
    ai_platform_cost=0,
    maintenance_cost=0,
):
    pro_forma = (
        current_ebitda
        + labor_savings
        + saas_savings
        + outsourcing_savings
        + revenue_margin_uplift
        - ai_platform_cost
        - maintenance_cost
    )
    return {
        "current_ebitda": current_ebitda,
        "labor_savings": labor_savings,
        "saas_savings": saas_savings,
        "outsourcing_savings": outsourcing_savings,
        "revenue_margin_uplift": revenue_margin_uplift,
        "ai_platform_cost": -ai_platform_cost,
        "maintenance_cost": -maintenance_cost,
        "pro_forma_ebitda": pro_forma,
        "ebitda_delta": pro_forma - current_ebitda,
    }
```

### Exercise
Create EBITDA bridges for approval automation, customer support copilot, SaaS rationalization, and procurement renewal assistant.

### Deliverable
`ebitda_bridge_template.xlsx`

---

## Lesson 04 — ROI, payback, NPV, and confidence

### Goal
Evaluate whether an AI workflow is worth building.

### Concepts
Implementation cost, recurring cost, annual benefit, net benefit, payback period, ROI, NPV, confidence factors, sensitivity analysis.

### Sample code

```python
def payback_months(initial_investment, annual_net_benefit):
    monthly_benefit = annual_net_benefit / 12
    if monthly_benefit <= 0:
        return None
    return initial_investment / monthly_benefit


def roi(initial_investment, annual_net_benefit):
    return annual_net_benefit / initial_investment


def npv(initial_investment, annual_cash_flows, discount_rate):
    total = -initial_investment
    for year, cash_flow in enumerate(annual_cash_flows, start=1):
        total += cash_flow / ((1 + discount_rate) ** year)
    return total
```

### Exercise
Run sensitivity analysis for adoption rate, AI accuracy, implementation cost, loaded labor cost, and workflow volume.

### Deliverable
`roi_sensitivity_model.ipynb`

---

# Part II — Private equity value creation logic

## Lesson 05 — Private equity value creation playbook

### Goal
Understand how PE managers think about operational improvement.

### Concepts
Buy-and-build, operating leverage, cost takeout, revenue acceleration, working capital improvement, multiple expansion, exit valuation, value creation plan, 100-day plan, portfolio playbooks.

### PE value levers for AI

1. Labor productivity
2. Software/SaaS rationalization
3. Faster sales cycles
4. Lower customer support cost
5. Faster finance close
6. Better pricing and margin control
7. Reduced compliance cost
8. Faster onboarding
9. Reduced expert bottlenecks
10. Working capital improvement

### Exercise
Map 10 AI interventions to PE value levers.

### Deliverable
`pe_ai_value_lever_matrix.md`

---

## Lesson 06 — Cost of friction model

### Goal
Quantify the financial cost of slow, manual, fragmented workflows.

### Concepts
Touch time, wait time, rework, escalation cost, expert interruption, opportunity cost, cost of delay, cost of low-quality data.

### Sample code

```python
def cost_of_friction(
    annual_cases,
    manual_minutes,
    rework_rate,
    rework_minutes,
    loaded_hourly_cost,
    expert_interruptions_per_case=0,
    expert_minutes_per_interruption=0,
    expert_hourly_cost=0,
):
    base = annual_cases * manual_minutes / 60 * loaded_hourly_cost
    rework = annual_cases * rework_rate * rework_minutes / 60 * loaded_hourly_cost
    expert = (
        annual_cases
        * expert_interruptions_per_case
        * expert_minutes_per_interruption
        / 60
        * expert_hourly_cost
    )
    return {
        "base_manual_cost": base,
        "rework_cost": rework,
        "expert_interruption_cost": expert,
        "total_cost_of_friction": base + rework + expert,
    }
```

### Exercise
Estimate the cost of friction for missing invoice fields, repeated support escalations, unclear access review evidence, and manual search across policy documents.

### Deliverable
`cost_of_friction_report.md`

---

## Lesson 07 — Value stream metrics for AI opportunities

### Goal
Translate value stream mapping into measurable AI opportunity analysis.

### Concepts
Lead time, process time, wait time, first-pass yield, rework loop, handoff, bottleneck, throughput, constraint.

### Exercise
Given a process log, compute average lead time, median lead time, process time, wait time, bottleneck step, and rework loop frequency.

### Sample code

```python
import pandas as pd

events = pd.DataFrame({
    "case_id": [1, 1, 1, 2, 2, 2],
    "step": ["submit", "review", "approve", "submit", "review", "approve"],
    "timestamp": pd.to_datetime([
        "2026-01-01 09:00", "2026-01-02 10:00", "2026-01-03 11:00",
        "2026-01-01 10:00", "2026-01-05 14:00", "2026-01-06 15:00",
    ])
})

lead_times = events.groupby("case_id")["timestamp"].agg(lambda s: s.max() - s.min())
print(lead_times)
print("Average lead time:", lead_times.mean())
```

### Deliverable
`value_stream_metrics.ipynb`

---

# Part III — Graph analytics for value creation

## Lesson 08 — From graph bottlenecks to value

### Goal
Use graph analysis to identify high-value AI interventions.

### Concepts
Directed weighted process graph, person-task graph, document-entity graph, user-app-system graph, centrality, betweenness, degree, bottleneck nodes, critical edges, communities.

### Example graph questions

- Who is the hidden bottleneck?
- Which approval path is slowest?
- Which document is central to many workflows?
- Which system creates manual bridges?
- Which team receives incomplete requests?
- Which user group depends on one expert?

### Sample code

```python
import networkx as nx
import pandas as pd

handoffs = pd.DataFrame({
    "from_role": ["Analyst", "Manager", "Manager", "Legal", "Manager", "CFO"],
    "to_role": ["Manager", "Legal", "CFO", "Manager", "AP", "AP"],
    "cases": [120, 80, 60, 30, 100, 40],
    "avg_wait_hours": [12, 30, 48, 20, 10, 72],
})

G = nx.DiGraph()

for _, row in handoffs.iterrows():
    G.add_edge(
        row["from_role"],
        row["to_role"],
        weight=row["cases"],
        avg_wait_hours=row["avg_wait_hours"],
        friction_score=row["cases"] * row["avg_wait_hours"],
    )

centrality = nx.betweenness_centrality(G, weight="avg_wait_hours")
print("Betweenness centrality:", centrality)

edge_friction = sorted(
    G.edges(data=True),
    key=lambda x: x[2]["friction_score"],
    reverse=True,
)

print("Top friction edges:")
for source, target, data in edge_friction:
    print(source, "->", target, data)
```

### Exercise
Build graph models for approval workflow, support escalation, expert dependency network, document reuse graph, and SaaS/system dependency graph.

### Deliverable
`graph_to_value_report.md`

---

## Lesson 09 — Working capital and cash value

### Goal
Understand how AI workflows can affect cash, not only operating expense.

### Concepts
DSO, DPO, inventory days, cash conversion cycle, invoice cycle time, payment terms, early payment discounts, collections prioritization, vendor renewal timing.

### AI opportunities
Invoice intake assistant, collections prioritization agent, payment term anomaly detector, vendor renewal assistant, dispute resolution summarizer.

### Exercise
Estimate working-capital impact from reducing invoice processing delays.

### Deliverable
`working_capital_ai_case.md`

---

## Lesson 10 — SaaS and system dependency rationalization

### Goal
Analyze software spend and system dependencies as PE value levers.

### Concepts
SaaS spend, seat utilization, duplicate tools, shadow IT, manual bridges, system dependency graph, vendor consolidation, replacement vs augmentation, risk of custom replacement.

### Important caution
Do not claim that every SaaS system can be replaced by an AI agent. Often the value comes from reducing seat growth, removing duplicate tools, automating manual bridges, deprecating narrow point solutions, improving utilization, and reducing process workarounds.

### Exercise
Given SSO logs, app usage, and workflow dependencies, identify rationalization opportunities.

### Deliverable
`saas_rationalization_scan.md`

---

## Lesson 11 — AI opportunity scoring for PE value

### Goal
Prioritize AI opportunities by value, feasibility, risk, and adoption.

### Scorecard

```text
AI Opportunity Score =
(value × frequency × reviewability × data availability)
/
(risk × integration complexity × change resistance)
```

### Recommended fields

```text
workflow
pain point
evidence
annual volume
manual effort
cost of friction
AI intervention
implementation effort
governance risk
adoption difficulty
expected run-rate value
payback period
confidence
priority
```

### Sample code

```python
import pandas as pd

opportunities = pd.DataFrame({
    "workflow": ["invoice triage", "support summary", "access review"],
    "value": [9, 8, 7],
    "frequency": [9, 10, 6],
    "reviewability": [8, 9, 8],
    "data_availability": [8, 7, 9],
    "risk": [4, 5, 7],
    "integration_complexity": [5, 4, 6],
    "change_resistance": [4, 3, 5],
})

opportunities["score"] = (
    opportunities["value"]
    * opportunities["frequency"]
    * opportunities["reviewability"]
    * opportunities["data_availability"]
    / (
        opportunities["risk"]
        * opportunities["integration_complexity"]
        * opportunities["change_resistance"]
    )
)

opportunities.sort_values("score", ascending=False)
```

### Deliverable
`ai_opportunity_scorecard.xlsx`

---

## Lesson 12 — Human/AI task split and value protection

### Goal
Design AI workflows that create value without increasing operational risk.

### Concepts
Human-in-the-loop, human-on-the-loop, draft vs execute, reviewability, auditability, decision rights, failure modes, control points, tool permissions.

### Task split model

AI can retrieve, summarize, extract, classify, draft, compare, recommend, and prepare approval packs.

Humans should approve external communication, financial transactions, final legal judgment, high-risk access changes, and ambiguous exceptions.

### Exercise
For each AI opportunity, define what AI reads, writes, drafts, what human approves, what is logged, and which failure modes matter.

### Deliverable
`human_ai_task_split.md`

---

# Part IV — Capstone projects

## Lesson 13 — Capstone: Approval Flow Acceleration Diagnostic

| Field | Content |
|---|---|
| Best buyer | CFO, COO, finance transformation lead |
| Why good entry point | Clear baseline, quick ROI, low privacy sensitivity |
| Core data | ticket/approval logs, timestamps, documents, review comments, approval outcomes |
| Primary graph | Directed weighted process graph |
| AI intervention | Pre-approval pack generator, missing-information checker, approval routing assistant |
| Primary value metrics | cycle time, rework, DSO, finance close speed, manual hours saved |

### Student tasks

1. Build approval process graph.
2. Identify top wait-time edges.
3. Quantify cost of delay.
4. Design AI pre-approval pack.
5. Estimate annual run-rate value.
6. Write CFO-ready recommendation memo.

### Deliverable
`approval_flow_acceleration_report.md`

---

## Lesson 14 — Capstone: Process Knowledge GraphRAG Assistant

| Field | Content |
|---|---|
| Best buyer | COO, shared services lead, head of customer operations |
| Why good entry point | High remote deliverability, strong onboarding and search value |
| Core data | SOPs, policies, tickets, knowledge bases, training documents |
| Primary graph | Document-entity-property graph |
| AI intervention | Citation-grounded Q&A, process summarization, expert interruption reducer |
| Primary value metrics | search time, onboarding time, expert interruption rate, ticket resolution speed |

### Student tasks

1. Build document/entity graph.
2. Identify central policy documents.
3. Detect duplicate or stale knowledge.
4. Design GraphRAG assistant.
5. Estimate search-time and onboarding savings.
6. Create adoption and evaluation plan.

### Deliverable
`knowledge_graphrag_value_case.md`

---

## Lesson 15 — Capstone: Procurement and Invoice Friction Optimizer

| Field | Content |
|---|---|
| Best buyer | CFO, procurement lead |
| Why good entry point | Hits both EBITDA and working capital |
| Core data | POs, invoices, vendors, contracts, approval logs, payment terms |
| Primary graph | Vendor-invoice-contract graph |
| AI intervention | Invoice triage agent, renewal assistant, missing-field checker, payment-term anomaly detector |
| Primary value metrics | processing cost, payment terms, early-payment discounts, late-payment penalties, working capital |

### Student tasks

1. Build vendor-invoice-contract graph.
2. Identify recurring exceptions.
3. Quantify manual processing cost.
4. Identify payment-term value.
5. Design AI triage workflow.
6. Build ROI model.

### Deliverable
`procurement_invoice_optimizer_case.md`

---

## Lesson 16 — Capstone: Access-Risk and Audit Evidence Assistant

| Field | Content |
|---|---|
| Best buyer | CIO, CISO, internal audit |
| Why good entry point | High governance value, strong due-diligence relevance |
| Core data | IAM roles, access logs, control descriptions, audit findings, policy documents, remediation tickets |
| Primary graph | Access-permission-policy graph |
| AI intervention | Audit evidence pack generator, remediation draft assistant, access anomaly explainer |
| Primary value metrics | audit effort, exception count, risk exposure, remediation cycle time |

### Student tasks

1. Build user-role-permission graph.
2. Identify overprivileged nodes.
3. Connect policy requirements to evidence.
4. Design audit evidence assistant.
5. Quantify audit effort savings.
6. Propose governance controls.

### Deliverable
`access_risk_audit_assistant_case.md`

---

## Lesson 17 — Capstone: SaaS and System Dependency Rationalization Scan

| Field | Content |
|---|---|
| Best buyer | CIO, transformation office, PE operating partner |
| Why good entry point | Common PE pain point, highly reusable across portfolios |
| Core data | SSO logs, app usage, SaaS spend, system inventory, data lineage, manual export/import records |
| Primary graph | User-app-system graph |
| AI intervention | Consolidation recommender, lineage explainer, manual bridge detector, SaaS usage analyst |
| Primary value metrics | SaaS spend, manual bridge cost, operational risk, seat utilization, system consolidation value |

### Student tasks

1. Build user-app-system graph.
2. Identify low-utilization high-cost tools.
3. Identify duplicate systems.
4. Identify manual bridges.
5. Propose AI-assisted rationalization plan.
6. Estimate run-rate value.

### Deliverable
`saas_system_dependency_scan.md`

---

## Lesson 18 — Portfolio AI Value Creation Playbook

### Goal
Combine all skills into a PE-style portfolio playbook.

### Student tasks

Given five portfolio-company cases:

1. Identify workflow value opportunities.
2. Build process/graph evidence.
3. Estimate cost of friction.
4. Score AI opportunities.
5. Select top 3 initiatives.
6. Build EBITDA bridge.
7. Estimate enterprise value impact.
8. Recommend 90-day implementation roadmap.
9. Define reusable patterns across companies.

### Deliverable
`portfolio_ai_value_creation_playbook.md`

---

# 5. Reusable report templates

## Template: AI value case

```markdown
# AI Value Case: [Workflow Name]

## 1. Executive summary

## 2. Current-state workflow

## 3. Evidence used

## 4. Baseline metrics

| Metric | Value |
|---|---:|
| Annual volume | |
| Manual minutes per case | |
| Loaded hourly cost | |
| Rework rate | |
| Cycle time | |

## 5. Cost of friction

## 6. Graph/process findings

## 7. Proposed AI intervention

## 8. Human/AI task split

## 9. Expected value

| Metric | Estimate |
|---|---:|
| Annual run-rate savings | |
| Implementation cost | |
| Recurring AI cost | |
| Payback months | |
| EBITDA impact | |
| Enterprise value impact | |

## 10. Risks and controls

## 11. 90-day implementation roadmap

## 12. Recommendation
```

## Template: Executive PE memo

```markdown
# PE AI Value Creation Memo

## Situation

## Workflow friction observed

## Financial baseline

## AI opportunity

## Expected EBITDA impact

## Implementation plan

## Risks and mitigations

## Decision needed
```

---

# 6. AI agent implementation instructions

Use this section as the prompt for a coding AI agent.

```text
You are building a repo called `pe-ai-value-masterclass`.

Goal:
Create a practical course for AI engineers and graph analysts to learn financial value calculation, EBITDA impact, ROI, payback, and PE-style value creation through graph and AI workflow use cases.

Style:
- Runnable local notebooks
- Synthetic business datasets
- Progressive lessons from basics to capstones
- Each lesson must contain:
  1. Business problem
  2. Learning goals
  3. Concepts explained simply
  4. Synthetic dataset
  5. Python analysis
  6. Value calculation
  7. AI intervention design
  8. Exercises
  9. Deliverable template
  10. Tests or validation checks

Technology:
- Python 3.11+
- pandas
- numpy
- networkx
- matplotlib
- openpyxl
- pytest
- ruff
- optional duckdb
- optional neo4j

Repository structure:
- notebooks/
- src/data_generation/
- src/value_models/
- src/graph_value/
- src/reporting/
- skills/
- reports/templates/
- tests/

Implementation rules:
- Use only synthetic data.
- Do not use real company data.
- Keep examples realistic but simple.
- Include unit tests for value formulas.
- Use deterministic random seeds.
- Keep notebooks executable from top to bottom.
- Add markdown explanations before code.
- Use plain matplotlib only.
- Avoid overcomplicated financial modeling in early lessons.
- Add progressively harder exercises.
- Include capstone projects tied to:
  approval flow acceleration,
  process knowledge GraphRAG,
  procurement/invoice optimization,
  access-risk audit assistant,
  SaaS/system dependency rationalization,
  portfolio AI value creation.

Core value formulas to implement:
- annual manual cost
- cost of friction
- expected run-rate value
- ROI
- payback period
- NPV
- EBITDA bridge
- enterprise value impact
- FTE capacity release
- sensitivity analysis

Expected deliverables:
- full lesson notebooks
- reusable value_model.py functions
- synthetic dataset generators
- report templates
- README.md
- MASTER_LESSONS.md
- tests
```

---

# 7. Suggested Python module skeleton

```python
# src/value_models/basic.py

from __future__ import annotations

from dataclasses import dataclass
from typing import Iterable


def annual_manual_cost(
    annual_volume: float,
    minutes_per_case: float,
    loaded_hourly_cost: float,
) -> float:
    return annual_volume * (minutes_per_case / 60.0) * loaded_hourly_cost


def expected_run_rate_value(
    annual_volume: float,
    minutes_per_case: float,
    loaded_hourly_cost: float,
    reduction_pct: float,
    adoption_pct: float = 1.0,
    confidence: float = 1.0,
) -> float:
    baseline = annual_manual_cost(
        annual_volume=annual_volume,
        minutes_per_case=minutes_per_case,
        loaded_hourly_cost=loaded_hourly_cost,
    )
    return baseline * reduction_pct * adoption_pct * confidence


def payback_months(initial_investment: float, annual_net_benefit: float) -> float | None:
    monthly_benefit = annual_net_benefit / 12.0
    if monthly_benefit <= 0:
        return None
    return initial_investment / monthly_benefit


def roi(initial_investment: float, annual_net_benefit: float) -> float:
    if initial_investment <= 0:
        raise ValueError("initial_investment must be positive")
    return annual_net_benefit / initial_investment


def npv(
    initial_investment: float,
    annual_cash_flows: Iterable[float],
    discount_rate: float,
) -> float:
    value = -initial_investment
    for year, cash_flow in enumerate(annual_cash_flows, start=1):
        value += cash_flow / ((1.0 + discount_rate) ** year)
    return value


def enterprise_value_impact(ebitda_delta: float, exit_multiple: float) -> float:
    return ebitda_delta * exit_multiple


@dataclass(frozen=True)
class EbitdaBridge:
    current_ebitda: float
    labor_savings: float = 0.0
    saas_savings: float = 0.0
    outsourcing_savings: float = 0.0
    revenue_margin_uplift: float = 0.0
    working_capital_operating_benefit: float = 0.0
    ai_platform_cost: float = 0.0
    maintenance_cost: float = 0.0

    @property
    def pro_forma_ebitda(self) -> float:
        return (
            self.current_ebitda
            + self.labor_savings
            + self.saas_savings
            + self.outsourcing_savings
            + self.revenue_margin_uplift
            + self.working_capital_operating_benefit
            - self.ai_platform_cost
            - self.maintenance_cost
        )

    @property
    def ebitda_delta(self) -> float:
        return self.pro_forma_ebitda - self.current_ebitda
```

---

# 8. Suggested graph-value helper skeleton

```python
# src/graph_value/process_graph.py

from __future__ import annotations

import networkx as nx
import pandas as pd


def build_handoff_graph(
    handoff_df: pd.DataFrame,
    source_col: str = "from_role",
    target_col: str = "to_role",
    case_count_col: str = "cases",
    wait_hours_col: str = "avg_wait_hours",
) -> nx.DiGraph:
    required = {source_col, target_col, case_count_col, wait_hours_col}
    missing = required - set(handoff_df.columns)
    if missing:
        raise ValueError(f"Missing required columns: {missing}")

    graph = nx.DiGraph()

    for _, row in handoff_df.iterrows():
        cases = float(row[case_count_col])
        wait_hours = float(row[wait_hours_col])
        graph.add_edge(
            row[source_col],
            row[target_col],
            cases=cases,
            avg_wait_hours=wait_hours,
            friction_score=cases * wait_hours,
        )

    return graph


def top_friction_edges(graph: nx.DiGraph, n: int = 10) -> list[tuple[str, str, dict]]:
    return sorted(
        graph.edges(data=True),
        key=lambda edge: edge[2].get("friction_score", 0),
        reverse=True,
    )[:n]


def node_bottleneck_scores(graph: nx.DiGraph) -> pd.DataFrame:
    betweenness = nx.betweenness_centrality(graph, weight="avg_wait_hours")
    in_degree = dict(graph.in_degree(weight="cases"))
    out_degree = dict(graph.out_degree(weight="cases"))

    rows = []
    for node in graph.nodes:
        rows.append({
            "node": node,
            "betweenness": betweenness.get(node, 0.0),
            "weighted_in_degree": in_degree.get(node, 0.0),
            "weighted_out_degree": out_degree.get(node, 0.0),
        })

    return pd.DataFrame(rows).sort_values(
        ["betweenness", "weighted_in_degree"],
        ascending=False,
    )
```

---

# 9. Suggested first build order

1. Create repository structure.
2. Implement `src/value_models/basic.py`.
3. Add tests for value formulas.
4. Create Lesson 00 (integrated notebook) and lessons 01–04 first.
5. Generate synthetic workflow datasets.
6. Create graph-value helper functions.
7. Build lessons 08 and 13 as early proof of concept.
8. Add capstones one by one.
9. Create report templates.
10. Add README and MASTER_LESSONS.

---

# 10. Course positioning

Recommended public title:

```text
Private Equity Value Masterclass for AI and Graph Engineers
```

Alternative title:

```text
AI Value Creation Masterclass: EBITDA, Graph Analytics, and Agentic Workflow ROI
```

Best subtitle:

```text
Learn to translate workflow bottlenecks, graph findings, and AI automation ideas into ROI, EBITDA impact, and PE-style value creation cases.
```
