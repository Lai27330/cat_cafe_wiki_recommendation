---
layout: page
type: log
title: Wiki 日誌
---

# Wiki 日誌

> 只能往後新增，不可修改舊紀錄。查最近 5 筆：`grep "^## \[" wiki/log.md | tail -5`

## [2026-11-15] schema | 建立 AGENTS.md 初版
- 建立三層架構、頁面格式、Ingest／Query／Lint 流程與網站發布規則

## [2026-11-15] schema | 新增「收到網址時」的處理規則
- AGENTS.md 新增 6.0 節：網路文章以「重點筆記」形式存入 raw/articles/，不收錄全文與照片

## [2026-11-15] ingest | Ruby｜Nekocoffee 貓珈貓咖推薦文
- 新增：raw/articles/2026-06-21-nekocoffee-ruby.md
- 新增：sources/2026-06-21-nekocoffee-ruby.md、cafes/taipei-nekocoffee.md、regions/taipei.md
- 新增：topics/pricing-models.md、topics/visiting-etiquette.md、overview.md、index.md
- 待確認：公休日、訂位方式、店貓數量與名字、是否送養、官方連結
- 線索：文末提到 7 家店，只有連結或摘要，已記在 overview.md 的「待蒐集」

## [2026-11-15] ingest | 批次整理 5 篇推薦文（擴充全台資料）
- 新增 raw：2026-08-26-taiwan-14-cat-cafes-bella、2026-04-05-taipei-10-cat-cafes-funliday、2025-10-02-taichung-3-cat-cafes-readygo、2023-08-09-most-cats-top5-beauty321、2026-02-21-bankemao-yam
- 新增店家頁 29 家（共 30 家，含已歇業 3 家）
- 新增地區頁：new-taipei、taoyuan、taichung、chiayi、tainan、kaohsiung、yilan；改寫 taipei
- 新增主題：adoption-cafes、kid-friendly；改寫 pricing-models、visiting-etiquette
- 改寫 overview.md、index.md
- 矛盾：FUFU 品種描述不一致；半刻貓貓咪數量（24／20 幾）不一致
- 時效：2023 年資料的 4 家店狀態改為「待確認」
- 線索：珈琲部已建立頁面；其餘 6 家仍在待蒐集；新線索記入 raw/inbox.md

## [2026-11-15] schema | 新增延伸應用規則（notes → 逐頁稿 → HTML 簡報）、待讀清單、照片規則
- 詳見 AGENTS.md 第 11、12 節與第 9 節第 3 條

## [2026-11-15] note | 第一次去貓咖要知道的事
- 新增：notes/2026-11-15-first-visit-guide.md（引用 9 個 Wiki 頁面）
- 搜尋到 3 篇 Wiki 尚未收錄的資料，列為建議參考文獻並加入 raw/inbox.md

## [2026-11-15] slides | 第一次去貓咖，先看這 3 分鐘
- 新增：slides/2026-11-15-first-visit-guide.md（8 頁，約 3 分鐘）

## [2026-11-15] deck | 第一次去貓咖，先看這 3 分鐘
- 新增：decks/_template.html（簡報模板）、decks/2026-11-15-first-visit-guide/index.html
- 更新：_data/decks.yml

## [2026-11-15] site | 建立 GitHub Pages 網站
- 新增：_config.yml、_layouts（default、home、page、cafe）、_includes/cat.svg、_data（cities、decks）、assets/css/style.css、index.md

## [2026-11-16] schema | 具體化視覺風格與網站頁面結構
- AGENTS.md 第 10 節改寫：10.2 頁面結構（首頁順序、店家卡片欄位、店家頁兩層）、10.3 網站配色與插圖、10.4 簡報霧綠配色
- 店家 frontmatter 新增 hours、highlights（5.1）

## [2026-11-16] site | 網站與簡報改版
- 新增 _includes/art/（cat-hero、cat-face、cat-peek、paw 四個原創 SVG），移除舊的 cat.svg
- 首頁店家卡片改為顯示位置、店貓、用餐時間；店家頁改為「重點卡＋看更多」兩層
- CSS 加入蜂蜜黃、珊瑚粉點綴色
- decks/_template.html 改為霧綠色系，重新產生 decks/2026-11-15-first-visit-guide/

## [2026-11-16] ingest | 30 家店家頁新增 hours、highlights 欄位
- 內容沒有新增事實，亮點皆出自各頁原有且附來源的資訊
- notes/2026-11-15-first-visit-guide.md 的 based_on 日期已同步；內容不受影響，不需重新產生
