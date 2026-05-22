---
description: Vue 3 + Vuetify 3 + TypeScript 前端開發指令
applyTo: "**/*.{vue,ts,tsx,js,jsx}"
---

# Vue 前端開發指令

## 🧠 1. 工作流程（最高優先）

- 實作前必須：
  1. 理解需求
  2. 定義成功標準
  3. 提出簡短規劃（範圍 / 方法 / 成功標準）

- 若有問題：
  - 不清楚 / 不足 / 衝突 → **先詢問**
  - 不得自行假設（必要時需列出假設）

- 任務原則：
  - 僅做被要求的事情
  - 長任務需分階段（checkpoint）
  - 失敗不可隱藏，需明確說明

---

## 🎯 2. 實作範圍控制

- 僅實作需求功能
- 採「外科手術式修改」（最小變更）
- 不改動無關程式碼
- 不擴充功能

👉 建議可提供，但：
- 必須獨立區塊
- 不可直接實作

---

## 🧩 3. 技術基本原則

- Vue 3 Composition API
- `<script setup lang="ts">`
- 必須使用 TypeScript
- 避免 `any`（必要時需說明）

---

## 🧾 4. 型別規範（全部要有型別）

必須定義：

- props / emits
- API response
- form model
- table row

補充：

- nullable / optional 必須明確處理
- 不濫用 type assertion

---

## ⚙️ 5. Vue 使用規則

- 不得修改 props
- computed：
  - 僅做衍生資料
  - 不可有副作用
- watch：
  - 僅用於副作用
- template：
  - 不放複雜邏輯
- event 命名：
  - `handleXxx`

---

## 🎨 6. UI / Vuetify 原則（強制）

- **務必使用 Vuetify 元件與其官方 layout / utility**
- 不得重造 Vuetify 已提供元件
- 不得使用 custom UI 取代 Vuetify
- 不得導入其他 UI library（除非明確要求）

---

## 📐 7. Layout / CSS

- 優先 Vuetify utility
- 使用 flex / grid（gap）
- CSS 必須 scoped

禁止：

- float
- table layout
- 大量 absolute

---

## 🌗 8. Theme（必要）

- 必須支援 dark / light
- 使用：
  - Vuetify theme 或 CSS variables
- 禁止：
  - 硬編碼顏色

---

## 🔌 9. API / 狀態

- 不改 API contract
- 必須處理：
  - loading / error / empty
- 不得吞錯誤
- 若已有 Pinia → 必須沿用

---

## 🤖 10. AI 使用限制

- 不可把「確定性邏輯」交給 AI
  - 例如：條件判斷 / 流程控制

---

## 📤 11. 回覆格式（固定）

1. 需求理解
2. 實作規劃
3. 實作
4. 建議（可選）

---

## ❌ 禁止事項（總結）

- 不新增功能
- 不新增套件 / UI / 狀態工具
- 不修改無關程式碼
- 不過度設計
- 不隱藏錯誤