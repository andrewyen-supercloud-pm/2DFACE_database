# Formulation：從規格文本產出規格模型

## 目標
從原始規格文本中萃取並結構化為規格模型，包含：
1. **資料模型 (Data Model)**：以 DBML 格式描述實體關係模型 (ERM)
2. **功能模型 (Functional Model)**：以 Gherkin Language 描述功能規格

---

## 執行步驟

### 1. 從規格中萃取資料模型 (Data Model)
從原始規格文本中識別並萃取資料實體及其關係，依照 [`formulation-rules.md`](./formulation-rules.md) 中的「資料模型萃取規則」執行：
- A. 識別「實體 (Entity)」
- B. 萃取實體的「屬性 (Attribute)」
- C. 標註「跨屬性不變條件」
- D. 識別實體之間的「關係 (Relationship)」
- E. 記錄實體的整體說明

### 2. 從規格中萃取功能階層：Feature > Rule > Example
依照 [`formulation-rules.md`](./formulation-rules.md) 中的「功能模型萃取規則」執行：
- A. 萃取「功能 (Feature)」
- B. 萃取功能的「規則 (Rule)」
- C. 萃取規則的「例子 (Example)」

### 3. 輸出規格檔案
依照 [`formulation-rules.md`](./formulation-rules.md) 中的「輸出格式規範」執行：
- A. 輸出資料模型（DBML 格式）→ `spec/erm.dbml`
- B. 輸出功能模型（Gherkin Language 格式）→ `spec/features/*.feature`

---

## 核心原則

**詳見 [`formulation-rules.md`](./formulation-rules.md)**，關鍵原則包括：
- **無腦補或任意假設原則**：嚴格遵守原始規格文本內容，不擅自假設或補充
- **規格表達格式**：DBML (資料模型) 與 Gherkin Language (功能模型)
- **原子化規則**：每個 Rule 只驗證一件事
- **句型一致性**：Feature File 中的 Step 定義保持句型一致