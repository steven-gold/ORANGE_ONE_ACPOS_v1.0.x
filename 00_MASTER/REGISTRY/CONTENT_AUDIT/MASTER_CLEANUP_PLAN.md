# ACPOS Master Cleanup Plan

## Purpose
整理 Registry、Index、Guide、Template 文件，避免重複規格來源。

## Authority Rule
唯一權威來源：
- ACPOS_SINGLE_AUTHORITY_CONSTRUCTION_MASTER_AI_SEQUENCED_FINAL.yaml

其他文件僅作為：
- Index
- Mapping
- Validation
- Execution Guide

不得取代母檔。

## Keep
保留：
- Page UID Registry
- Control Mapping Registry
- API Catalog
- Database Schema Catalog
- Permission Matrix
- Runtime Event Matrix
- QA Evidence Matrix

## Merge Candidates
合併：
- AI_EXECUTION_ORDER
- AI_AGENT_READ_SEQUENCE
- AI_CONSTRUCTION_RULES

目標：
AI_EXECUTION_PROTOCOL.md

## Archive Candidates
歷史階段文件：
- 舊版 Template
- 重複 Index
- 過程性說明文件

## Next Execution Order
1. 驗證母檔內容
2. 確認 Registry 對應
3. 展開 Page UID
4. 展開 Control Mapping
5. 展開 API / DB / Permission / Runtime / QA
