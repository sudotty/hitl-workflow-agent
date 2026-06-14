# Architecture

## Goal

Build a small reviewable workflow console. The system should turn an incoming business request into extracted fields, rule checks, a summary, a human review step, and a final record.

## System boundary

The first version should use sample data. It should not connect real business systems. The product value is a clear workflow path, not deep integration.

## Components

| Component | Responsibility |
|---|---|
| Web UI | Request intake, fields, rule checks, summary, review screen, final record |
| Workflow API | Create requests, run extraction, run checks, update review status |
| Extraction service | Convert source text into structured fields |
| Rule engine | Run simple business rules and create notes |
| Summary service | Produce a short explanation for the reviewer |
| Review module | Record reviewer action and notes |
| Record store | Keeps request, fields, checks, summary, and timeline |

## MVP flow

```text
Load request
  -> extract fields
  -> run rules
  -> prepare summary
  -> send to review
  -> record result
  -> show timeline
```

## Recommended first stack

- Frontend: React / Next.js / Tailwind
- Backend: FastAPI or Spring Boot
- Database: SQLite or PostgreSQL
- Rule engine: simple config file first
- Sample data: JSON files in the repository

## Design principle

The system should prepare the work, not hide the decision. A reviewer should understand what happened and why.
