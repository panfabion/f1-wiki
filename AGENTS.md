# 給 AI 的專案開發指南：F1 賽車策略與觀賽知識庫 (F1 Wiki)

## 1. 專案目的 (Project Context)
本專案是一個關於 Formula 1 (一級方程式賽車) 的輕量級靜態知識庫。
網站旨在幫助剛接觸 F1 的新手了解車隊資訊、賽道特性以及輪胎策略。
未來擴充時，AI 必須嚴格遵守下述的排版與結構規範，以確保所有頁面風格一致。

## 2. 專案結構 (Directory Structure)
專案採純靜態網頁架構，請依照以下結構放置檔案：
- `/index.html` : 網站首頁（目錄與最新資訊）
- `/pages/` : 存放所有子頁面（如 `ferrari.html`, `tyre-strategy.html`）
- `/css/style.css` : 全域樣式表
- `/AGENTS.md` : AI 開發指南（本檔案）

## 3. 技術堆疊 (Tech Stack)
- HTML5 (語意化標籤)
- Tailwind CSS (透過 CDN 引入 `<script src="https://cdn.tailwindcss.com"></script>`)
- 不使用任何前端框架 (React/Vue) 或後端資料庫。

## 4. 設計與排版規範 (Design Rules)
- **配色主題**：以深色模式為主（背景 `bg-gray-900`），文字為白色/淺灰（`text-gray-100`），強調色使用 F1 經典紅（`text-red-600` 或 `bg-red-600`）。
- **導覽列 (Navbar)**：每個頁面頂部都必須包含相同的導覽列，帶有「回首頁」、「車隊介紹」、「輪胎策略」等連結。
- **卡片式設計**：展示車隊或賽道資訊時，統一使用圓角卡片（`rounded-lg bg-gray-800 p-6 shadow-md`）。

## 5. 新增頁面的標準作業流程 (Workflow for AI)
當使用者要求「新增一個關於 [某主題] 的頁面」時，AI 必須：
1. **確認檔案名稱**：將頁面建立在 `/pages/` 下，使用全小寫英文及連字號（例：`red-bull.html`）。
2. **複製模板**：確保新頁面包含與首頁相同的 HTML head (包含 Tailwind CDN) 以及 Navbar。
3. **套用結構**：
   - 必須有一個 `<h1>` 標題（包含相關 Emoji）。
   - 必須有一段 2-3 句的簡介。
   - 必須使用條列式 (`<ul>`, `<li>`) 或表格 (`<table>`) 來呈現數據或重點。
4. **輸出**：直接輸出完整的 HTML 程式碼，不需省略。S