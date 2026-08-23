# ACPOS Registry Consolidation Audit

## Audit Purpose

Review existing GitHub construction documents and remove duplicated governance layers before continuing data expansion.

## Consolidation Rules

1. Single Authority YAML remains the only source of truth.
2. Registry files are implementation indexes and mappings only.
3. Templates that duplicate the same contract definition should merge into one authority document.
4. Empty placeholders must not be treated as completed implementation.

## Keep

- Single Authority Construction Master
- Page UID Registry
- Control Mapping Registry
- API Contract Registry
- Database Schema Registry
- Permission Matrix
- Runtime Event Matrix
- QA Evidence Matrix

## Merge Candidates

- Multiple AI execution/read sequence documents
- Repeated index documents describing the same contract
- Duplicate checklist documents

## Before Full Data Expansion

Verify YAML content, then generate actual Page UID, Control, API, DB, Permission, Runtime and QA records.
