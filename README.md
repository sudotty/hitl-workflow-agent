# Human-in-the-loop Workflow Agent

A human-in-the-loop workflow agent for invoice reconciliation, policy checks, risk scoring, tool dry-runs, and auditable approvals.

This project focuses on a realistic enterprise pattern: AI prepares the work, but humans approve risky actions.

## Why this project exists

Most companies do not want fully autonomous agents making financial, operational, or permission-changing decisions. They want agents that can reduce manual work while preserving control, auditability, and accountability.

The goal is not full autonomy. The goal is safe delegation.

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
Prepare tool dry-run
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
| Structured extraction | Extract vendor, amount, invoice id, due date, PO number |
| Policy checks | Enforce rules before execution |
| Risk scoring | Low / medium / high risk classification |
| Action plan | Explain what the agent wants to do |
| Tool dry-run | Preview external system changes |
| Approval gate | Approve, reject, or request changes |
| Workflow state | Pause and resume agent execution |
| Audit trail | Record facts, rules, decisions, and tool calls |

## Interview value

This project helps explain how AI agents enter real business workflows, where humans should remain in the loop, and how auditability makes automation trustworthy.

## Status

Planning and scaffolding. Issues are used as the implementation roadmap.
