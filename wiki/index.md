# 知識庫索引

這是 LLM 查詢與維護 wiki 時的第一個入口。新增或更新頁面後，請同步更新這裡的一句話摘要與分類。

## Start Here

- [[前端知識庫總覽]]：說明這個知識庫的目的、使用方式與目前狀態。
- [[產品地圖]]：整理產品、功能與前端工作之間的關聯。
- [[前端架構地圖]]：整理前端專案、架構、模組、工具與技術概念。
- [[工作流程地圖]]：整理前端開發、測試、審查、發版與協作流程。
- [[術語表]]：集中管理產品與前端常用名詞。

## Products

- 待補：匯入第一批產品資料後建立產品頁。

## Features

- 待補：匯入第一批功能資料後建立功能頁。

## Frontend Architecture

- [[前端架構地圖]]：前端架構與技術概念的總覽頁。
- [[前端套件與第三方服務]]：整理前端 packages、SDK 與第三方服務的用途分類與待確認問題。
- [[本機 Reverse Proxy 測試設定]]：整理用 nginx 在本機測試跨 `web-app` 與 `web-front` 頁面互轉、domain 模擬與 social login 的設定線索。

## Workflows

- [[工作流程地圖]]：前端工作流程的總覽頁。
- [[環境與 API 文件]]：整理 Development、Staging、Production、Production Beta 的用途、URL 與 API 文件入口。
- [[Git 提交與分支流程]]：整理 commit message type、ticket number、branch、MR review、release MR 與 hotfix 規則。
- [[前端專案版本維護流程]]：整理 `web-app`、`web-front`、`web-kit` 的版本號、API_KEY、branch、CI/CD 與 deploy script 流程。
- [[Staging 測試技巧]]：整理 Staging 電話驗證、信用卡綁卡與 WebATM 測試資料。

## Sources

- [[raw/README|Raw Sources]]：原始資料放置說明。
- [[raw/前端專案指引|前端專案指引]]：PRO360 前端 repository、共用模組與版本規則的初始 raw notes；尚未正式 ingest。
- [[raw/專案連結|專案連結]]：前端 repository 的 code URL 清單，並連回前端專案指引 raw notes。
- [[raw/pro360系統術語|PRO360 系統術語]]：由 Notion link 來源整理的 PRO360 產品、報價、新客源與前端相關術語 raw notes；尚未正式 ingest。
- [[raw/Environment|Environment]]：由 Notion link 來源複製的環境與 API 文件入口 raw notes；已整理為 [[環境與 API 文件]]。
- [[raw/套件使用與功能描述|套件使用與功能描述]]：前端 packages 與第三方服務功能描述 raw notes；已整理為 [[前端套件與第三方服務]]。
- [[raw/版控/Git提交注意事項|Git提交注意事項]]：commit message、branch control、review process 與 hotfix raw notes；已整理為 [[Git 提交與分支流程]]。
- [[raw/版控/前端專案版本維護流程|前端專案版本維護流程]]：Web App、Web Front、Web Kit 版本維護、API_KEY、branch 與 deploy script raw notes；已整理為 [[前端專案版本維護流程]]。
- [[raw/版控/WebApp-TW|WebApp-TW]]：WebApp-TW release version log，已依 deploy version log template 整理為可查詢 raw source；尚未拆成產品或 feature wiki 頁。
- [[raw/版控/WebApp-HK|WebApp-HK]]：WebApp-HK release version log，已依 deploy version log template 整理為可查詢 raw source；尚未拆成產品或 feature wiki 頁。
- [[raw/版控/WebApp-SG|WebApp-SG]]：WebApp-SG release version log，已依 deploy version log template 整理為可查詢 raw source；關聯至 [[前端專案版本維護流程]]。
- [[raw/版控/WebFront-TW|WebFront-TW]]：WebFront-TW release version log，已依 deploy version log template 整理為可查詢 raw source；關聯至 [[前端專案版本維護流程]]。
- [[raw/版控/WebKit-TW|WebKit-TW]]：WebKit-TW release version log，已依 web-kit deploy version log template 整理為可查詢 raw source；關聯至 [[前端專案版本維護流程]]。
- [[raw/staging測試技巧|staging測試技巧]]：Staging 測試資料與本機 nginx Reverse Proxy 測試設定；已整理為 [[Staging 測試技巧]] 與 [[本機 Reverse Proxy 測試設定]]。
- [[LLM-wiki|LLM-wiki]]：此 vault 採用的知識庫維護方法論。

## Pending Ingest

- [[raw/前端專案指引|前端專案指引]]：待確認 repository 命名、shared module 邊界、API Key 版本機制與適用範圍後，再拆成產品、架構與工作流程頁。
- [[raw/專案連結|專案連結]]：可作為 repository 來源索引；待搭配專案 README 或 onboarding 文件補齊用途與工作流程。
- [[raw/pro360系統術語|PRO360 系統術語]]：待拆入 [[術語表]]，並依內容連到產品、feature、architecture 或 workflow 頁。
- [[raw/版控/WebApp-TW|WebApp-TW]]：待依版本 notes 拆出產品、feature、architecture 與 workflow 連結。
- [[raw/版控/WebApp-HK|WebApp-HK]]：待依版本 notes 拆出產品、feature、architecture 與 workflow 連結。
- [[raw/版控/WebApp-SG|WebApp-SG]]：待依版本 notes 拆出產品、feature、architecture 與 workflow 連結。
- [[raw/版控/WebFront-TW|WebFront-TW]]：待依版本 notes 拆出產品、feature、architecture 與 workflow 連結。
- [[raw/版控/WebKit-TW|WebKit-TW]]：待依版本說明拆出產品、feature、architecture 與 workflow 連結。

## Maintenance Notes

- 優先建立 `產品 -> 功能 -> 前端實作 -> 工作流程` 的連結。
- 不確定的資訊使用 `待補` 標記，不要猜測。
- 每次匯入或整理後更新 [[log]]。
