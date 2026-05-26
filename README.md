# BTC 訊號監控 PWA

## 功能說明
- 15M / 30M / 1H / 4H / 1D 五個週期即時訊號
- MACD 金叉/死叉偵測
- RSI 超買超賣反轉偵測
- TD 序列 9轉/13轉偵測
- K棒收線倒數計時與推播通知
- 多週期共振分析與進出場建議

---

## iOS 安裝步驟（必須用 Safari）

1. 將整個資料夾部署到任一靜態網頁主機（見下方部署方式）
2. 用 **Safari** 開啟網址
3. 點選底部 **分享按鈕**（方框加箭頭圖示）
4. 選擇「**加入主畫面**」
5. 確認名稱後點「**新增**」

安裝完成後即可從主畫面直接開啟，外觀與原生 App 相同。

---

## 部署方式

### 方法一：GitHub Pages（免費，推薦）
1. 建立 GitHub 帳號（免費）
2. 建立新 Repository，名稱如 `btc-signal`
3. 上傳所有檔案（index.html, manifest.json, sw.js, icons/）
4. 至 Settings → Pages → Source 選 main branch
5. 網址為 `https://你的帳號.github.io/btc-signal/`

### 方法二：Netlify Drop（最快，拖放即用）
1. 開啟 https://app.netlify.com/drop
2. 將整個 `btc-alert-pwa` 資料夾拖入頁面
3. 自動取得 HTTPS 網址，可直接在 iOS Safari 開啟安裝

### 方法三：Vercel（需 CLI）
```bash
npm i -g vercel
cd btc-alert-pwa
vercel --prod
```

---

## 注意事項

- **必須使用 HTTPS** 網址才能安裝 PWA 並啟用通知
- iOS 16.4+ 支援 PWA 推播通知（需在 Safari 允許）
- 行情資料來源：Binance 公開 API（無需 API Key）
- 本工具僅供學習參考，不構成投資建議

---

## 檔案結構
```
btc-alert-pwa/
├── index.html      主程式
├── manifest.json   PWA 設定
├── sw.js           Service Worker（離線快取 + 通知）
├── icons/          各尺寸圖示
│   ├── icon-72.png
│   ├── icon-96.png
│   ├── icon-128.png
│   ├── icon-144.png
│   ├── icon-152.png
│   ├── icon-167.png
│   ├── icon-180.png
│   ├── icon-192.png
│   └── icon-512.png
└── README.md       安裝說明
```
