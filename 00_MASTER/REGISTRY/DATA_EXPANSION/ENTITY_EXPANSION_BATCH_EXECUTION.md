# Entity Expansion Batch Execution

## Scope

本批次進入資料實體展開階段。

執行順序：

1. CORE-01~CORE-06 Page UID
2. ASSET-01~ASSET-04 Page UID
3. VIDEO-01~VIDEO-04 Page UID
4. EDIT / VOICE Page UID
5. Control ID Mapping
6. API Request/Response Schema
7. Database Entity Relation
8. Permission Resource Matrix
9. Runtime State Transition
10. QA Evidence Cases

## Rules

- 以 Single Authority Construction Master 為唯一規格來源。
- Registry 僅作為施工映射層，不取代母檔。
- 未確認來源內容前，不自行補入不存在的功能定義。
- 每批資料需可追溯 Page UID、Control、API、DB、Permission、Runtime、QA 關聯。

## Batch Status

- Phase: Entity Expansion
- Status: Started
