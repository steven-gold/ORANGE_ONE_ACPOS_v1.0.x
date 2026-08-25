# ACPOS Global UI Shell Authority V1

## 文件定位

本文件定義 ACPOS 全站共用視覺與版面基礎模板。

用途：
- 固定首頁與所有工作區共同版面比例
- 固定 Header、Navigation、Workspace 結構
- 作為 CORE / ASSET / VIDEO / EDIT / VOICE / Strategic Center / System Maintenance 的 UI 基礎

本文件不定義部門功能，只定義全域視覺框架。

---

# 1. 基礎視覺定位

品牌：ORANGE ONE

風格：
- 專業科技感
- AI 生產工作站
- 高效率企業操作介面
- 深色沉浸式工作環境
- 清晰資訊層級

禁止：
- 普通聊天視窗風格
- 消費型 App 風格
- 過度裝飾影響操作

---

# 2. 畫布規格

主要工作環境：Desktop

比例：16:9

所有工作區必須在 Global Workspace 範圍內設計。

---

# 3. Global Layout

固定結構：

Header
↓
Navigation + Main Workspace

```text
+--------------------------------+
| Header / Top Bar               |
+----------+---------------------+
| Side Nav | Main Workspace      |
|          |                     |
+----------+---------------------+
```

---

# 4. Header 規範

高度：64px-72px

內容：
- ORANGE ONE Brand
- Project Context
- Topic Context
- Task Context
- Runtime Status
- Version
- Permission/User State

所有部門共用。

---

# 5. Side Navigation 規範

寬度：240px-280px

功能：
- 全站入口
- 部門切換
- 系統分類

支援：

展開模式：
- Icon
- 名稱
- 子項目

收合模式：
- Icon

收合後 Main Workspace 自動擴展。

---

# 6. Main Workspace 規範

Main Workspace 為所有功能實際操作區。

不得超出 Global Shell 定義。

工作區可依部門調整內部比例，但不可改變 Header / Navigation 基準。

---

# 7. Workspace 基礎比例

預設三區：

Left Panel
22%

Center Workspace
50%

Right Panel
28%

部門可依功能調整，但需遵守整體框架。

---

# 8. 元件風格規範

## Card

統一：
- 圓角
- 層級分明
- 資訊卡片化

## Button

狀態：
- Primary
- Secondary
- Warning
- Disabled

## Status

統一狀態：
- Waiting
- Running
- Review
- Completed
- Error
- Locked

---

# 9. 互動規範

Hover：
顯示操作名稱與說明。

Disabled：
必須顯示不可操作原因。

Loading：
不得空白等待，需顯示 Runtime 狀態。

---

# 10. 部門套用規則

CORE：
套用 Global Shell + CORE 專業區域。

ASSET：
套用 Global Shell + 素材生產區域。

VIDEO：
套用 Global Shell + 影片生產區域。

EDIT：
套用 Global Shell + 剪輯影音區域。

VOICE：
套用 Global Shell + 聲音製作區域。

---

# Authority Rule

Global UI Shell 為所有 ACPOS 頁面視覺基準。

任何新頁面建立前，必須先符合本模板，再建立部門專屬 UI。
