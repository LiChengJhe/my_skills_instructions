---
name: frontend-vue-code-review
description: Vue 3 + Vuetify 3 + TypeScript 前端 Code Review
---

# 前端 Code Review Skill

## 🧠 1. Review 原則（最高優先）

- 以「需求正確性」優先，其次才是技術品質
- 僅指出「重要問題」，避免雜訊
- 問題需分類：
  - 必須修（錯誤 / 風險）
  - 建議修（品質 / 維護性）
  - 可選（優化）

---

## 🔍 2. Review 流程（固定順序）

1. 需求符合度
2. 核心技術（Vue / TS / Vuetify）
3. UI / Layout
4. API / 狀態
5. 可讀性 / 維護性
6. 效能
7. 測試建議

---

## 🎯 3. 需求符合度（最重要）

檢查：

- 是否符合需求
- 是否：
  - 多做
  - 少做
  - 偏離
- 是否有未說明假設

👉 若此階段失敗，直接判定「需修改」

---

## 🧩 4. 核心技術檢查

### Vue

- 必須：
  - Composition API
  - `<script setup lang="ts">`
- 不得：
  - 修改 props
- 避免：
  - computed 有副作用
  - watch 濫用
  - template 複雜邏輯

---

### TypeScript

- 不得濫用 `any`
- 必須有型別：
  - props / emits
  - API response
  - form / table
- nullable 必須正確處理
- 避免不安全 assertion

---

### Vuetify（強制）

- 必須使用 Vuetify 元件 / layout / utility
- 不得：
  - 重造元件
  - 用 custom UI 取代
- 不得硬編碼顏色（應用 theme / token）

---

## 🎨 5. UI / Layout

- 使用 flex / grid（避免 float / table）
- CSS：
  - 必須 scoped
  - custom CSS 應最小化
- 不得：
  - 大量 absolute

### Theme 檢查

- 支援 dark / light
- 不得硬編碼顏色
- 對比度需合理
- 支援 prefers-color-scheme + persist

---

## 🔌 6. API / 狀態

必須處理：

- loading
- error
- empty

檢查：

- 是否吞錯
- 是否有 race condition
- 是否重複 API 邏輯
- 是否改 API contract

---

## ♻️ 7. 可讀性 / 維護性

- 命名清楚
- 方法不過長、不過度拆分
- 無重複邏輯
- 不過度設計

檢查：

- 是否影響 props / emits / API 相容性
- 是否不必要抽象（composable / pattern）

---

## ⚡ 8. 效能

- 避免：
  - 不必要 re-render
  - template 重運算
  - deep watch 濫用
- list / table：
  - 是否需要 pagination / virtual scroll

---

## 🧪 9. 測試建議（Playwright）

- 僅提供建議，不產生測試碼
- 優先：

  - 正常流程
  - 錯誤情境
  - loading / empty
  - 表單驗證
  - 關鍵互動

- Theme 測試：
  - dark / light 切換
  - 偏好 persist

---

## 📤 10. 回覆格式（固定）

### Review 結論
- 結論：通過 / 需修改 / 有風險
- 主要原因：

---

### 必須修改
- 嚴重問題（bug / 風險 / 需求錯）

---

### 建議修改
- 可讀性 / 型別 / Vuetify / 結構改善

---

### 可選建議
- 非必要優化

---

### 測試建議
- 僅列情境，不寫測試碼