# 首頁維護說明（給 Claude Code 與 Codex）

個人首頁 https://mjib007.github.io/ ，只有一個 `index.html`（英文為主，滑鼠移過去顯示中文：`data-bi` 加 `.en`／`.zh`）。

## 首頁順序

封面（含 NEW 公告列）→ **最新消息 Latest News** → **課程網站 Course Sites**（目前重點）→ About → Platform → Stack → Earlier Open Source Work → Contact

## 最新消息：什麼時候要更新

有重要的新發展就更新，例如：新課程網站上線、新系列影片、演講或研討會、重大改版。小修正、單支影片不用。

## 最新消息：怎麼更新

1. `<!-- NEWS -->` 區塊：標題 `section-title` 換成新消息；內容放在 `.news-item`（左邊影片或圖片，右邊日期 `.news-date`、標題 `.news-title`、說明 `.news-desc`、連結 `.news-links`）。
2. **新的放最上面**。同時保留最多 3 則；更舊的移除，或改成一行連結放在消息下方。
3. 封面的 `.hero-news` 公告列換成最新一則（格式：`NEW` + 日期 · 英文短標 · 中文短標 →），連到 `#news`。
4. 日期用英文月份（例：Nov 21, 2026）；中文說明寫在 `.zh`。
5. 影片用 `https://www.youtube-nocookie.com/embed/<影片ID>` 嵌入；本機用 file:// 開會顯示錯誤 153，要用 `python -m http.server` 開網址預覽。
6. 預覽電腦（1280 寬）與手機（375 寬），確認沒有橫向捲動、沒有主控台錯誤，再請 Jackie 確認。
7. **推送前一定先問 Jackie。** commit 後 GitHub Pages 約 30–60 秒更新。

## 目前的最新消息

- 2026-11-21：TAAI 2026 國際研討會簡報影音（中文 https://youtu.be/3Iz3-9Vrx1o ，英文 https://youtu.be/4W_V0Ph81s0 ）

## 訪客計數器

封面按鈕下方的 `.visitor-count`，用 visitor-badge.laobi.icu（與刑法網站相同服務），`page_id=mjib007.github.io`。每載入一次加 1，所以全頁只能放一個；本機預覽也會計數，預覽次數不要太多。

## 課程區（Jackie 的重點：申論題動畫影片＋互動講義）

`<!-- COURSES -->` 由上到下：
1. 主標「Bar-Exam Essay Questions, Animated」與中文副標（中文直接顯示，不要藏在滑鼠移過去才出現）。
2. `.showcase` 兩張示意圖：動畫影片（`assets/essay-video.jpg`）、互動講義（`assets/essay-handout.jpg`）。
3. 「挑一題試試」`.essay-grid`：6 張申論題卡片，連到民法網站的 `lectures/exam-*.html`；按鈕連到民法網站 `#library`。有新的代表性題目時可替換，維持 6 張。
4. 「各科課程網站」`.course-grid`：新增課程網站時加一張 `.course-card`（科目英中名、該網站首頁的引題、英文簡介、中文 `.zh`）。
