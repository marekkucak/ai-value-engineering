# Graph Bottleneck to Value Report

**Prepared by:** [Analyst Name]  
**Date:** [YYYY-MM-DD]  
**Scope:** [Workflow / Business Unit / Department]  
**Source data:** Process logs [start date] – [end date]

---

## 1. Executive Summary

| Item | Detail |
|------|--------|
| Workflows analysed | [n] |
| Total nodes in graph | [n] |
| Top structural bottleneck | [Node Name] (betweenness = [x.xx]) |
| Highest friction edge | [From] → [To] ([n] cases × [n] h = [n] friction units) |
| Total addressable friction (EUR) | EUR [n,nnn] |
| Recommended first AI action | [brief description] |
| Expected annual saving | EUR [n,nnn] |

---

## 2. Workflow Graph Analysis

### Graph Overview

| Workflow | Nodes | Edges | Top Bottleneck Node | Betweenness | Top Friction Edge | Friction Score |
|----------|-------|-------|---------------------|-------------|-------------------|---------------|
| [Workflow 1] | [n] | [n] | [Node] | [0.xx] | [From → To] | [n,nnn] |
| [Workflow 2] | [n] | [n] | [Node] | [0.xx] | [From → To] | [n,nnn] |
| [Workflow 3] | [n] | [n] | [Node] | [0.xx] | [From → To] | [n,nnn] |

### Graph Types Used

- [ ] Person-task graph (who does what: approval flows, escalation networks)
- [ ] Document-entity graph (which artefacts are reused across workflows)
- [ ] System dependency graph (which systems create manual bridges)

---

## 3. Bottleneck Details

### [Workflow 1] — [Workflow Name]

**Top bottleneck node:** [Node Name]  
**Betweenness centrality:** [0.xx] (sits on [xx]% of all case paths)  
**L06 friction cost:** EUR [n,nnn] per year ([n]% of total workflow cost)  
**L07 lead time impact:** +[n] days when node is congested  

**Graph evidence:**
- In-degree: [n] (receives handoffs from [n] different roles)
- Out-degree: [n] (hands off to [n] different roles)
- Cases through node: [n,nnn] per year
- Average wait time at node: [n] hours

**Friction edges involving this node:**

| Edge | Cases/Year | Avg Wait (h) | Friction Score |
|------|-----------|-------------|---------------|
| [From] → [Node] | [n,nnn] | [n] | [n,nnn] |
| [Node] → [To] | [n,nnn] | [n] | [n,nnn] |

---

### [Workflow 2] — [Workflow Name]

*(repeat section above)*

---

### [Workflow 3] — [Workflow Name]

*(repeat section above)*

---

## 4. Recommended AI Interventions

Ranked by expected friction reduction (highest first):

### Intervention 1 — [Title]

| Item | Detail |
|------|--------|
| Target workflow | [Workflow Name] |
| Target node/edge | [Node or From → To] |
| Current state | [n]% escalation / [n] h wait / [n]% rework rate |
| AI solution | [LLM classifier / Rule-based approval / Auto-routing / etc.] |
| Target state | [n]% escalation / [n] h wait / [n]% rework rate |
| Friction units removed | [n,nnn] |
| L06 friction EUR removed | EUR [n,nnn] |
| Betweenness change | [0.xx] → [0.xx] |
| Implementation effort | [Low / Medium / High] |

**Rationale:** [2–3 sentences explaining why this intervention is highest priority based on graph evidence]

---

### Intervention 2 — [Title]

*(repeat table above)*

---

### Intervention 3 — [Title]

*(repeat table above)*

---

## 5. Expected Financial Impact

| Intervention | Annual Saving (EUR) | Confidence | Payback Period |
|-------------|---------------------|-----------|----------------|
| [Intervention 1] | EUR [n,nnn] | [High/Medium/Low] | [n months] |
| [Intervention 2] | EUR [n,nnn] | [High/Medium/Low] | [n months] |
| [Intervention 3] | EUR [n,nnn] | [High/Medium/Low] | [n months] |
| **Total** | **EUR [n,nnn]** | | |

**Note:** Savings calculated as reduction in L06 friction cost components.  
Formula: `annual_cases × (old_rate - new_rate) × minutes_per_case / 60 × hourly_rate`

---

## 6. Implementation Priority

### Recommended Sequence

1. **[Intervention 1]** — Start here
   - Highest EUR saving
   - [x.xx] → [x.xx] betweenness reduction on [Node]
   - Data required: [list data sources needed]
   - Estimated time to value: [n weeks]

2. **[Intervention 2]** — Second priority
   - [Rationale: why second, not first]
   - Depends on: [any dependency on Intervention 1 data or infrastructure]
   - Estimated time to value: [n weeks]

3. **[Intervention 3]** — Third priority
   - [Rationale]
   - Estimated time to value: [n weeks]

### Risk Factors

| Risk | Likelihood | Impact | Mitigation |
|------|-----------|--------|-----------|
| [Risk 1] | [H/M/L] | [H/M/L] | [Mitigation action] |
| [Risk 2] | [H/M/L] | [H/M/L] | [Mitigation action] |

---

## 7. Appendix

### A. Graph Metrics Glossary

| Metric | Definition | How to read it |
|--------|-----------|----------------|
| **Betweenness centrality** | Fraction of all shortest paths that pass through this node | 0 = not on any shortest path; 1 = on every shortest path |
| **Degree centrality** | Normalised count of direct connections | Higher = more directly connected to other nodes |
| **Friction score** | `cases × avg_wait_hours` for an edge | Higher = more total waiting time accumulated on this handoff |
| **In-degree** | Number of incoming edges | Higher = receives work from more different sources |
| **Out-degree** | Number of outgoing edges | Higher = hands off work to more different destinations |

### B. Data Sources

| Source | Description | Date Range |
|--------|-------------|-----------|
| [System 1] | [Description] | [Start] – [End] |
| [System 2] | [Description] | [Start] – [End] |

### C. Assumptions and Limitations

- Handoff data derived from [source system]; excludes [any exclusions]
- Wait times are averages; actual distribution may have high variance (see L07 metrics)
- Centrality scores reflect the Q[n] [year] period only; seasonal variation not modelled
- EUR friction values use loaded hourly costs from L06: Analyst EUR 55/hr, Expert EUR 75–90/hr
