# CORE-01~CORE-06 Workbench Detail Mapping Batch 001

## Scope
建立 CORE 工作台第一層實體映射資料。

## Mapping Chain
Page UID → Section → Component → Control → API → DB → Permission → Runtime → QA

## CORE-01 Project Creation Wizard
- Section: Wizard Flow
- Component: Project Input / Conversation Entry / Blueprint Preparation
- Control Mapping: Pending detailed control IDs from authority source
- API Binding: Pending schema expansion
- DB Binding: Project domain entities
- Permission: Project creation scope
- Runtime: Create project lifecycle
- QA: Frontend / Backend / Runtime validation

## CORE-02 Topic Production Contract
- Section: Production Contract
- Component: Contract Definition / Requirement Binding
- Control Mapping: Pending detailed control IDs from authority source
- API Binding: Topic contract APIs
- DB Binding: Topic contract entities
- Permission: Production management scope
- Runtime: Contract state transition
- QA: Contract validation

## CORE-03 Blueprint Center
- Section: Blueprint Management
- Component: Story / DNA / Lock / Version
- Control Mapping: Pending detailed control IDs from authority source
- API Binding: Blueprint APIs
- DB Binding: Blueprint entities
- Permission: Blueprint access control
- Runtime: Blueprint lifecycle
- QA: Blueprint consistency validation

## CORE-04 Story / DNA Management
- Section: DNA Management
- Component: Character / Object / Scene / Rule
- Control Mapping: Pending detailed control IDs from authority source
- API Binding: DNA data APIs
- DB Binding: DNA entities
- Permission: DNA modification control
- Runtime: DNA lock workflow
- QA: Consistency checks

## CORE-05 Candidate Review Flow
- Section: Candidate Review
- Component: Candidate / Comparison / Approval
- Control Mapping: Pending detailed control IDs from authority source
- API Binding: Candidate APIs
- DB Binding: Candidate entities
- Permission: Review authority
- Runtime: Review state machine
- QA: Approval evidence

## CORE-06 Script Workspace
- Section: Script Workspace
- Component: Conversation Workspace / Script View / Task Tree
- Control Mapping: Pending detailed control IDs from authority source
- API Binding: Script workspace APIs
- DB Binding: Script entities
- Permission: Workspace access
- Runtime: Script generation workflow
- QA: Script validation

## Note
Detailed IDs must be filled only after authority YAML verification to avoid creating a second specification source.
