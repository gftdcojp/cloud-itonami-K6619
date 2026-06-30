# Operator Guide

## First Deployment

1. Register merchants, card ranges, networks and responsible operators.
2. Import authorization and settlement history.
3. Run read-only PAN (Luhn) and ISO 8583 MTI validation against existing data.
4. Configure clearing-window schedules, settlement accounts and escalation paths.
5. Publish a dry-run settlement and audit export.

## Minimum Production Controls

- Luhn and network validation before any authorization
- ISO 8583 MTI validation before message dispatch
- partial-approval amount enforcement at settlement
- tokenization of PANs at the edge (no raw PAN in storage)
- audit export for every settlement and chargeback
- backup manual settlement process

## Certification

Certified operators must prove authorization integrity, settlement
reconciliation, evidence-backed reporting and human review for
settlement-affecting actions.
