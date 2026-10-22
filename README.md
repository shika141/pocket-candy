# 《今日一顆糖》04－更換糖果插畫背景

曾巟糖の非科學糖果占卜，完整靜態網站原始碼。

## 04 修改內容

- 將使用者提供的直式糖果插畫設為全站背景。
- 加入淡白色背景遮罩，維持文字與操作按鈕的可讀性。
- 手機版保留直式插畫構圖，避免固定背景造成 Safari 顯示問題。
- 巧克力糖模式沿用同一張插畫，改以深色濾鏡呈現。
- 保留原有版面、90 張糖籤、動畫、糖紙冊及手機搖一搖功能。

## 專案結構

```text
04-更換糖果插畫背景-今日一顆糖完整原始碼/
├── dist/
│   ├── index.html
│   └── assets/
│       └── candy-background.jpeg
├── package.json
├── CHANGELOG.md
├── .gitignore
└── README.md
```

## 本機預覽

安裝 Node.js 後，在專案資料夾執行：

```bash
npm run preview
```

手機搖一搖需要 HTTPS 與使用者主動授權，請在正式部署後測試。

## Cloudflare Pages 部署

1. 將整個專案上傳至 GitHub。
2. 在 Cloudflare Pages 連接儲存庫。
3. Framework preset 選擇 `None`。
4. Build command 留空。
5. Build output directory 填入 `dist`。

Netlify 與 Vercel 同樣將發布目錄設為 `dist` 即可。

## 紀錄保存

每日抽取結果與糖紙冊使用瀏覽器 `localStorage` 保存。同一裝置、同一瀏覽器重新開啟仍會保留；無痕模式、清除網站資料或更換裝置後不會同步。

