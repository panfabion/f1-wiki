# 🏎️ F1 Wiki — Formula 1 賽車策略與觀賽知識庫

[![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)](https://developer.mozilla.org/zh-TW/docs/Web/HTML)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)](https://tailwindcss.com/)
[![License: MIT](https://img.shields.io/badge/License-MIT-red.svg?style=for-the-badge)](LICENSE)
[![F1 Season Ready](https://img.shields.io/badge/F1-2025%2F2026_Ready-E10600?style=for-the-badge&logo=formula1&logoColor=white)](https://www.formula1.com/)

> **F1 Wiki** 是一個專為新進車迷與賽車愛好者打造的輕量級靜態觀賽指南。聚焦於 F1 (一級方程式賽車) 的頂級車隊背景、現役王牌車手陣容，以及決定勝負天平的倍耐力輪胎物理與進站策略博弈。

---

## 📖 專案特色 (Key Highlights)

- 🏎️ **三大頂級車隊專屬配色**：法拉利經典烈焰紅（Rosso Corsa）、紅牛賽車海軍藍（Navy & Gold）、賓士銀箭與馬石油湖水綠（Petronas Teal），視覺沉浸感十足。
- 🛞 **專業級輪胎策略指南**：深度解析倍耐力 18 吋 C1~C5 乾地配方、工作溫度窗口 (Working Windows)、雨胎排水幾何，以及 Undercut / Overcut / SC 廉價進站戰術。
- 🌙 **極致深色沉浸主題**：採用現代深灰黑底色 (`bg-gray-900` / `bg-gray-800`) 與流暢圓角卡片設計，兼具科技感與閱讀舒適性。
- ⚡ **純靜態零相依 (Zero Dependencies)**：無需複雜 Node.js 建置環境或後端伺服器，透過 CDN 即開即用，支援任何靜態託管（GitHub Pages、Vercel、Netlify）。
- 📱 **響應式佈局 (Responsive Design)**：完美支援手機、平板與寬螢幕桌機閱讀。

---

## 🗂️ 專案檔案結構 (Project Structure)

```text
F1-wiki/
├── AGENTS.md               # AI 開發規範與結構指南
├── README.md               # 專案說明文件 (本檔案)
├── index.html              # 網站首頁（三大車隊巡禮、輪胎導覽、新手觀賽核心）
└── pages/                  # 子知識庫頁面目錄
    ├── ferrari.html        # 法拉利車隊 (Scuderia Ferrari) 專題頁
    ├── red-bull.html       # 紅牛車隊 (Red Bull Racing) 專題頁
    ├── mercedes.html       # 賓士車隊 (Mercedes-AMG PETRONAS) 專題頁
    └── tyre-strategy.html  # 專業輪胎配方規格與策略博弈指南
```

---

## 🛠️ 技術堆疊 (Tech Stack)

| 項目 | 說明 |
| :--- | :--- |
| **結構核心** | HTML5 語意化標籤 (`<header>`, `<main>`, `<nav>`, `<table>`, `<ul>`) |
| **樣式框架** | [Tailwind CSS](https://tailwindcss.com/) (經由官方 CDN 輕量引入) |
| **字體與排版** | 跨平台無襯線字體與深色主題對比優化 |
| **圖示符號** | 原生 Emoji，不額外加載外部龐大圖標字體包，秒開無負擔 |

---

## 🎨 車隊主題視覺規劃 (Color Schemes)

每個車隊子頁面與首頁展示卡皆嚴格比對真實車隊塗裝設計：

| 車隊 | 主題色調 | Tailwind 類別 | 代表元素 |
| :--- | :--- | :--- | :--- |
| **法拉利 (Ferrari)** | 經典烈焰紅 | `text-red-600`, `bg-red-600`, `border-red-800` | 🐎 躍馬軍團、Tifosi、馬拉內羅總部 |
| **紅牛 (Red Bull)** | 賽車海軍藍 + 冠軍金 | `text-blue-400`, `bg-blue-600`, `border-blue-800`, `text-yellow-400` | 🐂 1.82 秒神級進站、Newey 空力創新 |
| **賓士 (Mercedes)** | 馬石油湖水綠 + 銀箭 | `text-teal-400`, `bg-teal-600`, `border-teal-800`, `text-cyan-300` | ⭐ 混動王朝 8 連霸紀錄、精密工程學 |

---

## 🚀 快速開始 / 本地預覽 (Getting Started)

本專案為純前端靜態頁面，不需安裝任何套件包或執行編譯：

### 方法一：直接點擊開啟
使用瀏覽器（Chrome、Edge、Safari 或 Firefox）直接雙擊開啟專案根目錄下的 `index.html` 即可瀏覽。

### 方法二：使用 VS Code Live Server
1. 在 VS Code 中安裝擴充套件 **Live Server**。
2. 在 `index.html` 按右鍵，選擇 **「Open with Live Server」**。
3. 瀏覽器將自動在 `http://127.0.0.1:5500` 開啟。

### 方法三：使用 Python 本地伺服器
```bash
# 進入專案根目錄
cd F1-wiki

# 啟動 Python 本地伺服器
python -m http.server 8000
```
瀏覽器訪問：`http://localhost:8000`

---

## 🌐 部署至 GitHub Pages

若要發布上線至 GitHub 免費靜態託管：

1. 將本專案推送到您的 GitHub 儲存庫：
   ```bash
   git init
   git add .
   git commit -m "feat: complete F1 Wiki with Big 3 teams and tyre strategy"
   git branch -M main
   git remote add origin https://github.com/<您的用戶名>/F1-wiki.git
   git push -u origin main
   ```
2. 進入 GitHub 儲存庫的 **Settings** &rarr; **Pages**。
3. 在 **Build and deployment** 下方的 **Source** 選擇 `Deploy from a branch`。
4. **Branch** 選擇 `main` 分支並指定根目錄 `/ (root)`，點擊 **Save**。
5. 稍等 1-2 分鐘，即可透過 `https://<您的用戶名>.github.io/F1-wiki/` 線上瀏覽！

---

## 🤝 開發規範 (Contributing Guideline)

專案嚴格遵循根目錄的 [AGENTS.md](AGENTS.md) 開發準則：
- **新增頁面規格**：建立於 `/pages/` 下，檔名採全小寫英文字母與連字號（例如 `mclaren.html`）。
- **結構要素**：需具有同款 Navbar、`<h1>` 主題標題（帶 Emoji）、2-3 句精闢簡介，並透過 `<table>` 與 `<ul>` 清單結構化呈現數據。
- **主題規範**：以深色主題（`bg-gray-900`）與圓角卡片（`rounded-lg bg-gray-800 p-6 shadow-md`）為基底。

---

## 📄 版權聲明 (Disclaimer)

* 本專案僅作為程式設計教學與賽車知識推廣交流之用。
* Formula 1、F1、FIA、Scuderia Ferrari、Red Bull Racing、Mercedes-AMG 及倍耐力 (Pirelli) 等相關商標及隊徽名稱版權歸各自官方所有。

Made with ❤️ by F1 Fans & AI Engineering.
