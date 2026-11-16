# 🐰 兔飼養與照顧知識庫 Rabbit Care Wiki

給第一次養兔的人的繁體中文照護知識庫，內容整理自《兔飼養與照顧指南》。

🌐 **線上瀏覽網址**：[https://r13250026.github.io/rabbit-care-wiki/](https://r13250026.github.io/rabbit-care-wiki/)

## ✨ 專案特色

* **系統化照護指南**：將繁雜的養兔知識拆解為四大核心主題，涵蓋從奶兔到老兔的完整生命週期、飲食黃金比例、居家環境安全與緊急醫療警訊。
* **語意化安全提醒設計**：針對攸關兔子健康的紅線規範（如 12 小時未進食急診警訊、飲食禁忌、禁止仰躺抱姿等），統一使用高辨識度的紅框警語元件呈現。
* **零依賴快速部署**：純原生 HTML5 + CSS3 開發，無需任何前端打包工具（如 Vite/Webpack）或後端資料庫，直接透過 GitHub Pages 即可託管上線。
* **AI 驅動的可擴充架構**：內建完整的 [`AGENTS.md`](./AGENTS.md) 開發規範，定義了檔案命名、HTML 元件骨架與雙向連動流程，讓 AI 能隨時依照同一套設計語言新增章節。

## 📂 專案結構

```text
bunny-care-wiki/
├── AGENTS.md                        # 核心開發規範：供 AI 理解專案架構與新增內容的規則書
├── README.md                        # 專案說明文件
├── index.html                       # 首頁：品牌標頭、導讀、核心警語、章節卡片網格
├── style.css                        # 全站統一樣式表
├── content/
│   └── source.md                    #《兔飼養與照顧指南》原文
└── guides/                          # 單篇照護指南頁面目錄
    ├── basic-habits.html            # 第一章：認識兔子的基本習性
    ├── living-environment.html      # 第二章：適合兔子生活的環境
    ├── interaction-tips.html        # 第三章：與兔子相處的技巧
    └── health-care.html             # 第四章：基本照護與醫療
```

## 🤖 如何使用 `AGENTS.md` 擴充新頁面？

本專案的核心設計在於「可持續擴充性」。未來若要新增新的主題頁面（例如「第五章：常見兔病百科」或「牧草種類營養比較」），只需對支援讀取專案檔案的 AI 工具（如 Claude Code、Cursor、GitHub Copilot 或 ChatGPT/Gemini）下達如下指令：

> **Prompt 範例：**
> 「請閱讀 `AGENTS.md`，嚴格遵守裡面的視覺元件與工作流程規範，幫我根據以下資料新增一篇『第五章：常見兔病百科』（檔名 `guides/common-diseases.html`），並同步更新 `index.html`。」

AI 將會自動執行以下標準化流程：
1. 在 `guides/` 下建立符合 kebab-case 命名的 HTML 檔案，並引入 `Chiron GoRound TC` 字體與 `../style.css`。
2. 自動將資料中的注意事項與表格映射為標準的 `.alert-box`、`.data-table` 與 `.step-list` 元件。
3. 同步開啟 `index.html`，在 `#guide-grid` 中插入一張結構一致的手帳風卡片（偶數張卡片會自動套用粉橘紅蘿蔔色紙膠帶）。
4. 嚴格遵守「樣式保護原則」，不改動既有的 `style.css`，確保全站風格高度統一。

## 🚀 本地預覽方式

由於本專案為純靜態網頁，無需安裝任何套件：
1. 將專案 Clone 或下載至本地端：
   ```bash
   git clone https://github.com/r13250026/bunny-care-wiki.git
   ```
2. 直接用瀏覽器開啟 `index.html`，或使用 VS Code 的 **Live Server** 擴充套件即可在瀏覽器預覽完整網站。

## 📄 內容參考與授權

網站內容整理自《兔飼養與照顧指南》，原文收錄於 [`content/source.md`](./content/source.md)。本站為課程專題實作與學習整理，不能取代專業獸醫師的診斷。兔子出現食慾下降、排便減少或其他異常時，請儘速就醫。
