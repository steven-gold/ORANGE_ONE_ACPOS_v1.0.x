# CORE Final Data Fill Batch 008

## Scope
CORE-01 ~ CORE-06 六大 Catalog 資料列展開。

## 1. Control Registry
欄位：
- control_id
- page_uid
- section_id
- component_id
- field_name
- data_source
- state
- validation
- action
- permission_binding

## 2. API Endpoint Catalog
欄位：
- endpoint_id
- route
- method
- request_schema
- response_schema
- error_schema
- runtime_binding
- permission_gate

## 3. DB Entity Catalog
欄位：
- entity_id
- table_name
- column
- datatype
- relation
- migration
- audit_field

## 4. Permission Role Expansion
欄位：
- role
- resource
- action
- scope
- approval
- restriction

## 5. Runtime State Table
欄位：
- event_id
- trigger
- from_state
- to_state
- validation
- recovery

## 6. QA Case Table
欄位：
- qa_id
- layer
- target
- condition
- evidence
- pass_rule

## Completion Gate
CORE 完成後需通過：
Page → Control → API → DB → Permission → Runtime → QA 閉環檢查。

通過後進入 ASSET-01 ~ ASSET-04。