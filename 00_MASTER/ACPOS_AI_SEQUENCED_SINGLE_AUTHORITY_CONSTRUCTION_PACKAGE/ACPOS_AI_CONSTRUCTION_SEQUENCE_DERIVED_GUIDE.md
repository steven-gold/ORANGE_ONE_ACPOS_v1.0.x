# ACPOS AI 施工順序（Derived Guide）

> **GENERATED_FROM_MASTER / NON_AUTHORITATIVE / DO NOT EDIT AS AUTHORITY**
> 唯一施工權威：`ACPOS_SINGLE_AUTHORITY_CONSTRUCTION_MASTER_AI_SEQUENCED_FINAL.yaml`。

## 全局固定順序

1. PHASE 0 — Master Integrity + AI Read Index 驗證（不施工）
2. PHASE 1 — Global Page/UX Shell：導航、Route、左右收合、中央工作區伸縮、Tree、Drawer、Action Dock、全局狀態/i18n
3. PHASE 2 — Cross-unit Contract Freeze：只凍結既有接口，不做 Runtime 串接
4. PHASE 3 — 92 Page Unit 逐一施工：Page Design → UX Gate → Local Logic Binding → Function Gate → Freeze
5. PHASE 4 — 每個 Group 內部串接
6. PHASE 5 — 所有 Unit 完成後才做跨部門 Runtime Binding
7. PHASE 6 — System E2E（先到 Internal Runtime Boundary）
8. PHASE 7 — PostgreSQL / External Provider / Third-party Real Write 待明確授權後啟用

## 92 Page Unit 施工順序

### 01. 儀表板 — `WS-DASHBOARD`

01. `workspace:WB-01` — 儀表板

Group Gate：本群組全部 Page `UNIT_FROZEN` 後才允許 Group Internal Integration。

### 02. 核心生產 — `WS-CORE`

02. `workspace:CORE-01` — 建立 Project：故事與核心資料
03. `workspace:CORE-02` — 建立 Topic：生產目標與 Production Contract
04. `workspace:CORE-03` — Mother / Child Lock 審查
05. `workspace:CORE-04` — Topic Blueprint
06. `workspace:CORE-05` — Work Package / DAG
07. `workspace:CORE-06` — Core Workspace / Script / Canon

Group Gate：本群組全部 Page `UNIT_FROZEN` 後才允許 Group Internal Integration。

### 03. 素材製作 — `WS-ASSET`

08. `workspace:ASSET-01` — 素材任務工作區
09. `workspace:ASSET-02` — 素材版本與評分
10. `workspace:ASSET-03` — 素材交接
11. `workspace:ASSET-04` — 素材修正與返工

Group Gate：本群組全部 Page `UNIT_FROZEN` 後才允許 Group Internal Integration。

### 04. 影片生成 — `WS-VIDEO`

12. `workspace:VIDEO-01` — 影像任務工作區
13. `workspace:VIDEO-02` — Shot / Layer / Timeline 檢視
14. `workspace:VIDEO-03` — 影像評分與交接
15. `workspace:VIDEO-04` — 影像修正與重試

Group Gate：本群組全部 Page `UNIT_FROZEN` 後才允許 Group Internal Integration。

### 05. 剪輯／配音 — `WS-EDITVOICE`

16. `workspace:EDIT-01` — 剪輯影音任務工作區
17. `workspace:VOICE-01` — 配音、旁白與字幕工作區
18. `workspace:EDIT-03` — 剪輯評分與 QA 交接
19. `workspace:EDIT-04` — 剪輯修正與重檢

Group Gate：本群組全部 Page `UNIT_FROZEN` 後才允許 Group Internal Integration。

### 06. QA 審查 — `WS-QA`

20. `workspace:QA-01` — QA 審查工作區
21. `workspace:QA-02` — Finding / Manual Review
22. `workspace:QA-03` — QA 修正與返工追蹤
23. `workspace:QA-04` — Release Package
24. `workspace:QA-05` — Publish Request

Group Gate：本群組全部 Page `UNIT_FROZEN` 後才允許 Group Internal Integration。

### 07. 成品倉庫 — `WS-REL`

25. `workspace:REL-01` — 成品倉庫
26. `workspace:REL-02` — 發布追溯與撤回
27. `workspace:REL-03` — Release 成效回用

Group Gate：本群組全部 Page `UNIT_FROZEN` 後才允許 Group Internal Integration。

### 08. 素材庫 — `WS-LIB`

28. `workspace:LIB-01` — 素材庫搜尋
29. `workspace:LIB-02` — 素材詳情與版本
30. `workspace:LIB-03` — 素材重用候選

Group Gate：本群組全部 Page `UNIT_FROZEN` 後才允許 Group Internal Integration。

### 09. 最新資訊 — `WS-INFO`

31. `workspace:INFO-01` — 最新資訊儀表板
32. `workspace:INFO-02` — Fact Pack / Evidence
33. `workspace:INFO-03` — Context Pack Candidate

Group Gate：本群組全部 Page `UNIT_FROZEN` 後才允許 Group Internal Integration。

### 10. 戰略中心（前台） — `WS-STR`

34. `workspace:STR-01` — 戰略情報儀表板
35. `workspace:STR-02` — 戰略來源與 Watchlist
36. `workspace:STR-03` — 平台/帳號策略檔案
37. `workspace:STR-04` — Fact Pack / Cohort / 市場地圖
38. `workspace:STR-05` — Trend / Opportunity 預警
39. `workspace:STR-06` — Strategy Lab / AI Meeting

Group Gate：本群組全部 Page `UNIT_FROZEN` 後才允許 Group Internal Integration。

### 11. 系統維護／變更 — `AD-SYS`

