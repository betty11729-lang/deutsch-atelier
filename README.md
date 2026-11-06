# Deutsch Atelier｜德語 A1 互動式學習手帳

這份專案已可以直接發布至 **GitHub Pages**，不需要 Node.js、不需要安裝套件、也不需要額外的建置步驟。

## 功能

- 26 週初學者文法學習進度、詳細文法說明與練習
- 104 篇預先編寫的分級閱讀（週六、週日各兩篇），逐句翻譯和解析
- 1,074 筆分類德語單字、名詞冠詞及單複數、非名詞 A1 例句
- 原文閱讀／隱藏翻譯、互動測驗與錯題複習
- 裝置內建德語語音合成（TTS；依裝置的語音支援而定）
- 手機優先、PWA 主畫面圖示、首次連網後可離線讀取快取網頁
- 瀏覽器儲存學習進度；可自行匯出/匯入進度 JSON

## 第一次發布（GitHub 網頁操作）

1. 開啟 https://github.com/new ，建立 **新的儲存庫**，建議名稱 `deutsch-atelier`。
2. 若你使用 GitHub Free，想要透過 GitHub Pages 公開瀏覽，請選擇 **Public**。不需要把課程和個人資料放進現有旅行專案。
3. 建立儲存庫後，在 **Add file → Upload files**，上傳此資料夾內的所有檔案，包含 `index.html`、`sw.js`、`manifest.webmanifest`、三個 PNG 圖示與 `.nojekyll`。**不要直接把 ZIP 壓縮檔上傳後就期待它成為網站。**
4. 按 **Commit changes** 儲存。
5. 前往 **Settings → Pages**，在 **Build and deployment → Source** 選擇 **Deploy from a branch**；設定 Branch 為 **main**、Folder 為 **/(root)**，按 **Save**。
6. 部署完成後，從 Settings → Pages 的 **Visit site** 開啟你的 HTTPS 網址。

如果 GitHub 帳號是 `YOURNAME`、新儲存庫是 `deutsch-atelier`，則網站通常位於：

`https://YOURNAME.github.io/deutsch-atelier/`

GitHub 官方文件：
- https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site
- https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site

## iPhone / iPad 安裝到主畫面

用 **Safari** 開啟部署完成的 HTTPS 網址，選擇 **分享 → 加入主畫面**。往後可以從主畫面開啟，不必下載 HTML 附件。

## 常見問題

**部署網址打開是空白？** 先確認 `index.html` 在儲存庫根目錄（而非多包一層資料夾）；Pages 設定為 `main`、`/(root)`；打開真正的 GitHub Pages HTTPS 網址，不要用 GitHub 原始檔預覽頁面。新版加上了沒有 JavaScript 時的靜態備援首頁。

**換手機為什麼進度不一樣？** 目前沒有登入系統或雲端資料庫；進度存在瀏覽器 localStorage。換裝置或清除網站資料前，請在 App 的「設定與進度備份」匯出 JSON，在另一個裝置匯入。這不等同於 ChatGPT 帳號同步。

**每週新閱讀會自動出現在網站嗎？** 不會。網站內的 104 篇是預先編寫的內容，ChatGPT 裡另外設定的週末閱讀屬於不同流程，尚未串接更新機制。

**GitHub Pages 網站是否公開？** 是。此版本不包含你的私人學習紀錄，但若你把自己的 JSON 進度備份上傳至公開儲存庫，別人就可能讀到；請不要這樣做。

## 檔案結構

- `index.html`：主網站；包含課程、文法、閱讀、詞庫及互動邏輯
- `manifest.webmanifest`：PWA 安裝資訊
- `sw.js`：網站離線快取
- `icon-180.png`、`icon-192.png`、`icon-512.png`：App 圖示
- `.nojekyll`：停用 GitHub Pages 的 Jekyll 處理，讓靜態站原樣發布
- `README.md`：部署與使用說明（這份文件）

## 限制

GitHub Pages 為靜態網站託管。帳號登入、跨裝置即時同步、AI 每週自動新增文章和個人化批改，需要額外串接身分驗證、資料庫與後端服務，不能只靠 GitHub Pages 完成。
