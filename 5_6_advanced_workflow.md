# Day 5｜進階工作流程：檔案管理與任務切換

## 🚀 **前言**
經過前四天的學習，我們已經掌握了完整的 Git 協作流程。今天要學習兩個實用的進階技巧：如何管理忽略檔案，以及如何在多個任務間切換。

---

## 📁 一、忽略檔案管理

### 1.1 為什麼需要 .gitignore？
- 排除敏感資訊（密碼、API 金鑰）
- 避免大型檔案（編譯結果、套件資料夾）
- 排除暫存檔和系統檔案
- 保持倉庫整潔

### 1.2 建立 .gitignore 檔案
1. 在專案根目錄建立 `.gitignore` 檔案
2. 每行寫入一個要忽略的規則
3. 儲存後立即生效

### 1.3 常見忽略規則
```gitignore
# 依賴套件
node_modules/
vendor/

# 環境設定檔
.env
.env.local

# 編譯結果
dist/
build/

# 日誌檔案
*.log
logs/

# 作業系統檔案
.DS_Store
Thumbs.db

# IDE 設定檔
.vscode/
.idea/
```

、

---

## 🔄 二、工作暫存（Stash）

### 2.1 什麼是 Stash？
Stash 可以將未完成的修改暫時保存，讓工作區回到乾淨狀態，方便處理其他任務。

### 2.2 什麼時候使用 Stash？
- 緊急修正 bug 時
- 需要切換分支但修改未完成
- 實驗性代碼需要暫存

### 2.3 在 Sourcetree 中使用 Stash
1. 點擊「Stash」按鈕
2. 輸入描述（例如：「修正登入邏輯到一半」）
3. 選擇要暫存的檔案
4. 點擊「OK」保存

### 2.4 恢復 Stash
- **Apply Stash**：套用修改但保留 stash
- **Pop Stash**：套用修改並刪除 stash


---

## ⚡ 三、進階 Git 操作

### 3.1 Reset：回退 Commit
- **Soft**：保留檔案修改
- **Mixed**：保留修改但回到 Unstaged 狀態
- **Hard**：完全清除（⚠️ 小心使用）

### 3.2 Cherry Pick：選擇性合併
從某個分支選擇特定的 commit 套用到目前分支

### 3.3 Rebase：整理 Commit 歷史
- 合併多個小 commit
- 修改 commit 訊息
- 重新排序 commit

### 3.4 Reverse Commit：撤銷 Commit
建立新的 commit 來取消之前的修改，保留完整歷史

、

---

👉 [回到全輯篇](final_summary.md)
