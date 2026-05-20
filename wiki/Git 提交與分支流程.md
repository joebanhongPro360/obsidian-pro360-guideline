# Git 提交與分支流程

## Summary
- 觸發情境：前端功能開發、Bug 修復、release、hotfix。
- 參與角色：開發者、reviewer、測試或 release 相關角色待補。
- 產出物：commit、branch、Merge Request、MR 描述、release 變更清單、tag。

## Steps
1. 撰寫 commit message，格式為 `[{Type}] {jira-no}: message`。
2. 確認每個 commit 都有對應 ticket number。
3. 盡量讓一個 commit 專注在一個目標；若同時處理多個獨立問題，可以拆成多個 commit，使用同一個單號也可以。
4. 新功能開發時，從 `master` 建立新的 branch。
5. 功能開發完成後，確認 release 計畫，才可合併至 `master`。
6. 功能開發完成或定期 release 時，發起 Merge Request，進行 code review，並將 review 記錄於 MR 描述中。
7. Staging 測試完成且準備發布前，再次發起 Merge Request 進入 deploy branch，並在 MR 描述中記錄本次 release 相關檔案變動清單，也就是 Code Summary。

## Commit Types
- `Feature`：新功能或功能變更，因為有新的 spec 才新增的 code。
- `Bug`：依照原有 spec 修正，或修正效能、使用經驗、bug 板回報、測試未通過等問題。
- `Maintain`：架構或程序調整，應不影響任何功能，例如套件升級、程式碼排版或寫法調整。
- `Adjust`：不屬於以上分類的微調，不影響功能與邏輯，通常是 UI 或文案調整。
- 若內容同時符合多個 type，優先順序為 `Feature > Bug > Maintain > Adjust`。

## Examples
- 新功能開發：`[Feature] WEB-1234: new feature (WIP)`
- UI 微調：`[Adjust] WEB-1234: ui update`
- 測試未通過修正：`[Bug] WEB-1234: test case xxx fixed`

## Hotfix
- 目標：快速修正線上版本，用於快速修正、緊急釋出或暫時版本。
- 分支來源：從 deploy branch 分出。
- Branch name：使用 `hotfix/xxxxxx`。
- 發布時：若有發布，一樣要添加 tag。
- 合併規則：暫時性版本不會 merge 回 deploy 或 `master`。

## Related Knowledge
- 關聯產品：待補。
- 關聯功能：待補。
- 關聯架構：[[前端架構地圖]]
- 關聯流程：[[工作流程地圖]]

## Failure Modes
- 常見問題：commit 缺少 ticket number、commit 混入多個不相關目標、MR 描述未記錄 code review 或 Code Summary。
- 預防方式：提交前檢查 commit message 格式；開 MR 時補齊 review 紀錄；release MR 補上本次 release 變更清單。

## Open Questions
- Release 計畫由誰確認？確認標準與文件位置待補。
- Deploy branch 的正式名稱與保護規則待補。
- Hotfix 不 merge 回 deploy 或 `master` 時，正式修補如何回補到後續版本待補。
- MR reviewer、CI 檢查、測試通過條件待補。

## Sources
- [[raw/版控/Git提交注意事項]]
