---
name: frontend-vue-code-review
description: Vue 3、Vuetify 3、TypeScript 前端 Code Review Skill。用於檢查 Vue component、Vuetify UI、TypeScript 型別、layout、CSS、API、狀態管理、可讀性、維護性、效能、PR 與 Playwright 測試建議。關鍵字：Vue 3, Vuetify 3, TypeScript, code review, PR review, frontend review, UI review, Vuetify review, Playwright test suggestion.
---

# 前端 Code Review Skill

## 使用時機

使用者要求以下任務時，使用此 skill：

- code review
- PR review
- 檢查前端程式碼
- 找問題
- 改善品質
- 檢查 Vue component
- 檢查 Vuetify UI
- 檢查 TypeScript 型別
- 檢查 CSS 或 layout
- 檢查 API 或狀態管理

## Review 流程

依序檢查：

1. 需求符合度
2. Vue 3 寫法
3. TypeScript 型別
4. Vuetify 使用方式
5. CSS / layout
6. API / 狀態
7. 可讀性
8. 維護性
9. 效能
10. Playwright 測試建議

## 需求符合度

- 是否符合使用者需求。
- 是否多做。
- 是否少做。
- 是否偏離需求。
- 是否有未說明的假設。

## Vue 3 檢查

- 是否使用 Composition API。
- 是否使用 `<script setup lang="ts">`。
- 是否直接修改 props。
- `computed` 是否只處理衍生狀態。
- `watch` 是否被濫用。
- template 是否有複雜 inline expression。
- component 職責是否清楚。

## TypeScript 檢查

- 是否有不必要的 `any`。
- props 是否有明確型別。
- emits 是否有明確型別。
- API response 是否有明確型別。
- form model 是否有明確型別。
- table row 是否有明確型別。
- nullable 或 optional 資料是否正確處理。
- 是否有不安全 type assertion。

## Vuetify 檢查

- 是否優先使用 Vuetify 3 元件。
- 是否優先使用 Vuetify layout。
- 是否優先使用 Vuetify utility classes。
- 是否自行重造 Vuetify 已有元件。
- 是否不必要覆寫 Vuetify 內部 class。
- form、dialog、table、card、button 是否使用合適 Vuetify 元件。
 - 是否優先使用 Vuetify 的主題系統或 tokens，並避免在元件中硬編碼顏色（hex/rgba）。

## CSS / Layout 檢查

- custom CSS 是否必要。
- 是否優先使用 flex、grid、gap。
- 是否使用 float。
- 是否使用 table layout 做頁面排版。
- 是否大量使用 absolute positioning。
- CSS 是否 scoped。
- responsive layout 是否合理。
 - 是否存在硬編碼顏色；是否使用全域代幣/變數或 Vuetify theme tokens。
 - 切換主題（light/dark）後所有元件顏色是否正確映射且無可視異常。
 - 是否檢查文字與背景的對比度（正常文字 >= 4.5:1，大型文字 >= 3.0:1）。
 - 是否考量 `prefers-color-scheme` 與儲存使用者偏好（localStorage 或 state）。

## API / 狀態檢查

- 是否處理 loading state。
- 是否處理 error state。
- 是否處理 empty state。
- 是否吞掉錯誤。
- 是否有 race condition 風險。
- 是否重複 API 邏輯。
- 是否自行改變 API contract。

## 可讀性與維護性

- 命名是否清楚。
- 方法是否過長。
- 方法是否過度拆分。
- 是否有重複邏輯。
- 是否過度設計。
- 是否不必要引入 composable、service、mapper、adapter 或設計模式。
- 是否影響既有 props、emits、slots、API contract 或相容性。

## 效能檢查

- 是否有不必要 re-render。
- 是否在 template 中執行昂貴運算。
- 是否有不必要 deep watch。
- table 或 list 是否需要 pagination、server-side query 或 virtual scroll。
- 是否有不必要的重複 map、filter 或資料轉換。

## Playwright 測試建議

- 只提出 Playwright 測試建議。
- 不直接產生測試碼，除非使用者要求。
- 測試建議以 E2E / UI 操作流程為主。
- 優先建議正常流程、錯誤情境、loading、empty state、表單驗證與關鍵互動。
 - 建議加入主題切換測試：確認 `ThemeToggle` 行為、偏好持久化、以及在兩種主題下主要元件（button、card、form）外觀與互動無誤。

## 回覆格式

## Review 結論

- 結論：通過 / 需修改 / 有風險
- 主要原因：

## 必須修改

- 列出會造成錯誤、風險、需求不符或破壞既有行為的問題。

## 建議修改

- 列出可讀性、維護性、Vuetify 使用方式、TypeScript 型別或 UI 結構改善建議。

## 可選建議

- 列出非必要但可提升品質的建議。

## Playwright 測試建議

- 列出建議補充的 E2E / UI 測試情境。
- 不直接產生測試碼，除非使用者要求。