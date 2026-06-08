# Incident Management Process

**Owner:** Sara Collins (Service Desk Lead)  
**Accountable:** IT Manager  
**Version:** 1.0  
**Last Updated:** March 2026

---

## 1. Purpose

This process defines how Gulf Horizon Energy IT manages service disruptions from detection to resolution and post-incident review. It applies to all IT-managed systems across Dammam HQ, Dubai office, and field operations.

---

## 2. Scope

- **Users:** All 450 GHE users
- **Systems:** Oracle EBS, SAP, Microsoft 365, SCADA interface, Azure services, MPLS WAN, field tablets
- **IT Staff:** All 9 IT team members (Dammam + Dubai)

---

## 3. Priority Matrix

| Priority | Definition | Response Target | Resolution Target | IT Manager Role | GHE Example |
|----------|------------|----------------|-------------------|-----------------|-------------|
| **P1 - Critical** | Full service outage or compliance risk | 15 minutes | 4 hours | Activated immediately. Briefs CIO within 30 min. Owns resolution and communication. | INC-006: ERP01 down 90 min. INC-003: Dubai VPN offline 45 min. |
| **P2 - High** | Major degradation, multiple users affected | 30 minutes | 8 hours | Notified within 30 min. Monitors resolution. Briefs VP Operations if field affected. | INC-001: Dubai MPLS packet loss. INC-005: Terminated account breach. |
| **P3 - Medium** | Single user/team impacted, workaround available | 2 hours | Next business day | Reviewed in daily stand-up. Sara Collins manages as Service Desk Lead. | INC-002: ERP report timeout. INC-007: Field tablet patch failure. |
| **P4 - Low** | Minor issue, no productivity impact | 4 hours | 5 business days | Reviewed in weekly report. Tyler Park and Noelle Gagne handle at L1. | Password resets, access provisioning, standard service requests. |

---

## 4. Process Flow (6 Steps)

| Step | Action | Owner |
|------|--------|-------|
| 1 | **Detect** — User reports issue or monitoring alert triggers | User / PRTG |
| 2 | **Log** — Create ticket in ITSM system | Service Desk |
| 3 | **Triage** — Assign priority (P1–P4) based on matrix | Sara Collins |
| 4 | **Assign** — Route to appropriate team member | Sara Collins |
| 5 | **Resolve** — Fix the issue or implement workaround | Assigned owner |
| 6 | **Close** — Verify resolution, update ticket, close | Service Desk |

---

## 5. Escalation Path

| Priority | Escalation | Timeframe |
|----------|------------|-----------|
| P3 / P4 | Sara Collins (Service Desk Lead) handles | Immediate |
| P2 | Sara notifies IT Manager | Within 30 minutes |
| P1 | IT Manager activated immediately. Briefs Linda Hartley (CIO) | Within 30 minutes |
| P1 (field or ERP affected) | Brief David Marsh (VP Operations) | Within 30 minutes |
| P1 (financial systems affected) | Brief Robert Chen (CFO) | Within 30 minutes |

---

## 6. IT Manager Activation Criteria

IT Manager is activated immediately when ANY of the following occur:

- Any P1 incident
- Any P2 affecting Oracle EBS, SCADA, or Dubai connectivity
- Any security incident regardless of priority

---

## 7. Post-Incident Review (PIR) Requirement

| Requirement | Detail |
|-------------|--------|
| **When** | All P1 and P2 incidents |
| **Deadline** | Within 48 hours of resolution |
| **Owner** | IT Manager |
| **Format** | Documented RCA + corrective actions |
| **Review** | Standing agenda item at Tuesday CAB meeting |

**PIR must answer:**
1. What happened?
2. Why did it happen? (Root cause)
3. What is being done to prevent recurrence?
4. Who owns each corrective action?
5. What is the deadline?

---

## 8. Incident Log Reference

| Incident ID | Date | Priority | Description | Resolution Time | PIR Complete? |
|-------------|------|----------|-------------|-----------------|---------------|
| INC-003 | 3 Feb 2026 | P1 | Dubai VPN offline (STC routing failure) | 5.2 hours | Overdue — reinstated |
| INC-006 | 1 Mar 2026 | P1 | ERP01 unresponsive (Oracle memory exhaustion) | 90 minutes | In progress |
| INC-001 | Ongoing | P2 | Dubai MPLS packet loss | — | Pending |
| INC-005 | Ongoing | P2 | Terminated accounts with active access | — | Pending |
| INC-002 | Ongoing | P3 | ERP report timeout | — | N/A |
| INC-007 | Ongoing | P3 | Field tablet patch failure | — | N/A |

---

*Gulf Horizon Energy — Simulated Environment | All data is fictional for portfolio purposes*