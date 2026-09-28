# Biology Spelling Challenge

生物科英文串字挑戰（靜態網頁，經 GitHub Pages 發佈）。

🔗 網址：https://ksl-blip.github.io/biology-spelling-challenge/

## 設定成績上傳（Google Sheet + Apps Script）

1. 開啟成績試算表 > **擴充功能 > Apps Script**，貼上 `Code.gs` 的程式碼並儲存。
2. 執行一次 `testAppend` 以完成授權。
3. **部署 > 新增部署作業 > 網頁應用程式**：執行身分「我」，存取權「所有人」，複製以 `/exec` 結尾的 URL。
4. 設定 URL（任選其一）：
   - **全部學生通用（建議）**：編輯 `index.html`，把
     `const DEFAULT_SCRIPT_URL = 'PASTE_APPS_SCRIPT_URL_HERE';`
     中的 `PASTE_APPS_SCRIPT_URL_HERE` 換成你的 URL，commit 後 GitHub Pages 會自動更新（約 1–2 分鐘）。
   - **只限某部裝置**：在遊戲右上角 ⚙️ 貼上 URL 並按 Save（存於該瀏覽器的 localStorage，會優先於預設值）。

學生達到 100 分時，成績（時間、姓名、班別、學號、分數、作答字數、百分比、最高連勝）會自動寫入試算表。
