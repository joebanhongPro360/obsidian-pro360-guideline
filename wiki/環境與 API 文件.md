# 環境與 API 文件

## Summary
- 觸發情境：本機開發、上機測試、正式環境確認、Production Beta 新功能確認、查詢 API 說明文件。
- 參與角色：前端工程師、QA、產品或其他需確認功能的人員；實際角色分工待補。
- 產出物：可對應環境用途與 API 文件入口的工作參考。

## Steps
1. Development 用於本機端開發，並使用 Staging 的資料環境。
2. Staging 用於發布前功能測試，部署在 staging 機器；資料皆為測試資料，可任意操作。
3. Production 用於正式發布環境，網址為 https://www.pro360.com.tw。
4. Production Beta 用於正式環境的新功能上線前確認，可利用正式環境資料確認結果。
5. 查詢 API 時，優先確認新版 API 說明文件；舊版 Google 文件仍是來源之一，但適用範圍待補。

## Environment Map

| 環境 | 用途 | 資料 | URL |
| --- | --- | --- | --- |
| Development | 本機端開發用執行環境 | 使用 Staging 的資料環境 | 待補 |
| Staging | 上機測試環境，發布前功能測試 | 測試資料，可任意操作 | https://staging.pro360.com.tw |
| Production | 正式發布環境 | 正式資料；操作限制待補 | https://www.pro360.com.tw |
| Production Beta | 正式環境的功能測試，用於新功能上線前確認結果 | 正式環境資料 | https://beta.pro360.com.tw |

## API Documents
- API 說明文件（新版）：https://api-staging.pro360.com.tw/api_doc/api/index
- API 說明文件（舊版）：Google 文件，適用範圍與維護狀態待補。

## Related Knowledge
- 關聯產品：待補
- 關聯功能：待補
- 關聯架構：[[前端架構地圖]]
- 關聯流程：[[工作流程地圖]]、[[Staging 測試技巧]]、[[本機 Reverse Proxy 測試設定]]

## Failure Modes
- 常見問題：Production Beta 使用正式環境資料，操作限制與驗證邊界待補。
- 預防方式：正式資料相關操作前需確認允許範圍；具體流程待補。
- 常見問題：新版與舊版 API 文件並存，正確查詢順序與可信來源待補。
- 預防方式：補齊 API 文件維護規則與 deprecated 判斷方式。
- 常見問題：Staging 測試資料、Production Beta 正式資料與 Production 正式資料的操作邊界不同。
- 預防方式：使用 [[Staging 測試技巧]] 的測試資料前先確認目前環境；Production Beta 與 Production 操作限制仍待補。

## Sources
- [[raw/Environment]]
- [[raw/staging測試技巧]]
- Notion source: https://www.notion.so/pro360-co/Environment-d7d39ad90a7f46fc88080f408b96389b
