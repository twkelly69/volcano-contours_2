# Volcano Contours

A minimal static site ready for GitHub Pages. Use it to showcase volcano contour maps, notebooks, or project documentation.

## 互動台灣地圖（CSV 數據）

- 更新 `assets/taiwan-data.csv` 內的縣市名稱與數值，網頁會在載入時解析並顯示於地圖區塊。
- 將滑鼠或鍵盤焦點移到任何縣市圖磚，該區塊會放大，右側資訊卡同時顯示縣市名稱與對應數值。
- 圖磚採用六欄網格排列成台灣輪廓，適合展示人口、指標或評分等資料。
- 若部署時遇到檔案衝突或 CSV 遺失，頁面會退回內建的預設數據，確保互動區塊仍可瀏覽。

## GitHub Pages deployment

1. 開啟 repository 的 **Settings → Pages** 並將 **Source** 設為 **GitHub Actions**。
2. 推送提交到 `work` 分支。內附的 workflow `.github/workflows/pages.yml` 會建置並發布版本庫內容。
3. 在 Actions 分頁觀看 **Deploy GitHub Pages** workflow。公開網址會顯示於部署摘要與 Pages 設定頁。

### Customizing the site

- 編輯 `index.html` 可調整段落或新增區塊。
- 更新 `assets/style.css` 可修改版面、色彩或排版。
- 若要從其他分支或資料夾發布，請修改 `.github/workflows/pages.yml` 內的 `on.push.branches` 與 `upload-pages-artifact` 的 `path`。

## Local preview

因為網站是純靜態的，可直接在瀏覽器開啟 `index.html`。若想啟動本機伺服器，可執行：

```bash
python -m http.server 8000
```

接著瀏覽 <http://localhost:8000>。
