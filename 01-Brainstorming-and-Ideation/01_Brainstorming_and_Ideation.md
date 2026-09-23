# Phase 1 – Brainstorming & Ideation
## Project Title
Implement Client Script & UI Policy (Incident)

## Problem Statement
Incident records require consistent and accurate data entry for effective triage, routing, reporting, SLA compliance, and resolution. Manual checking can result in incomplete or inconsistent records.

## Proposed Solution
Use ServiceNow UI Policies and Client Scripts to enforce conditional field behavior and validation on Incident records.

## Objectives
- Make Assignment Group mandatory for High Impact incidents.
- Make Urgency read-only for High Impact incidents.
- Automatically set Urgency to High when Impact becomes High.
- Prevent submission when Assigned To is missing for a High Impact incident.
- Prevent State changes through direct list editing.

## Expected Benefits
Improved data quality, fewer incomplete submissions, and better Incident management workflow.
