# 《今日一顆糖》v14

此版本專門修正 GitHub 連接 Cloudflare Pages 時，線上網站仍讀取舊 `dist` 資料夾，造成新糖罐圖片與字體沒有生效的問題。

## 已修正

- 根目錄 `index.html` 與 `dist/index.html` 已同步為同一份最新版。
- 根目錄 `assets` 與 `dist/assets` 均包含完整素材。
- 圖二糖罐位於兩邊的 `assets/candy-jar-v13.png`。
- Fredoka、芫荽、jf open 粉圓與小賴字體設定已同步進兩份 `index.html`。
- 新增 Cloudflare Pages `_headers`，避免 `index.html` 長期沿用舊快取。

## 上傳到 GitHub

請解壓縮 ZIP，將資料夾裡的所有檔案與資料夾上傳到 GitHub 專案最外層，遇到同名檔案時選擇覆蓋。

Cloudflare Pages 的「建置輸出目錄」無論目前填寫 `dist` 或留空，都會讀到相同的最新版。
