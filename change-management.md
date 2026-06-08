# Change Management Process + CAB Charter

**Owner:** IT Manager  
**Accountable:** IT Manager  
**Version:** 1.0  
**Last Updated:** March 2026

> **Why this exists:** INC-006 — an Oracle job with no owner and no change control brought down Finance for 90 minutes. This document prevents that from happening again.

---

## 1. Purpose

This process defines how Gulf Horizon Energy IT manages changes to IT systems — from request through approval to implementation and review. It applies to all changes to production systems, configuration items, and IT services.

---

## 2. Change Type Definitions

| Change Type | Definition | Approval Path | GHE Example |
|-------------|------------|---------------|-------------|
| **Standard** | Pre-approved, low risk, repeatable. Follows defined procedure. | No CAB needed — pre-approved template | Monthly Windows patching (Laura Mitchell). Firewall rule updates (Kevin Walsh). These are already happening — just not documented as standard changes. |
| **Normal** | Planned change requiring risk assessment and CAB approval | CAB review — IT Manager chairs. 48-hour advance submission required | ERP01 Oracle job scheduling policy (post INC-006). STC WAN configuration changes. Azure DR script updates (INC-010). Cisco switch stack replacement (planned Q2). |
| **Emergency** | Urgent change needed to restore service or prevent critical failure | IT Manager approves with one business sign-off. Post-implementation review mandatory | INC-006 remediation: killing Oracle process and locking USR-022 account. INC-003: STC routing table restoration. |

---

## 3. Change Request Form Fields

Every Normal change requires a completed request form with these fields:

| Field | Description |
|-------|-------------|
| Change ID | Auto-generated (CHG-XXX) |
| Date Submitted | DD-MMM-YYYY |
| Requested By | Name and role |
| Change Type | Standard / Normal / Emergency |
| System Affected | Oracle EBS / SAP / M365 / SCADA / Azure / MPLS WAN / Field Tablets / Other |
| Description | What is being changed? (2-3 sentences) |
| Business Justification | Why is this needed? What problem does it solve? |
| Risk Assessment | Low / Medium / High |
| Impact if Change Fails | What breaks? Who is affected? |
| Rollback Plan | Exact steps to undo the change |
| Proposed Implementation Date | Date and time window |
| CAB Approval Signature | Leave blank — filled at CAB meeting |

---

## 4. CAB Charter

| Item | Detail |
|------|--------|
| **Chair** | IT Manager |
| **Members** | Kevin Walsh (Network), Laura Mitchell (Systems), Greg Thompson (ERP), Sara Collins (Service Desk), Owen Bradley (Security) |
| **Meeting Cadence** | Every Tuesday, 10am Dammam time |
| **Duration** | 30 minutes |
| **Quorum** | IT Manager + 2 members |
| **Advance Submission** | 48 hours for Normal changes (submitted by Sunday 10am for Tuesday CAB) |
| **Change Freeze Window** | Last 3 business days of each month (month-end close) |
| **Maintenance Window** | Sunday 1:00am – 5:00am Dammam time |

**CAB Agenda (30 minutes):**
- 5 min: Review previous changes (success/fail)
- 15 min: Review Normal changes submitted (max 5 per meeting)
- 5 min: Emergency changes from past week (post-implementation review)
- 5 min: Upcoming freeze window + exceptions

---

## 5. Rollback Requirement

All Normal changes must have a documented rollback plan that includes:

1. **Step-by-step commands** to revert the change
2. **Estimated time** to complete rollback
3. **Who executes** the rollback (name and role)
4. **Success criteria** — how do you know rollback worked?
5. **Testing evidence** — rollback tested in non-production where feasible

> **No rollback plan = No CAB approval.**

---

## 6. Change Calendar Policy

| Rule | Detail |
|------|--------|
| **Freeze Window** | Last 3 business days of each month (month-end close) |
| **Freeze Restriction** | No Normal changes during freeze window |
| **Freeze Exception** | Requires IT Manager + CIO written approval |
| **Emergency Change During Freeze** | Requires IT Manager + CIO approval |
| **Maintenance Window** | Sunday 1:00am – 5:00am (preferred for Normal changes) |
| **Change Blackout** | No changes 24 hours before any P1 incident PIR deadline |

---

## 7. Change Log Reference

| Change ID | Date | Type | System | Description | Status | Approved By |
|-----------|------|------|--------|-------------|--------|--------------|
| CHG-001 | Post INC-006 | Emergency | Oracle EBS | Kill Oracle processes + lock USR-022 account | Completed | IT Manager + CIO |
| CHG-002 | Pending | Normal | Oracle EBS | Oracle job scheduling policy with owner assignment | Pending CAB | — |
| CHG-003 | Pending | Normal | Azure | DR failover script fix (INC-010 remediation) | Pending CAB | — |
| CHG-004 | Planned Q2 | Normal | Network | Cisco Catalyst 9300 switch stack replacement | Draft | — |

---

## 8. Emergency Change Process

**Trigger:** Service outage, security incident, or imminent critical failure

**Steps:**
1. IT Manager assesses and approves (verbal approval acceptable)
2. One business sign-off obtained (CIO or VP Operations depending on system)
3. Change executed immediately
4. Change request form completed within 24 hours
5. Post-implementation review at next CAB meeting

**Emergency change approvers by system:**

| System Affected | Required Approver |
|----------------|-------------------|
| Oracle EBS (Finance) | IT Manager + CFO Robert Chen |
| SCADA / Field Operations | IT Manager + VP Operations David Marsh |
| Any security incident | IT Manager + CIO Linda Hartley |
| All other systems | IT Manager only |

---

*Gulf Horizon Energy — Simulated Environment | All data is fictional for portfolio purposes*