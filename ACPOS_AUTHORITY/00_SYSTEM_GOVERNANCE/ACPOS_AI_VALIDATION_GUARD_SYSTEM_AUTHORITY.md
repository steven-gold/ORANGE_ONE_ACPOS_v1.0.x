# ACPOS AI Validation Guard System Authority

## Purpose
建立 ACPOS 內部 AI 防護與驗證機制，避免 AI 在施工、設計、生成、修改時自行猜測、自行新增未定義邏輯、自行改變已封板內容。

## Core Principle
AI 不負責創造規則。
AI 只能依照 Authority Registry 執行、驗證與提出變更申請。

## Authority Flow

Authority Source
↓
Registry Parse
↓
Validation Engine
↓
Decision Gate
↓
Execution
↓
Audit Log

## 1. Source Validation
任何 AI 輸出前必須確認：

- 是否存在對應 Authority 文件
- 是否存在 Page / Component / Control 編碼
- 是否存在 Action 定義
- 是否存在 Permission
- 是否存在 Runtime Event

缺少來源：禁止生成。

## 2. Anti Hallucination Guard
禁止：

- 自行新增頁面
- 自行新增功能
- 自行改變 UI Shell
- 自行修改 Logo / Brand
- 自行改變流程順序
- 自行補不存在的欄位

## 3. Change Request Mechanism
當發現需求需要變更：

Current Authority
↓
Change Proposal
↓
Impact Analysis
↓
Human Approval
↓
Version Update
↓
Deploy

AI 不直接修改 Authority。

## 4. Visual Generation Guard
生成 UI 圖片時：

必須輸入：

- Global Shell Authority
- Page Registry
- Component Registry
- Control Registry
- Action Registry

圖片元素必須可回溯至編碼。

## 5. Runtime Execution Guard
Runtime 執行必須綁定：

- Task ID
- Project ID
- Topic ID
- Version
- Permission
- Audit Event

## 6. Learning / Experience System Rule
Experience System 不允許 AI 自行改規則。

Experience 用於：

- 記錄成功案例
- 提供建議
- 提升評估準確度
- 輔助人工決策

規則變更必須經 Change Request 流程。

## 7. Deployment Guard
任何系統更新：

設計
↓
測試環境
↓
QA
↓
人工核准
↓
正式部署

不得直接由 AI 對話修改正式系統。

## Final Rule
ACPOS AI 是生產與驗證引擎，不是未受限制的自主開發者。
所有變更必須可追蹤、可驗證、可回溯。