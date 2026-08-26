# ACPOS Global UI Shell Visual Authority - Purple Freeze FINAL

## Status
Authority Freeze FINAL

用途：固定 ACPOS 全站共用首頁與工作區外框，不允許任何頁面重新設計 Header、Sidebar、Workspace 基礎結構。

## Visual Identity
- Brand: ORANGE ONE
- Product: ACPOS AI Production OS
- Style: 深色紫霧科技風 / AI Enterprise Production Workspace
- Positioning: 專業 AI 生產工作站，不是一般聊天介面

## Global Canvas
- Desktop First
- Ratio: 16:9
- Header + Sidebar + Main Workspace 固定結構

## Header
- Height: 72px
- Padding: 24px
- Left: ORANGE ONE Logo / Brand
- Center: PAGE_CONTEXT_SLOT，由頁面權威決定 Project / Topic / Production Task 等上下文，不可由 Global Shell 強制內容
- Right: Search / System Status / Notification / User
- Logo 必須保留既定比例；禁止重新繪製或改比例

## Sidebar
- Expanded Width: 240px
- Collapsed Width: 72px
- Item Height: 52px
- Icon: 20px
- Text: 16px
- Vertical Navigation
- Active: 紫色漸層 + Soft Glow
- Hover: 低亮紫色 Overlay

## Main Workspace
- Header 下方、Sidebar 右側
- Outer Margin: 20px
- Border Radius: 24px
- Padding: 32px
- Background: Deep Purple Navy Glass Panel
- 所有頁面只能替換此容器內部內容

## Color Token
- Background Base: #050816
- Deep Navy: #070B1D
- Panel Base: #0C1026
- Panel Overlay: #111936
- Primary Purple: #8B5CFF
- Secondary Purple: #6E35FF
- Highlight Violet: #B38CFF
- Accent Blue Purple: #4D6BFF
- Text Primary: #F3F5FF
- Text Secondary: #AEB7D9
- Text Muted: #7F88A8
- Border Subtle: rgba(142,112,255,0.28)
- Hover Surface: rgba(139,92,255,0.18)
- Active Surface: rgba(139,92,255,0.28)

## Interaction
Active:
- Purple gradient highlight
- Soft glow

Hover:
- Low intensity purple overlay

Disabled:
- Reduced opacity
- 必須顯示不可操作原因

Loading:
- Must show runtime state

Error:
- 顯示錯誤狀態與恢復入口

## Page Inheritance Rule
所有頁面必須繼承本 Shell。
CORE / ASSET / VIDEO / EDIT / VOICE / Strategic Center / System Maintenance 僅可修改 Main Workspace 內部內容。

## Forbidden
- Changing Header layout
- Changing Sidebar layout
- Changing Logo ratio
- Changing global color theme
- Creating another visual system
- Injecting page-specific context not authorized by that page
