# Project Rules: LLM Wiki & Educational HTML Slides Generator

## 1. Directory Architecture
- `raw/`: 存放原始參考資料摘要與來源網址（不可隨意修改原始事實）。
- `wiki/`: 存放由 AI 整理後的結構化 Markdown 知識條目，必須包含 `wiki/index.md` 作為總目錄。
- `index.html`: 最終輸出的單頁式教學簡報（Single-file HTML/CSS/JS）。

## 2. Wiki Ingestion Workflow (新增知識規則)
當執行「Ingest 新資料」時，必須依序完成以下步驟：
1. 讀取 `raw/` 中的新檔案，提煉核心概念、專有名詞白話解釋與實務重點。
2. 在 `wiki/` 建立對應編號的 `.md` 檔案，並在文末附上原始參考網址（Source URL）。
3. 自動更新 `wiki/index.md`，加入新條目的連結與一句話摘要。

## 3. HTML Slide Generation Rules (簡報生成規範)
當根據 `wiki/` 生成或更新 `index.html` 時，必須嚴格遵守：
- **知識邊界**：僅能引用 `wiki/` 內已存在的知識，嚴禁引入外部未驗證的艱深概念。
- **教學易讀性**：目標受眾為「完全不懂該主題的初學者」。每張投影片（`.slide`）正文字數上限為 120 字，優先使用三欄卡片（`.grid-3`）、雙欄對比（`.grid-2`）或條列重點。
- **來源可追溯**：每張投影片最下方必須包含 `<div class="wiki-ref">`，明確標示該頁內容對應的 `wiki/` 檔案名稱。
- **互動功能**：必須保留進度條（`#progress`）、頁碼指示器及鍵盤左右鍵切換投影片功能，並支援手機版 RWD 響應式排版。