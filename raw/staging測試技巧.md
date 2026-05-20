---
title: staging測試技巧
source:
  - https://www.notion.so/pro360-co/1fa102cae60441068980a8e76a8391d6
  - https://www.notion.so/pro360-co/d240a4a327364e5292bd718533f76f60
updated: 2026-05-20 09:30:23 CST
---

## Notes

- 本檔為 `raw/` 原始資料整理檔，內容來自使用者提供的 Notion source。
- 來源內容包含 Staging 測試資料與本機 Reverse Proxy 測試設定。
- 原始內容語意已保留；未補猜測缺漏資訊。

## Staging環境中：

- 電話驗證：
  使用098765432X，即可以任意四位驗證碼通過
- 信用卡：
  - 綁卡時使用：4242 4242 4242 4242，有效期限與CVC任意
    其他測試卡號請參考Tappay or Stripe文件
  - 單次購點可選用WebATM會自動完成流程

## 自由修改本機測試網址

### 使用時機

在本機測試時，有時候一個流程會橫跨web-app和web-fornt，但他們的dev server分別掛在不同的port，無法直接測試頁面互轉。這時候我們可以用nginx架一個Reverse Proxy來達成轉址，讓兩個專案用同一個port。

若再配合修改private/etc/hosts，這個方法也可以用來模擬production的domain name，騙過google, facebook和apple的social login，讓我們可以在本機測試第三方登入功能（但為了使用https，還需要自己製作憑證）。

### 作用

可以用一個單一的domain name（例如http://localhost:3010）同時測試web-app和web-front的網頁。

### 設定方法

### 1. 安裝nginx

```bash
brew install nginx
```

### 2. 編輯nginx的設定檔（自行修改其中port）

/opt/homebrew/etc/nginx/nginx.conf

[nginx.conf](https://prod-files-secure.s3.us-west-2.amazonaws.com/59e42f79-b84c-4653-b9d0-be24c6113394/5923c332-aeb2-4fab-b2d8-734e6eb7b900/nginx.conf)

### 3. 啟動nginx

```bash
#啟動
sudo nginx

＃停止
sudo nginx -s stop
```
