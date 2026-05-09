# 細胞實驗服務 — 生技細胞服務互動網站總專案

## 對話開始時請先讀
進度與最近更動都在 Obsidian：`secondbrain/細胞實驗服務/工作筆記.md`

## 專案簡介
為生技公司建立可供客戶瀏覽服務、提交訂單的互動式網站。
客戶端：瀏覽服務項目、輸入基因資訊、提交訂單。
後台：Firebase Firestore 自動接收訂單列表。

## 工作模式
- **加新功能**：對 Claude 說「我想做 XXX 功能」→ Claude 會建對應子資料夾、引導開發
- **結束工作**：對 Claude 說「**收工**」→ 自動 commit + push + 更新 Obsidian 工作筆記
- **接續工作**：對 Claude 說「**開工**」→ 讀工作筆記、報告進度、建議下一步

## 工作桌 + 三個家
- 📋 GDrive 工作桌：`G:\我的雲端硬碟\專案資料\細胞實驗服務\`（自動跨電腦同步）
- 🐙 GitHub repo：`weichankai-ops/cell-service`（公開，網頁的家）
- 📘 Obsidian 駕駛艙：`secondbrain/細胞實驗服務/工作筆記.md`（想法的家）
- 🔥 Firebase 專案：`biotech-tools`（資料的家）

## 功能清單
（之後加新功能時會自動更新）
- [ ] 服務瀏覽頁（細胞服務項目展示）
- [ ] 基因資訊輸入與訂單提交
- [ ] Firebase 後台訂單列表
- [ ] PWA 支援（可加入主畫面）
- [ ] Unsplash 生技圖庫整合
- [ ] AI 生圖功能（gpt-image-2）

## 技術架構
- **前端**：HTML/CSS/JavaScript（或 React）
- **後端資料庫**：Firebase Firestore
- **圖片**：Unsplash API
- **AI 生圖**：OpenAI gpt-image-2
- **部署**：GitHub Pages 或 Firebase Hosting
- **PWA**：manifest.json + service-worker.js

## 工作注意事項
- 客戶個資一律遵循個資保護（只存必要欄位）
- commit 訊息要寫清楚做了什麼 + 為什麼
- 收工前說「收工」讓 Claude 同步三方
- API Key 不要 commit 進 GitHub（已加 .gitignore）
- `.claude/` 一定要排除（含 token 設定）
