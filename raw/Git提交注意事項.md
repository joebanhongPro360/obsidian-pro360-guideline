---
title: Git提交注意事項
source:
  - https://www.notion.so/pro360-co/Git-1069b837ab1080b88a20f23da420b6aa
updated: 2026-05-20 09:30:23 CST
---

## Notes

- 本檔為 `raw/` 原始資料整理檔，內容以 Git commit、branch control、review process 與 hotfix 注意事項為準。
- 保留 commit message type、ticket number、branch、Merge Request、Code Summary、tag 與 hotfix 規則，不補猜測內容。
- Release 計畫確認方式、deploy branch 正式名稱、reviewer、CI 與 hotfix 回補流程待補。

## Git Commit and Branch Workflow

commit message 格式如下：

[{Type}] {jira-no}: message..Type: 主要是快速了解這個commit主要的目的

Feature：新功能/功能變更，因為有新的spec才新增的code

Bug：依照原有的spec進行修正，或是效能、經驗問題的修正，通常來自bug板或是測試未通過的修正

Maintain: 為了架構或是程序上的調整，應不影響任何功能，可能來自套件升級或是程式碼的排版、寫法調整等

Adjust: 其他不屬於上面的微調，不影響功能與邏輯，通常是UI或是文案的調整// 若內容包含則多個依序選一個即可：Feature > Bug > Maintain > Adjust範例：

新功能開發

[Feature] WEB-1234: new feature (WIP)

[Adjust] WEB-1234: ui update

若是測試未通過的修正可能會長這樣

[Bug] WEB-1234: test case xxx fixed (edited)

確保commit都有對應的ticket no

基本上一個commit應該盡量專注在一個目標上，同時進行的東西若是獨立的問題可以分開commit，使用同一個單號也沒問題

[AI Notes](https://www.notion.so/AI-Notes-1219b837ab10809baf02d250c9752081?pvs=21)

Branch Control  & Review Process:

- 新功能開發需在master建立新的branch進行開發，確認完成功能開發，需確認release計畫，始可合併於master中。
- 已上線的Bug修復，可直接提交於master上(若未被排入release請與提出)
- 當功能開發完成或是定期release版本，需發起Merge Request，並在此階段中進行code review，並記錄於MR的敘述中
- 當staging測試完成需進行發布前，再次發起Merge Request 進入deploy branch，並將此次release 相關檔案變動清單記錄於MR敘述中(Code Summary)

關於Hotfix：

- 目標要快速修正線上版本，從deploy branch分出來，用於快速修正/緊急釋出/**暫時版本**
- 使用hotfix/xxxxxx作為branch name
- 若有發布一樣要添加Tag
- 暫時性版本不會merge回depoly/master

[PRO360系統術語](https://www.notion.so/PRO360-bf5db664acfc471d8a08459eecee9179?pvs=21)
