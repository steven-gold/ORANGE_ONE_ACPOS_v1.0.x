# ACPOS Global UI Shell Authority V1.1

## 文件定位

本文件定義 ACPOS 全站共用視覺與版面基礎模板。

用途：
- 固定首頁與所有工作區共同版面比例
- 固定 Header、Navigation、Workspace 結構
- 作為 CORE / ASSET / VIDEO / EDIT / VOICE / Strategic Center / System Maintenance 的 UI 基礎
- 定義所有頁面只能替換 Main Workspace 內容，不得重新建立 Global Shell

本文件不定義部門功能，不定義頁面專屬業務邏輯。

## 1. 基礎視覺定位

品牌：ORANGE ONE

風格：
- 深色紫霧科技風
- AI 生產工作站
- 高效率企業操作介面
- 清晰資訊層級
- 非一般聊天介面

## 2. 畫布與固定尺寸

- Desktop First
- 基準比例：16:9
- Header：72px 固定
- Sidebar：240px 展開 / 72px 收合
- Sidebar Item：52px
- Main Workspace Outer Margin：20px
- Main Workspace Padding：32px
- Main Workspace Radius：24px

## 3. Global Layout

固定結構：

Header
↓
Sidebar + Main Workspace

任何頁面只能替換 Main Workspace 內部內容。

## 4. Header Authority

固定區域：
- Brand Slot：ORANGE ONE Logo / Brand
- Page Context Slot：由目前頁面的 Page Authority 決定顯示內容
- Runtime / System Status Slot
- User Control Slot

重要規則：
- Global Shell 不強制 Project / Topic / Task 同時出現。
- Page Context 必須依頁面 Authority 顯示。
- CORE 目前只允許 Project / Topic Context，不綁 Production Task。
- 後續生產部門可依其 Page Authority 顯示 Production Task。
- 禁止因 Global Header 舊規則把 Task Context 強制注入 CORE。

## 5. Side Navigation Authority

- Expanded Width：240px
- Collapsed Width：72px
- Vertical Navigation
- Icon Size：20px
- Text：16px
- Item Height：52px
- 支援展開 / 收合
- 收合後 Main Workspace 自動擴展

Navigation 項目內容必須由正式 Navigation Authority 提供；Global Shell 只負責承載、排列與互動規則，禁止自行建立平行 Navigation。

## 6. Main Workspace

- 所有頁面內容必須位於 GLOBAL_WORKSPACE_001
- Main Workspace 內部比例由各 Page Authority 定義
- 禁止超出 Global Shell
- 禁止頁面自行重建 Header / Sidebar

## 7. Global Interaction

- Hover：顯示低亮度紫色疊層
- Active：紫色漸層 + 輕度外發光
- Disabled：降低透明度並顯示原因
- Loading：顯示 Runtime 狀態，不得空白等待
- Error：必須顯示錯誤狀態與恢復入口

## 8. Authority / Source Trace

每個 Global UI 元素必須可追溯：
Page → Section → Component → Control → Action → State → Visual Mapping → Render Binding。

未知來源：Reject Render。

## 9. Conflict Resolution

權威順序：
1. Single Construction Authority
2. Global UI Shell Authority
3. Global Page / Component / Control / State Registries
4. Page-specific Authority
5. Render Binding

低優先級不得覆蓋高優先級。

## 10. Department / Page Inheritance

CORE / ASSET / VIDEO / EDIT / VOICE / Strategic Center / System Maintenance：
- 繼承 Global Shell
- 只定義 Main Workspace 專屬內容
- 不得修改 Logo 比例、Header、Sidebar、全域色系

## Status

Global Shell Structure: FINAL
Global Visual Direction: FINAL
Render Authority: controlled by registries and validation files
