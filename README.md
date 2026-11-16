# BunnyCare

給第一次養兔的人的繁體中文照護知識庫，內容整理自《兔飼養與照顧指南》。

**網站：** https://r13250026.github.io/rabbit-care-wiki/

## 內容

網站分成四個章節，每章一個獨立頁面：

| 章節 | 頁面 | 重點 |
| --- | --- | --- |
| 一、認識兔子的基本習性 | `guides/basic-habits.html` | 生命週期、繁殖、換毛、磨牙、常見行為 |
| 二、適合兔子生活的環境 | `guides/living-environment.html` | 籠舍、溫度、飲水、每日飲食比例、環境豐富化 |
| 三、與兔子相處的技巧 | `guides/interaction-tips.html` | 單隻與多隻飼養、初次配對、正確抓抱 |
| 四、基本照護與醫療 | `guides/health-care.html` | 梳毛剃毛、日常觀察、異常徵狀、就醫須知 |

## 技術與風格

- 純原生 HTML5 + CSS3，沒有框架、打包工具或建置步驟。
- 視覺風格為「牧草燕麥手帳風」：點點筆記本底紋、深森林綠手繪邊框、硬陰影與紙膠帶裝飾。
- 字體使用 Google Fonts 的 Chiron GoRound TC（標題）與 Noto Sans TC（內文）。
- 支援桌面與手機瀏覽，手機版（寬度 640px 以下）首頁卡片自動轉為單欄。

## 專案結構

```
.
├── AGENTS.md          專案規則：AI 新增或修改內容時必須遵守
├── README.md          本文件
├── index.html         首頁
├── style.css          全站唯一樣式表
├── content/
│   └── source.md      原始指南全文（內容事實的唯一依據）
└── guides/            單篇照護指南
```

## 本機預覽

不需要安裝任何東西，直接用瀏覽器開啟 `index.html` 即可。

## 新增一篇指南

完整規則與檢查清單都寫在 [AGENTS.md](./AGENTS.md)，大致流程如下：

1. 先確認 `content/` 裡有該主題的來源資料。
2. 在 `guides/` 以英文小寫加連字號命名，建立新的 `.html` 檔案，套用既有的頁面骨架與元件。
3. 到 `index.html` 的 `#guide-grid` 新增對應的卡片。
4. 更新 `AGENTS.md` 的檔案結構，並逐項檢查完成前清單。

如果使用 AI 協助，請先讓它閱讀 `AGENTS.md`，再提出需求，例如：「請依照 AGENTS.md，新增一篇『夏季防中暑』指南。」

## 部署到 GitHub Pages

1. 把專案推送到 GitHub 的 `main` 分支。
2. 進入 repository 的 **Settings → Pages**。
3. **Source** 選擇 `Deploy from a branch`，**Branch** 選擇 `main`，資料夾選 `/ (root)`，按下 Save。
4. 等待約 1 到 2 分鐘，頁面上方會顯示網站網址。

專案所有連結都使用相對路徑，因此部署在子路徑下也能正常顯示。

## 內容來源與免責聲明

網站內容整理自《兔飼養與照顧指南》，原文收錄於 [`content/source.md`](./content/source.md)。本站為學習與整理用途，不能取代專業獸醫師的診斷。兔子出現食慾下降、排便減少或其他異常時，請儘速就醫。
