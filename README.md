# 台灣天氣 Weather App
<img width="1920" height="917" alt="Weather App - Google Chrome 2026_2_20 上午 11_50_03" src="https://github.com/user-attachments/assets/e128aca4-f279-435c-9d76-c880de63f9f8" />


以中央氣象署開放資料平臺 API 為資料來源的輕量天氣查詢網頁，支援台灣各縣市 36 小時天氣預報。

---

## 功能

- 查詢台灣各縣市天氣預報（36 小時）
- 顯示天氣現象、平均溫度、溫度區間
- 顯示降雨機率與舒適度指數
- 天氣 Emoji 對應氣象署天氣代碼

---

## 使用技術

- HTML / CSS / JavaScript（純前端，無框架）
- [中央氣象署開放資料平臺 API](https://opendata.cwa.gov.tw) `v1.0.0`
  - 資料集：`F-C0032-001`（三十六小時天氣預報）

---

## 檔案結構

```
專案/
├── index.html   # 頁面結構 + JavaScript
└── style.css    # 樣式
```

---

## 使用方式

1. 至 [中央氣象署開放資料平臺](https://opendata.cwa.gov.tw) 申請授權碼
2. 開啟 `index.html`，將授權碼填入：
   ```js
   const API_KEY = 'YOUR_CWA_API_KEY';
   ```
3. 以瀏覽器開啟 `index.html`，選擇縣市後按「查詢」

---

## 支援縣市

台北市、新北市、桃園市、新竹市、台中市、台南市、高雄市、基隆市、宜蘭縣、花蓮縣、臺東縣

---

## 資料說明

| 欄位 | 來源要素 | 說明 |
|------|---------|------|
| 天氣現象 | `Wx` | 例如：多雲時晴 |
| 平均溫度 | `MinT` + `MaxT` | 最低與最高溫的平均值 |
| 溫度區間 | `MinT` / `MaxT` | 當前時段最低／最高溫 |
| 降雨機率 | `PoP` | 單位：% |
| 舒適度 | `CI` | 例如：稍有寒意、舒適 |
