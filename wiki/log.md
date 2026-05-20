# 維護紀錄

此檔案是追加式紀錄，用來讓 LLM 與使用者快速理解知識庫如何演進。

## [2026-05-19] setup | Frontend AI knowledge base
- Source: [[LLM-wiki|LLM-wiki]]
- Updated: [[index]], [[前端知識庫總覽]], [[產品地圖]], [[前端架構地圖]], [[工作流程地圖]], [[術語表]]
- Notes: 初始化 LLM-wiki 風格的 Obsidian 前端知識庫骨架，目標是逐步熟悉專案、前端架構與流程。

## [2026-05-19] maintenance | Frontend raw source registration
- Source: [[raw/前端專案指引]], [[raw/專案連結]]
- Updated: [[index]], [[前端架構地圖]], [[工作流程地圖]]
- Notes: 登錄前端專案指引與 repository 連結作為待匯入 raw sources；補上候選來源與 open questions，但暫不建立正式產品 / 架構實體頁，避免把未確認資訊升格為 wiki 結論。

## [2026-05-19] maintenance | PRO360 system terms raw cleanup
- Source: [[raw/pro360系統術語]]
- Updated: [[raw/pro360系統術語]], [[index]]
- Notes: 依 Notion link 來源將 PRO360 系統術語整理成完整 Markdown raw，並加入 updated 紀錄：2026-05-19 14:31:46 CST。來源：https://www.notion.so/pro360-co/PRO360-bf5db664acfc471d8a08459eecee9179

## [2026-05-19] ingest | Environment
- Source: [[raw/Environment]]
- Updated: [[環境與 API 文件]], [[工作流程地圖]], [[前端架構地圖]], [[index]]
- Notes: 整理 Notion Environment 來源中的 Development、Staging、Production、Production Beta 與 API 文件入口；未補齊的環境切換、操作限制與文件維護規則標記為待補。來源：https://www.notion.so/pro360-co/Environment-d7d39ad90a7f46fc88080f408b96389b

## [2026-05-19] ingest | 套件使用與功能描述
- Source: [[raw/套件使用與功能描述]]
- Updated: [[前端套件與第三方服務]], [[前端架構地圖]], [[index]]
- Notes: 將 packages、SDK 與第三方服務清單整理為架構頁；raw 已依 [[raw/pro360系統術語]] 模板補上 metadata、Updated、Notes 與 Source，updated time：2026-05-19 15:13:59 CST。來源未指出 repository、版本或實際使用位置，相關資訊標記為待補。

## [2026-05-19] maintenance | Raw template cleanup
- Source: [[raw/Environment]], [[raw/pro360系統術語]], [[raw/前端專案指引]], [[raw/套件使用與功能描述]], [[raw/專案連結]]
- Updated: [[raw/Environment]], [[raw/pro360系統術語]], [[raw/前端專案指引]], [[raw/套件使用與功能描述]], [[raw/專案連結]], [[template/raw-source-table-example]], [[log]]
- Notes: 依使用者調整後的 raw template 規則，保留 frontmatter、Notes 與主要內容區塊，移除重複的頁面標題、Updated 與 Source 區塊；補齊套件來源連結，並同步精簡 template example。

## [2026-05-20] ingest | Git提交注意事項
- Source: [[raw/Git提交注意事項]]
- Updated: [[Git 提交與分支流程]], [[工作流程地圖]], [[index]]
- Template: normalized raw source note
- Notes: 已先將 raw 補上 frontmatter、source、updated、Notes 與內容標題，保留原始 Git commit、branch control、MR review、release MR、Code Summary 與 hotfix 規則，再整理為 workflow 頁。
