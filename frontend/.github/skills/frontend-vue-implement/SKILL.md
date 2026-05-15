---
name: frontend-vue-implement
description: Vue 3、Vuetify 3、TypeScript 前端實作 Skill。用於新增、修改、修正、重構 component、page、composable、form、table、dialog、layout、UI、API 串接與前端互動邏輯。關鍵字：Vue 3, Vuetify 3, TypeScript, frontend, component, page, composable, UI, layout, form, table, dialog, API, implement, refactor, fix bug.
---

# 前端實作 Skill

## 使用時機

使用者要求以下任務時，使用此 skill：

- 新增前端功能
- 修改前端功能
- 修正前端 bug
- 重構 Vue component
- 實作 Vuetify UI
- 實作 form、table、dialog、layout
- 實作 composable
- 串接 API
- 調整前端互動邏輯

## 執行流程

1. 先理解需求。
2. 若需求不清楚，先詢問使用者。
3. 若資訊不足，先詢問使用者。
4. 若條件衝突，先詢問使用者。
5. 先提出簡短實作規劃。
6. 再產生或修改程式碼。
7. 完成後說明修改內容與驗證方式。

## 實作限制

- 只完成使用者指定的任務。
- 不得自行延伸功能。
- 不得主動寫測試。
- 不得任意修改無關檔案。
- 不得任意改變既有架構。
- 不得任意改變 props、emits、slots、API contract 或資料結構。
- 不得自行導入新套件、新 UI library 或新狀態管理工具。

## Vue / TypeScript 規則

- 優先使用 Vue 3 Composition API。
- 優先使用 `<script setup lang="ts">`。
- 必須定義明確 TypeScript 型別。
- 避免使用 `any`。
- `computed` 只用於衍生狀態。
- `watch` 只在需要副作用時使用。
- template 避免複雜 inline expression。
- event handler 使用 `handleXxx` 命名。

## Vuetify 規則

- 優先使用 Vuetify 3 元件。
- 優先使用 Vuetify layout。
- 優先使用 Vuetify utility classes。
- 優先使用 `v-container`、`v-row`、`v-col`、`v-card`、`v-btn`、`v-dialog`、`v-form`、`v-text-field`、`v-select`、`v-data-table`。
- 不自行重造 Vuetify 已提供的基礎元件。
- 不自行覆寫 Vuetify 內部 class，除非沒有其他合理方式。

## CSS 規則

- 若必須自行寫 CSS，優先使用 `flex`、`grid`、`gap`。
- 不使用 float。
- 不使用 table layout 做頁面排版。
- 不大量使用 absolute positioning。
- CSS 優先 scoped。
- 不用大量 custom CSS 取代 Vuetify utility classes。

## 暗/明主題（Theme）支援

- 必須支援暗色與亮色主題，包含系統偏好偵測（`prefers-color-scheme`）與使用者切換。
- 優先使用 Vuetify 主題系統或全域 CSS 變數（CSS variables，`--token`），避免在元件中硬編碼顏色。
- 初始主題選擇順序：`localStorage` 儲存的偏好 → `prefers-color-scheme` → 預設 `light`。
- 儲存偏好建議使用 `localStorage` 或專案既有的 state（例如 Pinia）。
- 元件應使用代幣/變數（例如 `var(--bg)`, `var(--surface)`, `var(--text)`, `var(--primary)`），不要直接使用 hex 或 rgba。
- 提供一個 `ThemeToggle` 元件，切換時同步更新全域 state 與 Vuetify 的主題設定並儲存偏好。
- 建議採漸進改造：先更新 header、button、card 等常用元件，再逐步替換其餘元件的色彩用法。
- 必須執行色彩對比檢查，常規文字目標對比度 >= 4.5:1（大字 >= 3.0:1）。
- Code review 時檢查是否有硬編碼顏色、是否使用代幣/變數，以及是否符合對比度與可及性要求。

## 程式碼品質

- 優先可讀性。
- 優先維護性。
- 命名必須清楚。
- coding style 必須一致。
- 方法不要切太細。
- 不得過度設計。
- 只有在能降低複雜度或提升維護性時，才使用設計模式。