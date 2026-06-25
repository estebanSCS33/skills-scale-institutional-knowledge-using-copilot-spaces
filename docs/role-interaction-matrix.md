# Role Interaction Matrix

This document clarifies how different OctoAcme personas interact, communicate, and hand off work across project phases.

## Purpose
Reduce ambiguity around accountability, decision authority, and cross-functional dependencies by mapping explicit interactions between roles.

---

## Interaction Legend

- **D** = Directly Responsible (makes decisions, executes)
- **C** = Consulted (provides input, advises)
- **I** = Informed (kept in the loop, receives updates)
- **A** = Approves (gates/validates, can block)

---

## Project Initiation

| Activity | Dev | QA | PdM | PM | Architect | Sponsor | Support |
|----------|-----|-----|-----|-----|-----------|---------|---------|
| Define problem statement | I | I | D | C | I | A | C |
| Create One-pager | I | I | D | D | C | A | I |
| Identify success metrics | I | C | D | C | I | A | C |
| Assess technical feasibility | C | I | C | C | D | I | I |
| Customer need validation | I | I | C | C | I | I | D |
| Resource allocation | C | C | C | C | C | D | I |
| Approve to proceed to planning | I | I | C | C | C | D | I |

---

## Project Planning

| Activity | Dev | QA | PdM | PM | Architect | Sponsor | Support |
|----------|-----|-----|-----|-----|-----------|---------|---------|
| Backlog creation & prioritization | I | C | D | C | C | I | C |
| Acceptance criteria definition | D | D | D | C | C | I | C |
| Effort estimation | D | D | I | C | D | I | I |
| Test plan development | C | D | C | I | I | I | I |
| Architecture & design review | D | I | C | I | D | I | I |
| Risk identification | C | C | C | D | D | C | C |
| Release timeline agreement | C | C | C | D | C | A | C |
| Support documentation planning | I | I | C | C | I | I | D |

---

## Sprint/Iteration Planning

| Activity | Dev | QA | PdM | PM | Architect | Sponsor | Support |
|----------|-----|-----|-----|-----|-----------|---------|---------|
| Select backlog items | D | I | D | C | C | I | I |
| Confirm DoD | D | D | C | C | C | I | I |
| Task breakdown | D | C | C | I | C | I | I |
| Capacity planning | D | C | I | D | I | I | I |
| Dependency mapping | C | I | C | D | D | I | I |

---

## Execution & Development

| Activity | Dev | QA | PdM | PM | Architect | Sponsor | Support |
|----------|-----|-----|-----|-----|-----------|---------|---------|
| Implement feature | D | I | I | I | C | I | I |
| Write unit tests | D | C | I | I | C | I | I |
| Code review | D | I | C | I | C | I | I |
| Architecture review | C | I | I | I | D | I | I |
| Design documentation | D | I | I | I | D | I | I |
| Daily standup | D | D | C | D | I | I | I |
| Report blockers | D | D | I | D | C | I | C |

---

## Testing & QA

| Activity | Dev | QA | PdM | PM | Architect | Sponsor | Support |
|----------|-----|-----|-----|-----|-----------|---------|---------|
| Test case creation | C | D | C | I | I | I | I |
| Test execution | I | D | I | I | I | I | I |
| Bug triage | D | D | C | C | C | I | I |
| Acceptance validation | C | D | D | I | I | I | I |
| Performance testing | C | D | I | I | D | I | I |
| Security validation | C | C | I | I | D | I | I |

---

## Release & Deployment

| Activity | Dev | QA | PdM | PM | Architect | Sponsor | Support |
|----------|-----|-----|-----|-----|-----------|---------|---------|
| Release notes creation | C | C | D | D | I | I | C |
| Deployment planning | C | I | I | D | D | I | I |
| Pre-deployment testing | I | D | I | I | C | I | I |
| Deployment execution | D | I | I | C | D | I | I |
| Post-deployment validation | D | D | I | I | D | I | I |
| Customer communication | I | I | C | C | I | C | D |
| Support runbook update | I | I | C | C | I | I | D |
| Performance monitoring | D | I | I | I | D | I | I |

---

## Incident Response

| Activity | Dev | QA | PdM | PM | Architect | Sponsor | Support |
|----------|-----|-----|-----|-----|-----------|---------|---------|
| Incident triage | D | D | C | D | C | I | D |
| Root cause investigation | D | C | I | I | D | I | I |
| Fix implementation | D | I | I | I | C | I | I |
| Hotfix testing | I | D | I | I | C | I | I |
| Hotfix deployment | D | C | I | C | D | I | I |
| Customer notification | I | I | C | D | I | I | D |
| Post-incident review | D | D | C | D | D | C | D |

---

## Retrospective & Improvement

| Activity | Dev | QA | PdM | PM | Architect | Sponsor | Support |
|----------|-----|-----|-----|-----|-----------|---------|---------|
| Conduct retrospective | D | D | D | D | D | I | D |
| Identify action items | D | D | D | D | D | I | D |
| Track improvements | I | I | I | D | I | I | I |
| Success metrics review | C | C | D | C | I | A | C |
| Process improvement | C | C | C | D | D | I | I |

---

## Key Insights from This Matrix

### Decision Authority
- **Product Manager**: Feature prioritization, success metrics, customer value
- **Technical Architect**: Technical design, feasibility, risk mitigation
- **Project Manager**: Timeline, scope, resource allocation, escalation
- **Sponsor**: Budget, strategic alignment, project approval
- **QA/Testing Lead**: Quality gates, release readiness

### High-Touch Handoffs (Require Explicit Communication)
1. **Planning → Execution**: Backlog clarity, acceptance criteria, test plans
2. **Development → QA**: Code complete, test coverage, known issues
3. **QA → Release**: Quality sign-off, known issues documented, release notes
4. **Release → Support**: Documentation, runbooks, customer comms

### Common Friction Points & Mitigations
| Friction Point | Roles Involved | Mitigation |
|---|---|---|
| Unclear acceptance criteria | Dev, QA, PdM | Written, reviewed before sprint starts |
| Scope creep during execution | Dev, PM, PdM | Change request process; explicit trade-offs |
| Late QA involvement | QA, Dev, PM | QA joins planning; embedded in daily standups |
| Architectural misalignment | Dev, Architect, PM | Design review in planning; code review checkpoints |
| Surprise customer impact | Support, PdM, Dev | Support included in planning; customer feedback loops |
| Stakeholder misalignment | Sponsor, PM, PdM | Monthly updates; clear success metrics |

---

## Using This Matrix

1. **Clarify Decisions**: When unsure who decides, check the "D" cells
2. **Identify Consulted Parties**: Check "C" cells to know who needs input
3. **Plan Communication**: Check "I" cells for who needs to be kept updated
4. **Gate Activities**: Check "A" cells for approval requirements
5. **Resolve Conflicts**: Reference this matrix to clarify role boundaries
