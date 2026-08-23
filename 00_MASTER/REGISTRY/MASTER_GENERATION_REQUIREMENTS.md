# ORANGE ONE ACPOS v1.0.x Master Generation Requirements

## Purpose
建立唯一施工母檔所需的實際生成內容規範，作為後續 Registry、Runtime、API、Database、Permission、QA 展開依據。

## Authority Order
1. Single Authority Construction Package
2. R9 Master Rules
3. Page UID Registry
4. UI / UX Mapping
5. Data Contract
6. Runtime Contract
7. QA Evidence

## Required Registry Output

### Page UID
- page_uid
- route
- navigation_l1_l6
- section
- component
- control_binding
- api_binding
- db_binding
- permission_binding
- qa_binding

### Control Mapping
- control_id
- page_uid
- component
- type
- label
- datasource
- state
- validation
- action
- permission

### API Catalog
- endpoint_id
- method
- path
- request_schema
- response_schema
- error_schema
- runtime_event
- permission_gate

### Database Catalog
- entity
- table
- column
- datatype
- relation
- migration
- audit

### Permission Matrix
- role
- resource
- action
- scope
- approval
- restriction

### Runtime State
- event_id
- trigger
- current_state
- next_state
- validation
- recovery

### QA Evidence
- qa_id
- layer
- target
- test_condition
- evidence
- acceptance_rule

## Construction Rules
- 不建立第二套規格。
- 不新增未經母檔定義的功能。
- 不以空模板取代實際資料。
- 所有資料必須可追溯 UI → API → DB → Permission → Runtime → QA。
- 完成一個模組閉環後再進入下一模組。

## Module Sequence
CORE → ASSET → VIDEO → EDIT → VOICE → Integration Validation
