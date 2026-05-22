---
name: frontend-vue-implement
description: Vue 3 + Vuetify 3 + TypeScript 前端實作
---

# 前端實作 Skill

## 🧠 1. 工作流程（最高優先）

執行順序：

1. 理解需求
2. 定義成功標準
3. 提出實作規劃
4. 確認後才實作

### 異常處理

- 不清楚 / 不足 / 衝突 → 先詢問
- 不得自行假設需求（必要需列出）

### 任務原則

- 僅完成指定任務
- 長任務需分階段（checkpoint）
- 失敗需明確說明

---

## 🎯 2. 範圍控制（強制）

- 僅實作需求
- 採最小修改（外科手術式）

不得：

- 擴充功能
- 延伸應用
- 改架構 / API / schema
- 新增套件 / UI / 狀態工具
- 修改無關檔案
- 主動寫測試

---

## 🧩 3. 技術核心（Vue / TS / Vuetify）

### Vue / TypeScript

- Composition API + `<script setup lang="ts">`
- 必須有型別（props / emits / API / form / table）
- 避免 `any`

規則：

- 不改 props
- computed 無副作用
- watch 僅用於副作用
- template 不放複雜邏輯
- event → `handleXxx`

---

### Vuetify（強制）

- 必須使用 Vuetify 元件 / layout / utility
- 不得：
  - 重造元件
  - 用 custom UI 取代
  - 任意覆寫內部 class

---

## 🎨 4. UI / Layout

- 使用 flex / grid（gap）
- CSS：
  - scoped
  - custom CSS 最小化

禁止：

- float
- table layout
- 大量 absolute

---

## 🌗 5. Theme（必要，精簡版）

- 必須支援 dark / light
- 使用：
  - Vuetify theme 或 CSS variables
- 禁止：
  - 硬編碼顏色

基本要求：

- 支援 prefers-color-scheme
- 可切換並 persist（localStorage 或 state）
- 顏色需可讀（對比度合理）

---

## 🔌 6. API / 狀態

必須處理：

- loading
- error
- empty

不得：

- 吞錯誤
- 改 API contract

避免：

- 重複 API 邏輯
- race condition

---

## ♻️ 7. 程式碼品質

- 可讀性優先
- 命名清楚
- coding style 一致

避免：

- 過度設計 / 過度抽象
- 方法過長或過度拆分

---

## 📤 8. 回覆格式（固定）

1. 需求理解
2. 實作規劃
3. 實作內容
4. 建議（可選）