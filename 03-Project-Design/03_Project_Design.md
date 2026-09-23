# Phase 3 – Project Design
## System Flow
User opens Incident → changes Impact → UI Policy evaluates condition → UI Policy Actions control fields → onChange Client Script updates Urgency → user submits → onSubmit validates Assigned To → record saves only when validation succeeds.

## List Edit Flow
Incident List → State edited → onCellEdit Client Script → direct change blocked.

## Components
### UI Policy
Name: High Impact Control
Table: Incident
Condition: Impact is 1 – High
Reverse if false: True

### UI Policy Actions
- Assignment group: Mandatory
- Urgency: Read-only

### Client Scripts
- Auto set urgency for high impact — onChange — Impact
- Prevent save if Assigned To missing — onSubmit
- Prevent state change via list edit — onCellEdit — State
