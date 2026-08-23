# CORE-01~CORE-06 Implementation Detail Batch 002

## Scope

CORE 模組詳細施工資料展開層。

## 1. Control ID Mapping

Mapping chain:

Page UID → Section → Component → Control ID → Action → API → DB → Permission → Runtime → QA

CORE modules:
- CORE-01 Project Creation Wizard
- CORE-02 Topic Production Contract
- CORE-03 Blueprint Center
- CORE-04 Story / DNA Management
- CORE-05 Candidate Review Flow
- CORE-06 Script Workspace

## 2. API Schema Layer

Required fields:
- Endpoint ID
- Method
- Request Schema
- Response Schema
- Error Schema
- Permission Gate
- Runtime Event Binding

## 3. Database Entity Layer

Required fields:
- Entity Name
- Column
- Type
- Relation
- Migration
- Audit Requirement

## 4. Permission Resource Matrix

Required fields:
- Role
- Resource
- Action
- Scope
- Approval
- Restriction

## 5. Runtime State Machine

Required fields:
- Event ID
- Trigger
- Current State
- Next State
- Validation
- Recovery Flow

## 6. QA Evidence

Seven layer verification:
1. Data Model
2. Backend API
3. Runtime
4. Frontend
5. State/Error
6. i18n
7. Real Test Evidence

## Constraint

No new business logic is introduced. Detailed values must bind to the Single Authority Construction Master before final population.
