# 本機 Reverse Proxy 測試設定

## Summary
- 用途：在本機測試跨 `web-app` 與 `web-front` / `web-fornt` 的頁面互轉流程，讓不同 dev server 共用單一 domain name 或 port。
- 使用範圍：本機開發測試；實際 repository 與路由規則待補。
- 目前狀態：來源提供 nginx 安裝、設定檔位置與啟停指令；完整 nginx config 內容未收錄在本 vault。

## Where It Appears
- 關聯產品：待補
- 關聯功能：跨前端專案頁面互轉、第三方 social login 本機測試；實際 feature 待補。
- 專案位置：`web-app`、`web-front` / `web-fornt`；來源拼字需確認。

## How It Works
- 核心概念：用 nginx 建立 Reverse Proxy，讓多個本機 dev server 透過同一個 domain name，例如 `http://localhost:3010`，進行測試。
- 資料流：瀏覽器請求先進 nginx，再依設定轉送到不同 frontend dev server；具體 path 與 port 規則待補。
- 重要依賴：nginx、`/opt/homebrew/etc/nginx/nginx.conf`、可能需要修改 `private/etc/hosts`，若要測試 Google、Facebook、Apple social login 並使用 HTTPS，還需要自行製作憑證。

## Change Notes
- 常見修改點：調整 nginx config 中的 port、domain name、proxy path 與目標 dev server。
- 風險：hosts 或 nginx config 設定錯誤會導致頁面轉址失敗；HTTPS 憑證設定不完整會阻擋第三方登入測試。
- 驗證方式：啟動 nginx 後，用單一 domain name 開啟跨 `web-app` 與 `web-front` 的流程，確認頁面互轉與 social login callback 是否正常；具體測試清單待補。

## Local Commands

```bash
brew install nginx
sudo nginx
sudo nginx -s stop
```

## Open Questions
- `web-fornt` 是否為 `web-front` 的拼字錯誤？
- nginx config 的完整內容與維護位置是什麼？
- 各 frontend dev server 的預設 port 是什麼？
- HTTPS 憑證的產生與信任流程是否已有內部標準？
- 修改 `private/etc/hosts` 時建議使用哪些 domain name？

## Sources
- [[raw/staging測試技巧]]
