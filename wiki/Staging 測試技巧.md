# Staging 測試技巧

## Summary
- 觸發情境：在 Staging 環境驗證電話、信用卡綁卡、單次購點或相關測試流程。
- 參與角色：前端工程師、QA；實際分工待補。
- 產出物：Staging 測試時可使用的測試資料與注意事項。

## Steps
1. 電話驗證可使用 `098765432X`，並以任意四位驗證碼通過；`X` 的可用範圍待補。
2. 信用卡綁卡可使用 `4242 4242 4242 4242`，有效期限與 CVC 任意。
3. 其他測試卡號需參考 Tappay 或 Stripe 文件；實際對應服務與文件連結待補。
4. 單次購點可選用 WebATM，來源記錄此流程會自動完成。

## Related Knowledge
- 關聯產品：待補
- 關聯功能：電話驗證、信用卡綁卡、單次購點；對應產品頁待補。
- 關聯架構：[[環境與 API 文件]]

## Failure Modes
- 常見問題：Staging 測試資料可能只適用於測試環境，不能套用到 Production 或 Production Beta。
- 預防方式：測試前確認目前所在環境，並依 [[環境與 API 文件]] 區分 Staging、Production Beta 與 Production。
- 常見問題：Tappay 或 Stripe 測試卡號來源未收錄在 wiki。
- 預防方式：補入官方測試文件或內部付款測試文件。

## Open Questions
- `098765432X` 中 `X` 的允許值是任意數字，還是特定測試門號清單？
- 目前信用卡綁卡實際使用 Tappay、Stripe，或兩者都使用？
- WebATM 自動完成流程的適用範圍與限制是什麼？
- 電話驗證、綁卡與購點分別屬於哪些產品或 feature？

## Sources
- [[raw/staging測試技巧]]
