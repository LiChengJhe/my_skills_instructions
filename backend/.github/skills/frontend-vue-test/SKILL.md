---
name: frontend-vue-test
description: Vue 3 + Vuetify 3 + TypeScript Playwright 測試
---

# 前端 Playwright 測試 Skill

## 🧠 1. 使用條件（強制）

僅當使用者明確要求時才使用：

- 寫測試 / 補測試
- Playwright / E2E / UI / 流程測試

---

## 🎯 2. 測試原則（最高優先）

- 以「使用者操作流程」為核心
- 不測試實作細節
- 測試必須：
  - 可重複
  - 獨立
  - 有明確驗證結果

不得：

- 為覆蓋率寫測試
- 任意修改 production code（除非允許）

---

## 🧩 3. 執行流程

1. 確認測試範圍
2. 確認操作流程
3. 確認預期結果
4. 資訊不足 → 先詢問
5. 再產生測試程式碼

---

## ⚙️ 4. 測試框架（固定）

- 必須使用 Playwright
- 不得使用：
  - Vitest
  - Vue Test Utils
  - 其他測試工具（除非要求）

---

## 🔍 5. 測試覆蓋（核心情境）

優先涵蓋：

- 正常流程
- 錯誤情境
- loading / empty
- 表單與關鍵互動

（例：click、dialog、table、search、pagination）

---

## 🧪 6. Playwright 實作規則

### Selector（穩定優先）

優先使用：

- getByRole
- getByLabel
- getByText
- getByTestId

避免：

- Vuetify 內部 class
- DOM 結構依賴（nth-child 等）

---

### 等待策略

- 使用 locator assertion（例如 toBeVisible）
- 使用條件等待（非 timeout）
- 不以硬編碼 timeout 作為主要機制

---

### 命名

- 測試名稱需描述：
  - 情境 + 預期結果

---

## 📤 7. 輸出要求

必須說明：

- 新增測試案例
- 覆蓋的使用者流程
- 執行方式
- 可測性建議（若有）
