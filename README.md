# 壽司傳送門 (3D Stencil Portal)

透過 Three.js 與 WebGL 模版緩衝區（Stencil Buffer）技術實現的 3D 壽司傳送門互動卡片展示專案。支援 Progressive Web App (PWA)，可在 Android / iOS 等行動裝置瀏覽器中直接安裝至主畫面作為獨立 App 運行。

## 🌟 特色功能

- **📱 支援 Android / iOS 行動裝置 App 安裝 (PWA)**：
  - 具備 Web App Manifest (`manifest.json`) 與專屬壽司 App 圖示（含 192x192、512x512、Maskable 安全邊距與高清規格）。
  - 整合 Service Worker 支援離線快取與加速載入。
  - 在 Android Chrome / Edge 等瀏覽器中，右上角選單會顯示「安裝至手機主畫面」按鈕，亦可透過瀏覽器選單「安裝應用程式」一鍵安裝為獨立全螢幕 App。
- **3D 傳送門視效（Stencil Buffer）**：卡片框內呈現獨立的 3D 壽司空間，透過模版緩衝技術實現穿透式立體視覺。
- **雙重視角模式**：
  - **模式 A（外環）**：攝影機由外向內環視卡片。
  - **模式 B（內環）**：攝影機置身於卡片環內，帶來沉浸式全景體驗（預設）。
- **體感傾斜支援（Device Tilt / Gyroscope）**：支援行動裝置陀螺儀體感控制，隨手機傾斜動態旋轉視角。
- **自訂參數控制**：
  - 可動態調整卡片數量（10 ~ 25 張）。
  - 可調整卡片間距（緊湊至寬鬆）。
  - 自動於瀏覽器 LocalStorage 記憶個人化設定。
- **動態天空與星空背景**：
  - 四時段三色漸層天色（清晨、早上、黃昏、夜晚），可設為隨時間自動切換或手動指定。
  - 固定隨機種子（Random 42）星點畫布。
- **零依賴建置**：單一靜態專案架構，完全不需要 npm 或打包流程，輕鬆部署至 GitHub Pages。

## 📱 手機安裝 App 說明 (Android)

1. 使用 Android 手機上的 **Chrome** 或 **Edge** 瀏覽器開啟網頁。
2. 點擊右上角漢堡選單，點選頂部「**安裝至手機主畫面**」按鈕（或點擊瀏覽器右上角三個點選單 ➜ 選擇「**安裝應用程式**」或「**新增至主畫面**」）。
3. 確認安裝後，手機桌面即會產生專屬壽司圖示的 App，開啟時將以全螢幕原生體驗獨立運作！

## 🚀 快速開始

### 本地瀏覽

直接使用任何靜態網頁伺服器開啟本專案，例如：

使用 Python：
```bash
python3 -m http.server 8000
```
或使用 Node.js `serve` / `npx http-server`：
```bash
npx serve .
```

開啟瀏覽器前往 `http://localhost:8000` 即可體驗。

## 📂 檔案結構

```
.
├── index.html            # 最新主要入口檔案（壽司傳送門 + PWA 支援）
├── manifest.json         # PWA Web App Manifest 設定
├── sw.js                 # PWA Service Worker (離線快取與安裝支援)
├── favicon.ico           # 網站圖示
├── icons/                # App 圖示資源包
│   ├── app-icon.jpeg     # 原始高畫質 App 圖示
│   ├── icon-192.png      # PWA 192x192 標準圖示
│   ├── icon-512.png      # PWA 512x512 高清圖示
│   ├── icon-1024.png     # PWA 1024x1024 超高清圖示
│   ├── icon-maskable-192.png # 自適應遮罩圖示 (192px)
│   ├── icon-maskable-512.png # 自適應遮罩圖示 (512px)
│   ├── apple-touch-icon.png  # iOS 主畫面圖示 (180px)
│   └── favicon-32.png    # 32x32 圖示
└── README.md             # 專案說明文件
```

## 🛠️ 技術棧

- **PWA (Progressive Web App)**：Web App Manifest, Service Worker
- **WebGL / Three.js**
- **HTML5 Canvas / CSS3**
- **JavaScript (ES6+)**
- **DeviceOrientation API**
