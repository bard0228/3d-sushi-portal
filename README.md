# 壽司傳送門 (3D Stencil Portal)

透過 Three.js 與 WebGL 模版緩衝區（Stencil Buffer）技術實現的 3D 壽司傳送門互動卡片展示專案。

## 🌟 特色功能

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
- **零依賴建置**：單一 HTML 檔案隨開即用，完全不需要 npm 或打包流程，輕鬆部署至 GitHub Pages。

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
├── index.html                     # 主要入口檔案（壽司傳送門）
├── stencil_portal_cards-v12.html  # 原始版本備份
└── README.md                      # 專案說明文件
```

## 🛠️ 技術棧

- **WebGL / Three.js**
- **HTML5 Canvas / CSS3**
- **JavaScript (ES6+)**
- **DeviceOrientation API**
