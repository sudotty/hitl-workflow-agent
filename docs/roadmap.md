# Roadmap

## Phase 1: Workflow definition

- Define invoice and payment request data shape.
- Prepare sample invoices and vendor records.
- Define workflow states: intake, extract, validate, risk score, preview, approval wait, execute, audit, failed.

## Phase 2: Extraction and validation

- Implement structured extraction schema.
- Validate vendor, amount, invoice id, due date, and purchase order number.
- Add duplicate payment and missing purchase order checks.

## Phase 3: Risk and approval

- Implement risk scoring.
- Generate action plan and business explanation.
- Add approval actions: approve, reject, request changes.

## Phase 4: Execution and audit

- Add mock ERP or payment service.
- Add preview and execution modes.
- Persist audit trail for every decision and external call.

## Phase 5: Interview package

- Add demo data and screenshots.
- Add business workflow notes.
- Add trade-offs: autonomy versus control.
