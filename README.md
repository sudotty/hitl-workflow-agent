# Human-in-the-loop Workflow Agent

A reviewable workflow agent for structured business operations: extract facts, check rules, prepare a summary, ask for human review, and keep a clear record.

This project focuses on a realistic enterprise pattern: AI prepares the work, but humans keep the final decision visible and controlled.

## Why this project exists

Many business workflows are repetitive but still require judgment. Requests often arrive through documents, spreadsheets, emails, or internal systems. The useful agent is not the one that hides the decision. The useful agent is the one that prepares the case clearly.

The goal is not full autonomy. The goal is safe delegation.

A practical workflow agent should answer:

1. What request came in?
2. What facts were extracted?
3. Which rules were checked?
4. What does the system recommend?
5. What should the human reviewer decide?
6. What record remains after the decision?

## Product shape

The product should feel like a small work review console.

Core screens:

| Screen | What it shows |
|---|---|
| Request Intake | Original request and attached sample data |
| Extracted Fields | Structured fields with confidence or notes |
| Rule Checks | Matched rules, missing fields, and warnings |
| Summary View | Short explanation of what the system understood |
| Review Screen | Approve, reject, or request changes |
| Record View | Final state, reviewer action, and timeline |

## MVP target

Build a sample business workflow where the agent extracts facts, checks rules, prepares a review summary, pauses for human decision, and records the result.

```text
request -> fields -> rule checks -> summary -> review -> final record
```

The first demo should show that the workflow is concrete and easy to inspect.

## Prioritized roadmap

| Priority | Workstream | Outcome |
|---|---|---|
| P0 / MVP | Workflow definition | The business process is concrete and understandable |
| P0 / MVP | Structured extraction | The system works with facts, not loose text |
| P0 / MVP | Rule checks and summary | The reviewer can understand why attention is needed |
| P0 / MVP | Showcase path | One demo path from request intake to final record |
| P1 | Review UI | Humans can approve, reject, or request changes |
| P1 | Mock business-system action | The workflow can close the loop without real systems |
| P1 | Workflow evaluation cases | Business rules can be checked repeatedly |
| P2 | Interview notes and demo script | The project is easy to explain to operations and AI teams |

## Repository documents

- [Roadmap](docs/roadmap.md)
- [Demo Positioning](docs/demo-positioning.md)
- [Showcase Plan](docs/showcase-plan.md)
- [Design Gallery](docs/design-gallery.md)

## Demo narrative

1. Load a sample business request.
2. Show extracted fields.
3. Show rule checks.
4. Generate a clear summary.
5. Send the case to review.
6. Show the final record.

## What this project demonstrates

- Business workflow understanding.
- Structured extraction and decision preparation.
- Human-centered automation rather than blind autonomy.
- Clear review and record design.
- Strong fit for AI automation, internal tools, and operations roles.

## Status

Planning and scaffolding. Issues are used as the implementation roadmap. The next build target is the P0 MVP showcase path.
