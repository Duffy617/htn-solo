# Dietetics Isles（單人版）

學生打開網址就能在 3D 島上探索講義重點，不需要帳號，也不需要任何資料庫。

- 每棟建築讀到最底並停留 20 秒，得到一顆星。星星存在學生自己的瀏覽器裡，換電腦或清除瀏覽資料會歸零。
- 不連網也能用：解壓後雙擊 `index.html` 就能開。

## 放上 GitHub Pages

1. 登入 github.com → 右上「＋」→ New repository → 名稱例如 `dietetics-isles`，選 **Public** → Create。
2. 在 repository 頁面點「uploading an existing file」，把本資料夾**裡面的所有東西**拖進去（`index.html`、`vendor`、`data` 兩個資料夾、`.nojekyll`）→ Commit changes。
   - `.nojekyll` 是隱藏檔；Mac 的 Finder 按 Cmd＋Shift＋. 才看得到。
3. Settings → Pages → Branch 選 `main`、`/ (root)` → Save。
4. 一兩分鐘後網址會是 `https://你的帳號.github.io/dietetics-isles/`，把它給學生。

## 修改內容或新增島嶼

島上所有內容都在 `data/seed.js`。要改重點或新增島嶼，把講義交給 Claude 產生新的 `seed.js`，再到 GitHub repository 的 `data` 資料夾上傳覆蓋即可（學生重新整理頁面就會看到）。

## 檔案

```
index.html              島嶼本體
data/seed.js            島嶼內容（高血壓島）
data/hypertension.json  同一份內容的 JSON 版本（備份用）
vendor/                 three.js r128（MIT 授權）
.nojekyll
```