40. `admin:SYS-01` — 系統 AI 對話與 Context
41. `admin:SYS-02` — Change Request Center
42. `admin:SYS-03` — Architecture / Dependency / Diff
43. `admin:SYS-04` — Code Candidate / Review
44. `admin:SYS-05` — Sandbox / Test Center
45. `admin:SYS-06` — System Release / Rollback
46. `admin:SYS-07` — System Health / Queue / Worker / Incident

Group Gate：本群組全部 Page `UNIT_FROZEN` 後才允許 Group Internal Integration。

### 12. ACPOS API 中心 — `AD-API`

47. `admin:API-01` — ACPOS API 總覽
48. `admin:API-02` — API Catalog / Contract
49. `admin:API-03` — Command / Query Trace
50. `admin:API-04` — Event / Outbox / Consumer / DLQ
51. `admin:API-05` — API Execution Sandbox
52. `admin:API-06` — Replay / Incident
53. `admin:API-07` — API Dashboard Feed

Group Gate：本群組全部 Page `UNIT_FROZEN` 後才允許 Group Internal Integration。

### 13. 外部 AI API 中心 — `AD-AIAPI`

54. `admin:AIAPI-01` — 外部 AI API 總覽
55. `admin:AIAPI-02` — Provider Registry
56. `admin:AIAPI-03` — Secret Reference
57. `admin:AIAPI-04` — Capability Registry
58. `admin:AIAPI-05` — Route Policy
59. `admin:AIAPI-06` — Instruction Compile Audit
60. `admin:AIAPI-07` — Provider Job / Attempt
61. `admin:AIAPI-08` — Provider Sandbox
62. `admin:AIAPI-09` — Budget / Provider Incident

Group Gate：本群組全部 Page `UNIT_FROZEN` 後才允許 Group Internal Integration。

### 14. 帳戶與權限 — `AD-IAM`

63. `admin:IAM-01` — User List
64. `admin:IAM-02` — User Wizard
65. `admin:IAM-03` — User Detail / Privilege
66. `admin:IAM-04` — Organization / Department Scope / SoD
67. `admin:IAM-05` — Permission Tree
68. `admin:IAM-06` — Access Review / Break-glass

Group Gate：本群組全部 Page `UNIT_FROZEN` 後才允許 Group Internal Integration。

### 15. 企業自動開發 — `AD-DEV`

69. `admin:DEV-01` — 企業名單持續搜集
70. `admin:DEV-02` — 企業主資料庫
71. `admin:DEV-03` — 企業開發信內容工作區
72. `admin:DEV-04` — 開發活動／受眾批次管理
73. `admin:DEV-05` — 一對一 Email 發送控制

Group Gate：本群組全部 Page `UNIT_FROZEN` 後才允許 Group Internal Integration。

### 16. 社群發布 — `AD-SOC`

74. `admin:SOC-01` — 社群平台登錄
75. `admin:SOC-02` — 社群帳號綁定／市場目標
76. `admin:SOC-03` — 社群內容包／平台版本
77. `admin:SOC-04` — 社群發布目標／頻率控制
78. `admin:SOC-05` — 社群貼文／互動／人工處理紀錄

Group Gate：本群組全部 Page `UNIT_FROZEN` 後才允許 Group Internal Integration。

### 17. 知識庫 — `AD-KB`

79. `admin:KB-01` — Knowledge Source Registry
80. `admin:KB-02` — Ingestion / Research Queue
81. `admin:KB-03` — Knowledge Search / Citation / Context Builder

Group Gate：本群組全部 Page `UNIT_FROZEN` 後才允許 Group Internal Integration。

### 18. 戰略中心（後台） — `AD-STR`

82. `admin:STR-01` — Intelligence Dashboard
83. `admin:STR-02` — Strategy Source / Watchlist
84. `admin:STR-03` — Platform / Account Playbook
85. `admin:STR-04` — Fact / Cohort
86. `admin:STR-05` — Trend / Opportunity
87. `admin:STR-06` — Strategy Decision Lab

Group Gate：本群組全部 Page `UNIT_FROZEN` 後才允許 Group Internal Integration。

### 19. ERP／財務 — `AD-ERP`

88. `admin:ERP-01` — ERP Connector / Snapshot
89. `admin:ERP-02` — Finance / Capacity Guardrail

Group Gate：本群組全部 Page `UNIT_FROZEN` 後才允許 Group Internal Integration。

### 20. 評分與 QA 治理 — `AD-SG`

90. `admin:SG-01` — Instruction Package Governance
91. `admin:SG-02` — Quality Criteria / Gate Policy
92. `admin:SG-03` — Scorecard / Review Trace

Group Gate：本群組全部 Page `UNIT_FROZEN` 後才允許 Group Internal Integration。

## 每個 Page 固定施工迴圈

```text
LOAD CURRENT UNIT ONLY
↓
PAGE DESIGN
↓
PAGE DESIGN GATE
↓
LOCAL LOGIC BINDING
↓
UNIT FUNCTION GATE
↓
UNIT FREEZE
↓
NEXT UNIT
```

## 跨部門串接規則

只有在 **92/92 Page Unit 全部 Freeze + 各 Group Internal Integration PASS** 後才允許。
跨部門只能使用母檔已存在的 `handoff / workflow / API / permission / runtime` 契約；若缺失或衝突，回報 `INTEGRATION_CONFLICT`，不得自行修改已封板單位。

Source master SHA256: `3e67c257c739345e74d49055a2e8fb8a2ad857ec7354ca583c2ff25c5ff37614`
Sequenced master SHA256: `06d39da9678e6c3f289053e11e8ec0ab26a3a96c7caa74ac869d6efebb0befad`