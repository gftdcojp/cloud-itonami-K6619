# Governance

`cloud-itonami-6619` is an OSS open-business blueprint for community card
transaction processing and settlement. Governance covers both the capability
layer and the operator model.

## Maintainers

Maintainers may merge changes that preserve these invariants:

- transactions with a failed Luhn check or declined authorization can never
  settle.
- the Card Settlement Governor remains independent of the advisor.
- hard policy violations (override-decline, force-settle, chargeback bypass)
  cannot be overridden by human approval.
- raw PANs are never persisted — tokenization is mandatory.
- every authorize, clear, settle and disclose path is auditable.

## Decision Records

Architecture decisions live in `docs/adr/`. Changes to the trust model,
storage contract, public business model, operator certification or license
should add or update an ADR.

## Operator Governance

Anyone may fork and operate independently. itonami.cloud certification is a
separate trust mark and should require security, audit, tokenization and
data-flow review.

Certified operators can lose certification for:

- bypassing authorization or settlement policy checks
- persisting raw PANs or mishandling cardholder data
- misrepresenting certification status
- failing to respond to security incidents
- hiding material changes to customer-facing operation
