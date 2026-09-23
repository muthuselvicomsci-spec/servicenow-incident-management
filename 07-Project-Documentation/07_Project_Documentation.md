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
## Evidence

### Final Configuration Evidence

The following screenshots document the final ServiceNow configuration:

- High Impact Control UI Policy
- Assignment Group mandatory action
- Urgency read-only action
- onChange Client Script for automatic Urgency
- onSubmit Client Script for Assigned To validation
- onCellEdit Client Script for State restriction

### Final Testing Evidence

The following screenshots document the completed testing:

- TC01 – High Impact with Assigned To empty: save blocked
- TC02 – High Impact with Assigned To selected: incident saved
- TC03 – Impact High: Urgency automatically set to High
- TC04 – Impact High: Urgency becomes read-only
- TC05 – Impact changed from High to Medium: UI Policy behavior reverses
- TC06 – State list editing: change blocked
- TC07 – State changed from Incident form: change saved

All final configuration and testing evidence has been uploaded to the corresponding project phase folders.
