# 喵咖日誌｜台灣貓咪咖啡廳 Wiki

一個由 AI 依照 **[AGENTS.md](./AGENTS.md)** 規則持續整理的台灣貓咪咖啡廳知識庫，參考 Andrej Karpathy 的「LLM Wiki」模式。

- 🌐 網站：`[https://Lai27330.github.io/cat_cafe_wiki_recommendation/](https://lai27330.github.io/cat_cafe_wiki_recommendation/)`
- 📘 AI 規則書：[AGENTS.md](./AGENTS.md)（Claude Code 透過 [CLAUDE.md](./CLAUDE.md) 自動讀取）

## 目前內容

- 30 家店（8 個縣市），4 個主題頁，6 份來源
- 1 份示範研究：筆記 → 逐頁稿 → 3 分鐘 HTML 簡報

## 架構

```
raw/       原始資料：網路文章的重點筆記、待讀清單（AI 唯讀，不發布）
wiki/      Wiki：店家、地區、主題、來源摘要、目錄、日誌（AI 維護，發布）
notes/     研究筆記：只根據 Wiki 撰寫（不發布）
slides/    簡報逐頁稿：只根據 notes 撰寫（不發布）
decks/     HTML 簡報：只根據逐頁稿製作（發布）
_layouts/  網站版型；首頁會自動依縣市列出所有店家
```

資料只往一個方向流動：`raw → wiki → notes → slides → decks`，下游不可以加入上游沒有的事實。

## 怎麼請 AI 繼續做

| 你說 | AI 會做 |
|---|---|
| 貼上一篇推薦文網址 | 存成 raw 重點筆記 → 建立／更新店家、地區、主題頁 → 更新目錄與日誌（AGENTS.md 6.0、6.1） |
| 「台北有哪些不限時的貓咖？」 | 先讀目錄，再根據 Wiki 回答並附連結（6.2） |
| 「檢查 Wiki」 | 找出矛盾、過時、斷連結、孤兒頁、過時的 notes（6.3） |
| 「研究：○○，做成簡報」 | notes → 逐頁稿 → HTML 簡報（第 11 節） |
| 「處理待讀清單」 | 逐筆 ingest `raw/inbox.md` 的資料 |

## 部署到 GitHub Pages

1. 在 GitHub 建立公開 repo，把本資料夾**裡面的所有檔案**上傳（`_config.yml`、`_layouts/` 等要在最外層）。
2. Settings → Pages → Source 選 **Deploy from a branch**，Branch 選 `main`、資料夾選 `/ (root)`，按 Save。
3. 約 1～3 分鐘後即可瀏覽。GitHub 會自動用 Jekyll 把 Markdown 轉成網頁，不需要在電腦上安裝任何東西。

## 本機瀏覽

用 Obsidian 開啟本資料夾即可瀏覽 Wiki（設定：Files and links → 關閉 Wikilinks、連結格式選相對路徑）。
