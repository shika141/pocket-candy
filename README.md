# 《今日一顆糖》05－替換九種糖果抽取插畫

曾巟糖の非科學糖果占卜，完整靜態網站原始碼。

## 05 修改內容

- 將抽取揭曉畫面的糖果 Emoji 主圖替換為九張專屬 Q 版糖糖插畫。
- 糖紙揭曉動畫同步顯示抽中的對應插畫。
- 九種糖果皆有獨立圖片，不會出現錯誤配對。
- 保留小型 Emoji 作為分類標示與糖紙冊圖示。
- 將原始透明 PNG 最佳化為高品質透明 WebP，提升手機載入速度。
- 保留 04 版糖果背景、全部糖籤、糖紙冊、手機搖一搖與特殊彩蛋。

## 圖片對應

```text
草莓糖   → dist/assets/candy/strawberry.webp
檸檬糖   → dist/assets/candy/lemon.webp
葡萄糖   → dist/assets/candy/grape.webp
牛奶糖   → dist/assets/candy/milk.webp
水蜜桃糖 → dist/assets/candy/peach.webp
薄荷糖   → dist/assets/candy/mint.webp
焦糖     → dist/assets/candy/caramel.webp
巧克力糖 → dist/assets/candy/chocolate.webp
棒棒糖   → dist/assets/candy/lollipop.webp
```

## 專案結構

```text
05-替換九種糖果抽取插畫-今日一顆糖完整原始碼/
├── dist/
│   ├── index.html
│   └── assets/
│       ├── candy-background.jpeg
│       └── candy/
│           ├── strawberry.webp
│           ├── lemon.webp
│           ├── grape.webp
│           ├── milk.webp
│           ├── peach.webp
│           ├── mint.webp
│           ├── caramel.webp
│           ├── chocolate.webp
│           └── lollipop.webp
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

