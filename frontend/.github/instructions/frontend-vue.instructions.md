---
description: Vue 3、Vuetify 3、TypeScript 前端開發指令。適用於 component、page、composable、UI、layout、form、table、dialog、API 與前端互動邏輯。
applyTo: "**/*.{vue,ts,tsx,js,jsx}"
---

# Vue 3 / Vuetify 3 / TypeScript 前端指令

## 🧠 工作流程

- 實作前必須先理解需求。
- 必須先定義「成功標準」再進行實作。
- 若需求不清楚、不足或衝突，必須先詢問使用者。
- 不得自行假設需求；若必須假設，需明確列出並等待確認。
- 實作前必須先提出簡短規劃（修改範圍 / 實作方式 / 成功標準）。
- 長任務需分階段進行，需回報進度（checkpoint）。
- 若任務失敗或無法完成，必須明確說明，不可靜默略過。

---

## 🎯 任務範圍

- 僅實作使用者要求的功能。
- 不得擴充或延伸未要求內容。
- 採「外科手術式修改」（只改必要範圍）。
- 可提供建議，但：
  - 必須放在「建議」區塊
  - 不可直接實作

---

## 🧩 基本技術原則

- 必須使用 Vue 3 Composition API。
- 必須使用 `<script setup lang="ts">`。
- 必須使用 TypeScript 型別。
- 避免 `any`：
  - 若必須使用，需說明原因並限制範圍。

---

## 🧾 型別規則

- props / emits 必須有明確型別
- API response 必須有型別
- form model 必須有型別
- table row 必須有型別
- nullable / optional 必須明確處理
- 不得濫用 type assertion

---

## ⚙️ Vue 規則

- 不得直接修改 props
- computed：
  - 僅用於衍生狀態
  - 不得有副作用
- watch：
  - 僅在需要副作用時使用
  - 不得濫用
- template：
  - 不得放入複雜 inline expression
  - 複雜邏輯應移至 computed / method
- event handler 命名：
  - 使用 `handleXxx`

---

## 🎨 Vuetify 規則

- 優先使用 Vuetify 元件 / layout / utility classes
- 不得重造 Vuetify 已提供元件
- 不得導入其他 UI library（除非明確要求）

### 元件優先順序

優先使用：

- `v-container` / `v-row` / `v-col`
- `v-card` / `v-btn` / `v-icon`
- `v-dialog` / `v-form`
- `v-text-field` / `v-select`
- `v-data-table`
- `v-alert` / `v-chip`
- `v-tabs` / `v-menu` / `v-list`

---

## 📐 CSS / Layout

- 優先使用 Vuetify utility classes
- 必須使用現代 layout（flex / grid / gap）
- 禁止：
  - float 排版
  - table layout
  - 大量 absolute positioning
- CSS 應使用 scoped
- 不得用 custom CSS 取代 Vuetify

---

## 🌗 主題（Dark / Light）

- 必須支援 dark / light mode
- 必須支援：
  - `prefers-color-scheme`
  - 使用者切換（persist）
- 使用：
  - Vuetify theme 或 CSS variables
- 禁止硬編碼顏色
- 必須確保：
  - hover / focus / disabled 可辨識
- 建議提供 `ThemeToggle`

---

## 🧱 Component 設計

- 職責需清楚
- 不得過度拆分
- 單次使用且簡單 → 不拆
- 重複 UI / 邏輯 → 才抽 component
- 重用邏輯 → 才抽 composable

---

## 🔌 API / 狀態管理

- 必須沿用既有 API 寫法
- 不得改變 API contract
- 必須處理：
  - loading
  - error
  - empty state
- 不得吞錯誤
- 若已有 Pinia → 必須沿用
- 不得導入新狀態管理工具

---

## 🤖 AI 使用邊界

- 不可將確定性邏輯交給 AI（如流程控制、狀態判斷）

---

## 🧪 測試規則

- 預設不寫測試
- 僅在使用者要求時撰寫
- 測試工具：Playwright
- 測試需驗證業務邏輯
- 若需補測試 → 放「建議」

---

## 📤 輸出規則

- 需求不明 → 先詢問
- 修改前 → 先給規劃
- 僅輸出必要內容
- 不可冗長或模糊
- 建議需獨立區塊

---

## ✅ 回覆流程

1. 需求理解
2. 實作規劃（含成功標準）
3. 實作內容
4. 驗證方式
5. 建議（可選）

---

## ❌ 禁止事項

- 不新增未要求功能
- 不新增測試
- 不導入新 UI / 套件 / 狀態工具
- 不修改無關程式碼
- 不得改變 public API / contract / schema。
- 不過度設計
- 不混用 coding style
- 不在未理解 context 下修改
- 不隱藏失敗

---
