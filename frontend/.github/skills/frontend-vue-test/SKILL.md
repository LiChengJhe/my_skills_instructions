---
name: frontend-vue-test
description: Vue 3、Vuetify 3、TypeScript 前端 Playwright 測試 Skill。只有在使用者明確要求寫測試、補測試、產生 Playwright 測試、E2E test、UI test 或流程測試時使用。關鍵字：Vue 3, Vuetify 3, TypeScript, Playwright, E2E, UI test, frontend test, test cases.
---

# 前端 Playwright 測試 Skill

## 使用時機

只有使用者明確要求以下任務時，才使用此 skill：

- 寫測試
- 補測試
- 產生 Playwright 測試
- E2E test
- UI test
- 流程測試

## 測試框架

- 固定使用 Playwright。
- 不使用 Vitest。
- 不使用 Vue Test Utils。
- 不使用其他測試框架，除非使用者明確要求。

## 執行流程

1. 先確認測試範圍。
2. 先確認測試頁面。
3. 先確認使用者操作流程。
4. 先確認預期結果。
5. 若資訊不足，先詢問使用者。
6. 再產生 Playwright 測試程式碼。

## 測試原則

- 優先測試使用者實際操作流程。
- 不測試實作細節。
- 不為了覆蓋率產生無意義測試。
- 測試必須可重複執行。
- 測試資料必須簡潔且明確。
- 測試之間不得互相依賴。
- 不得任意修改 production code，除非使用者同意。

## 覆蓋情境

優先覆蓋：

- 正常流程
- 錯誤情境
- loading state
- empty state
- 表單驗證
- button click
- dialog 開啟與關閉
- table 顯示
- filter
- search
- pagination

## Selector 規則

優先使用穩定 selector：

- role
- label
- placeholder
- text
- test id

避免使用不穩定 selector：

- Vuetify 內部 class
- 複雜 CSS selector
- DOM 階層位置
- nth-child

## Playwright 寫法

- 使用 Playwright locator。
- 使用 `getByRole`、`getByLabel`、`getByPlaceholder`、`getByText`、`getByTestId`。
- 不使用硬編碼 timeout 作為主要等待方式。
- 等待元素可見時，使用 locator expectation。
- 等待資料載入時，使用合理的等待條件。
- 測試名稱必須描述情境與預期結果。

## 完成回覆

完成後必須說明：

- 新增哪些測試案例。
- 覆蓋哪些使用者流程。
- 如何執行測試。
- 是否有可測性建議。