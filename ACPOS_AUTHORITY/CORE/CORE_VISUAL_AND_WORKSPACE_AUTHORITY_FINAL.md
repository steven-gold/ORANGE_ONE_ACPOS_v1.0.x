# ACPOS CORE Visual and Workspace Authority V2

## 文件定位
本文件定義 CORE 在 Global UI Shell 下的最新單一工作頁。舊的 CORE-01/CORE-02 分頁式操作視為已取代，不得再由渲染層建立平行頁面。

基礎來源：
- ACPOS Global UI Shell Visual Authority Purple Freeze FINAL
- AI Conversation Core Authority
- CORE 最新作業邏輯

禁止：
- 修改 Header / Sidebar / Logo / 全站色系
- 把 Production Task 當成 CORE Conversation 綁定欄位
- 把所有 CORE 工作塞進單一無分類聊天紀錄
- 新增未定義 Dashboard 元件

## 1. CORE 定位
CORE 負責 Project / Topic 的核心內容建立與封板，故事、章節、世界設定、DNA、Blueprint、Script 等內容以 AI Conversation 為主要工作方式。

Project 與 Topic 為頁面綁定上下文；不同核心工作項目擁有各自 Conversation Thread。

## 2. 單一頁面架構
CORE 使用一個主要工作頁：CORE-01。

Main Workspace：
1. 上方固定 Page Context Bar：Project Selector + Topic Selector + 對應建立入口。
2. 左側 Work Item / Conversation Rail：顯示目前 Project / Topic 下的核心工作項目與各自對話紀錄入口。
3. 中央 AI Conversation Workspace：載入目前所選 Work Item 的獨立 Conversation Thread，為最大操作區。
4. 右側 Output / State Rail：顯示 DNA、Blueprint、Script、Version、Decision 等目前狀態與結果入口。

## 3. Work Item 與 Task 名稱邊界
左側「任務欄」屬於 CORE 內部 Work Item / Conversation Item Navigation，不是 Production Task。

Work Item 可對應：
- Story
- Chapter
- World / Setting
- DNA
- Blueprint
- Script
- 其他由 CORE Authority 正式建立的核心項目

每個 Work Item 必須綁定自己的 conversation_thread_id、version_id、status 與 lock state。

Production Task 僅在 CORE Project / Topic 完成封板後建立並交接 ASSET；不得出現在 CORE Page Context Selector。

## 4. AI Conversation
Conversation 必須綁定：
- Project
- Topic
- Work Item
- Conversation Thread
- Version / Context

Conversation 不綁定 Production Task。

使用者切換 Work Item 時，中央 Conversation Workspace 必須載入該項目的獨立歷史，不得混用其他 Work Item 的訊息。

## 5. 右側狀態區
右側為狀態與結果入口，不是另一套獨立工作流程。

顯示順序依核心依賴：
1. DNA
2. Blueprint
3. Script
4. Version
5. Decision

Story / Chapter / World 等工作項目的細節由左側 Work Item Navigation 與中央 Conversation 處理。

## 6. CORE 正確流程
Project 建立與基本設定
→ Project 內各核心 Work Item 透過 Conversation 建立並逐項定案
→ Project 完整後鎖定
→ Topic 建立 / Production Scope 定義
→ Topic 內產生後續部門所需 Script
→ Topic 完成鎖定
→ 建立 Production Task
→ 通知 ASSET

在單一工作項目的依賴中：
Story / Chapter / World Context
→ DNA
→ Blueprint
→ Script
→ Version
→ Decision / Lock

禁止 Blueprint Lock 後再回頭把 DNA 當下一個必經步驟。

## 7. 版面比例
Global Header / Sidebar 由 Global Shell 固定。
CORE Main Workspace 內：
- Page Context Bar：上方固定橫列
- Left Work Item Rail：約 22%
- Center AI Conversation：約 50%，主要區域
- Right Output State Rail：約 28%

若畫面寬度改變，中央 Conversation 優先保留最大可用區域。

## 8. 封板規則
任何 CORE 畫面元素必須能回溯：Page → Section → Component → Control → Action → State → Position → Source。

未知來源：Reject Render。

## Status
CORE Latest Architecture: ACTIVE AUTHORITY
Legacy split-page model: REPLACED
Production Task binding inside CORE Conversation: FORBIDDEN
Work Item / Conversation Navigation: REQUIRED
