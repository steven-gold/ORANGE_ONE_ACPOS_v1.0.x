# AI Core Foundation Authority

## 定位

ACPOS AI 基礎模板，不綁定單一部門。

核心模組：

- AI Conversation
- Multi-AI
- Context
- Memory
- Decision
- Version
- Notebook / Record
- Provider
- Runtime State
- Permission
- Audit
- Experience

## 原則

AI 不自行新增系統規則。

Experience System 必須透過判斷機制決定：
- 可優化內容
- 需人工確認內容
- 禁止變更核心規則

所有資料需可追蹤來源、版本、決策。

## Authority Binding

本文件為 AI Core Foundation 說明層，正式模組清單與 Authority 狀態以 `AI_CORE_AUTHORITY_REGISTRY.yaml` 為準。

不得以「建立中」狀態覆蓋已封板 Registry；後續 API、DB、Runtime、Permission、QA 的落地完整度屬施工與驗收狀態，不改變 AI Core 基礎架構 Authority 狀態。

## 狀態

AI Core Foundation Authority: AUTHORITY_FROZEN
Authority Registry Source: AI_CORE_AUTHORITY_REGISTRY.yaml
