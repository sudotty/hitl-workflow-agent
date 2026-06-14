# Data Model

## Core tables

### workflow_requests

| Field | Purpose |
|---|---|
| id | Request id |
| title | Short display title |
| source_text | Original request text |
| source_type | email, document, form, sample |
| status | new, extracted, checked, in_review, completed |
| created_at | Created time |

### extracted_fields

| Field | Purpose |
|---|---|
| id | Field id |
| request_id | Parent request |
| field_name | Field key |
| field_value | Extracted value |
| confidence | Optional confidence |
| note | Human-readable note |

### rule_checks

| Field | Purpose |
|---|---|
| id | Check id |
| request_id | Parent request |
| rule_name | Rule name |
| result | pass, warn, fail |
| message | Short explanation |

### review_records

| Field | Purpose |
|---|---|
| id | Review id |
| request_id | Parent request |
| reviewer | Reviewer name or id |
| decision | accepted, rejected, needs_changes |
| note | Reviewer note |
| created_at | Review time |

### workflow_events

| Field | Purpose |
|---|---|
| id | Event id |
| request_id | Parent request |
| event_type | created, extracted, checked, reviewed, completed |
| summary | Short event summary |
| created_at | Event time |

## MVP rule

Every workflow step should leave a readable record. The product is strong only when a human can inspect the path.
