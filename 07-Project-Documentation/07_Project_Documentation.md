# Phase 7 – Project Documentation
## Overview
This project demonstrates how ServiceNow UI Policies and Client Scripts can enforce business rules on Incident records.

## Configuration Summary
- High Impact Control UI Policy
- Assignment Group mandatory action
- Urgency read-only action
- onChange Urgency automation
- onSubmit Assigned To validation
- onCellEdit State restriction

## Working Process
1. User opens an Incident.
2. User sets Impact.
3. UI Policy evaluates the condition.
4. Relevant fields change.
5. onChange updates Urgency when Impact is High.
6. onSubmit validates Assigned To.
7. Valid records are saved.
8. Direct State list editing is blocked.

## Conclusion
The implementation demonstrates practical client-side controls for data integrity, user guidance, and consistent Incident management.

## Evidence
Add final configuration screenshots and final testing screenshots.
