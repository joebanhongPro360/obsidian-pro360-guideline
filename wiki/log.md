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
- Source: [[raw/版控/Git提交注意事項]]
- Updated: [[Git 提交與分支流程]], [[工作流程地圖]], [[index]]
- Template: normalized raw source note
- Notes: 已先將 raw 補上 frontmatter、source、updated、Notes 與內容標題，保留原始 Git commit、branch control、MR review、release MR、Code Summary 與 hotfix 規則，再整理為 workflow 頁。

## [2026-05-20] ingest | staging測試技巧
- Source: [[raw/staging測試技巧]]
- Updated: [[Staging 測試技巧]], [[本機 Reverse Proxy 測試設定]], [[環境與 API 文件]], [[工作流程地圖]], [[前端架構地圖]], [[index]]
- Template: normalized raw source note
- Notes: 已依使用者提供 metadata 補上 raw frontmatter、source、updated 與 Notes；將 Staging 電話驗證、信用卡與 WebATM 測試資料整理為 workflow 頁，並將 nginx Reverse Proxy、hosts、production domain 模擬與 social login 本機測試整理為 architecture 頁。來源：https://www.notion.so/pro360-co/1fa102cae60441068980a8e76a8391d6, https://www.notion.so/pro360-co/d240a4a327364e5292bd718533f76f60

## [2026-05-20] maintenance | Ingest metadata prompt
- Source: [[AGENTS]]
- Updated: [[AGENTS]], [[log]]
- Notes: 更新 ingest workflow 規則；當使用者提供 `updated: now` 時，應自動轉成目前本地時間格式 `YYYY-MM-DD HH:mm:ss CST`，其他明確 metadata 值仍照原文保留。

## [2026-05-20] ingest | 前端專案版本維護流程
- Source: [[raw/版控/前端專案版本維護流程]]
- Updated: [[前端專案版本維護流程]], [[工作流程地圖]], [[前端架構地圖]], [[index]]
- Template: normalized raw source note / workflow page
- Notes: 已依使用者提供 metadata 補上 raw frontmatter、source、updated 與 Notes；將 Web App、Web Front、Web Kit 的版本號、API_KEY、branch、CI/CD 與 deploy script 操作整理為 workflow 頁，並將 release branch 流程標記為來源建議、正式採用狀態待補。來源：https://www.notion.so/pro360-co/Note-889220a833e84088b72efd13629e9cd7

## [2026-05-20] maintenance | 版控 raw sources organization
- Source: [[raw/版控/Git提交注意事項]], [[raw/版控/前端專案版本維護流程]], [[raw/版控/WebApp-TW]]
- Updated: [[raw/README]], [[Git 提交與分支流程]], [[前端專案版本維護流程]], [[工作流程地圖]], [[前端架構地圖]], [[index]]
- Notes: 將 Git commit、branch、MR、hotfix、前端版本號與 deploy 相關 raw 文件整理至 `raw/版控/`，並同步更新 wiki 與 log 中指向舊 raw 路徑的 Obsidian links。

## [2026-05-20] maintenance | WebApp-TW
- Source: [[raw/版控/WebApp-TW]]
- Updated: [[raw/版控/WebApp-TW]], [[raw/README]], [[index]], [[log]]
- Template: deploy-version-log-app&front-example
- Notes: 已訪問 raw 內 23 個公開 Notion version source，將 v5.2.4 至 v6.0.1-2 整理為 version、ai_summary、release_date、status、messages、note 格式；公開頁未提供或空白欄位標記為 `待補`。

## [2026-05-22] maintenance | WebApp-TW raw rename
- Source: [[raw/版控/WebApp-TW]]
- Updated: [[raw/版控/WebApp-TW]], [[raw/README]], [[index]], [[log]]
- Notes: 將 raw 檔名由 `WebApp-TW 版控紀錄.md` 改為 `WebApp-TW.md`，並同步更新 wiki/index.md、wiki/log.md 與 raw/README.md 的 Obsidian links。

## [2026-05-22] maintenance | WebApp-HK raw normalization
- Source: [[raw/版控/WebApp-HK]]
- Updated: [[raw/版控/WebApp-HK]], [[index]], [[log]]
- Template: deploy-version-log-app&front-example
- Notes: 參考 [[raw/版控/WebApp-TW]] 的 raw source 結構，將 WebApp-HK v5.1.3 release 訊息整理為 frontmatter、Notes、版本標題、version、ai_summary、release_date、status、messages、note 欄位；原始筆記未提供的欄位標記為 `待補`。

## [2026-05-22] maintenance | Release log wiki relations
- Source: [[raw/版控/WebKit-TW]], [[raw/版控/WebFront-TW]], [[raw/版控/WebApp-SG]]
- Updated: [[前端專案版本維護流程]], [[工作流程地圖]], [[前端架構地圖]], [[index]]
- Template: wiki relation update
- Notes: 將 WebKit-TW、WebFront-TW、WebApp-SG release log raw sources 連到 [[前端專案版本維護流程]]，並同步加入 workflow / architecture map 與 index；release log 尚未拆成產品、feature 或架構 wiki 頁。

## [2026-05-22] maintenance | Version source link cleanup
- Source: [[raw/版控/WebApp-HK]], [[raw/版控/WebApp-SG]], [[raw/版控/WebApp-TW]], [[raw/版控/WebFront-TW]]
- Updated: [[raw/版控/WebApp-HK]], [[raw/版控/WebApp-SG]], [[raw/版控/WebApp-TW]], [[raw/版控/WebFront-TW]], [[log]]
- Template: deploy-version-log-app&front-example
- Notes: 檢查 `raw/版控/` 內 version heading 的 source links，移除 Notion URL 結尾的 `?pvs=74` 與 `?pvs=21` params；未修改非 version heading 的一般文件連結。
