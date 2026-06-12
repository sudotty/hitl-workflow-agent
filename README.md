# Human-in-the-loop Workflow Agent

A human-in-the-loop workflow agent for invoice reconciliation, policy checks, risk scoring, tool dry-runs, and auditable approvals.

This project focuses on a realistic enterprise pattern: AI prepares the work, but humans approve sensitive actions.

## Why this project exists

Most companies do not want fully autonomous agents making financial, operational, or permission-changing decisions. They want agents that can reduce manual work while preserving control, auditability, and accountability.

The goal is not full autonomy. The goal is safe delegation.

## MVP target

Build an invoice reconciliation and payment approval workflow where the agent extracts facts, checks policy, scores risk, previews the action, pauses for human review, and records an audit trail.

```text
invoice -> structured extraction -> validation -> policy checks -> risk score -> preview -> approval -> mock execution -> audit trail
```

## Prioritized roadmap

| Priority | Workstream | Outcome |
|---|---|---|
| P0 / MVP | Invoice workflow definition | The business process is concrete and understandable |
| P0 / MVP | Structured extraction and validation | The agent works with facts, not loose text |
| P0 / MVP | Policy checks and risk scoring | The system explains why a case needs review |
| P1 | Preview and approval UI | Humans can approve, reject, or request changes |
| P1 | Mock ERP/payment execution and audit | The workflow closes the loop without touching real systems |
| P1 | Workflow evaluation cases | Business rules can be regression-tested |
| P2 | Interview notes and demo | The project is easy to explain to operations and AI teams |

## Demo use case

Vendor invoice reconciliation and payment approval.

```text
Invoice / payment request
  ↓
Extract structured fields
  ↓
Validate vendor and invoice data
  ↓
Check policies: amount threshold, duplicate payment, missing PO
  ↓
Score risk
  ↓
Prepare action preview
  ↓
Pause for human approval
  ↓
Execute mock ERP / payment action
  ↓
Write audit trail
```

## Core features

| Feature | Purpose |
|---|---|
| Invoice intake | Accept sample invoice/payment requests |
| Structured extraction | Extract vendor, amount, invoice id, due date, purchase order number |
| Policy checks | Enforce business rules before execution |
| Risk scoring | Low / medium / high risk classification |
| Action plan | Explain what the agent wants to do |
| Preview mode | Preview external system changes |
| Approval gate | Approve, reject, or request changes |
| Workflow state | Pause and resume execution |
| Audit trail | Record facts, rules, decisions, and external actions |

## Interview value

This project helps explain how AI agents enter real business workflows, where humans should remain in the loop, and how auditability makes automation trustworthy.

## Status

Planning and scaffolding. Issues are used as the implementation roadmap.
