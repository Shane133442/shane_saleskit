# SHANE 產品體驗架構計畫｜專案紀錄

> 版本紀錄日期：2026-08-07  
> GitHub 儲存庫：[Shane133442/shane_saleskit](https://github.com/Shane133442/shane_saleskit)  
> 設計參考來源：`C:\Users\User\Desktop\saleskit\01.png` ～ `06.png`

## 1. 專案概覽

本專案是一個以 Bootstrap 5 製作的單頁式廣告銷售頁，品牌名稱為 **SHANE**。頁面以深色太空、月相與軌道為主要視覺語言，服務內容聚焦於 SaaS、AI 產品、新創團隊及獨立創作者的產品體驗架構規劃。

目前版本已依 6 張 UI/UX 設計圖完成響應式切版，包含導覽、銷售文案、問題分析、品牌方法、服務特色、實作案例及預約診斷表單。

## 2. 專案結構

```text
website/
├─ index.html
├─ PROJECT.md
└─ img/
   ├─ moon-hero.png
   ├─ moon-hero01.png
   ├─ plan.png
   ├─ project.png
   ├─ rem.png
   └─ shape.png
```

專案沒有 Node.js、套件管理或建置設定，所有頁面結構、客製 CSS 與少量 JavaScript 均集中在 `index.html`。

## 3. 使用技術

- HTML5，頁面語言設定為 `zh-Hant`。
- Bootstrap `5.0.2` CSS 與 Bundle JavaScript。
- Bootstrap JavaScript Bundle 已包含 Popper。
- Google Fonts：`Noto Sans TC` 與 `Noto Serif TC`。
- 原生 CSS：自訂色彩、字級、月球軌道、卡片、素材裁切與響應式版面。
- 原生 JavaScript：點擊行動版導覽項目後，自動收合 Bootstrap 選單。

外部 CSS、字型及 Bootstrap JavaScript 均透過 CDN 載入，因此完整呈現需要網路連線。

## 4. 視覺系統

### 色彩與質感

- 主背景：接近黑色的 `#070809`。
- 主要文字：灰白色 `#f1f0ed`。
- 次要文字：灰色 `#9a9a9a`。
- 邊框：低透明度白色線條。
- 使用徑向漸層、SVG noise、半透明面板與軌道線條建立深色太空質感。

### 字體

- 一般文字與介面：`Noto Sans TC`。
- 大標題與敘事文字：`Noto Serif TC`。
- 英文案例名稱部分使用 Georgia 作為襯線字體備援。

### 響應式斷點

除 Bootstrap 網格外，自訂 CSS 也針對以下寬度調整：

- `1199.98px` 以下：導覽列收合、部分視覺與面板縮小。
- `991.98px` 以下：雙欄改為上下排列、表單與服務利益區重新排列。
- `767.98px` 以下：手機字級、間距、CTA、卡片及圖片裁切重新設定。

## 5. 頁面區塊

### 5.1 首屏 Hero｜`#top`

- 顯示產品體驗架構計畫定位、主要銷售標題與介紹文案。
- 提供「預約 30 分鐘免費產品體驗診斷」CTA。
- 顯示每日限量資訊與 SaaS、AI 產品、新創團隊、獨立創作者標籤。
- 右側使用 `img/moon-hero01.png` 作為完整月球素材。
- 月球外層以 CSS 建立軌道、節點及 SHANE DESIGN 品牌文字。

### 5.2 產品失控問題｜`#problem`

- 左側使用 `img/rem.png` 裁切出產品流程與功能關係圖。
- 右側以 PAS 結構呈現：
  1. Problem
  2. Agitation
  3. Solution

### 5.3 品牌信念｜`#belief`

- 使用 Golden Circle 概念說明 WHY、HOW、WHAT。
- 左側使用 `img/shape.png` 呈現月相與黃金圈視覺。
- 右側以三張卡片說明信念、月相方法與交付成果。

### 5.4 雙焦核心與旗艦計畫｜`#focus`

- 說明「情境式變焦設計」的三層介面：
  1. 賞月：感受與快速完成。
  2. 望遠：理解與掌控細節。
  3. 登月：創造與留下足跡。
- 三個介面示意圖由 `img/plan.png` 進行背景定位與裁切。
- 導覽列中的「雙焦核心」與「旗艦計畫」目前都連至此區塊。

### 5.5 實踐者實證｜`#proof`

- 使用 `img/project.png` 裁切呈現三個自有產品案例：
  - Block Vibe
  - Scent Loop
  - 之間郵局
- 右側說明服務邊界，包括不提供大量高保真美化、不承接程式開發，以及交付可供 UI 與開發團隊使用的前期藍圖。

### 5.6 預約診斷｜`#booking`

- 顯示三項預約利益：
  - 30 分鐘免費診斷。
  - 顧問親自回覆。
  - 絕不強迫推銷。
- 表單包含公司或專案名稱、產品類型及目前問題三個必填欄位。
- 提交按鈕與說明文字已完成 UI。

## 6. 導覽列

導覽列使用 Bootstrap `navbar` 與 `collapse` 元件，固定於頁面頂部並帶有半透明模糊背景。

目前導覽項目：

- 品牌信念
- 產品失控嗎？
- 雙焦核心
- 旗艦計畫
- 實踐者實證
- 預約診斷

所有導覽錨點均已對應現有頁面區塊。行動版點擊連結後會自動收合選單。

## 7. 圖片資源

| 檔案 | 用途 |
|---|---|
| `moon-hero01.png` | 首屏右側目前使用的完整月球，來源為使用者提供的附圖 1 |
| `moon-hero.png` | 前一版月球素材，目前未被頁面引用 |
| `rem.png` | 產品問題區的流程關係視覺 |
| `shape.png` | Golden Circle、背景月球及其他月相裝飾 |
| `plan.png` | 三層級介面示意圖的裁切來源 |
| `project.png` | 三個實作產品案例圖片的裁切來源 |

多張圖片目前以 CSS `background-position` 裁切原始設計圖中的局部區域。若後續取得獨立原始素材，建議替換為各自的圖檔，以改善維護性與不同螢幕比例下的顯示精準度。

## 8. 表單狀態

預約表單目前只有前端介面：

- 使用 HTML `required` 提供基本必填驗證。
- `action` 目前為 `#`。
- 尚未串接 API、資料庫、Email、Google Form 或其他 CRM。
- 尚未實作送出成功、失敗、讀取中與防止重複送出的狀態。

正式上線前必須決定表單資料的接收方式，並補上隱私權告知及必要的防濫用機制。

## 9. 執行方式

可直接以瀏覽器開啟 `index.html`。為避免本機檔案模式限制，建議透過任意靜態檔案伺服器開啟專案。

本專案沒有建置或安裝指令。

## 10. 已完成檢查

- 6 個 `<section>` 開始與結束標籤配對正確。
- 表單標籤配對正確。
- CSS 大括號數量配對正確。
- 頁面沒有重複 ID。
- 導覽錨點均能找到對應 ID。
- 所有 `img/` 圖片引用均存在。
- 已包含 Bootstrap 5 與手機響應式設定。

目前環境缺少自動瀏覽器驗證工具，因此尚未進行自動化桌面與手機截圖比對。

## 11. 建議後續工作

1. 串接預約表單後端或第三方表單服務。
2. 加入送出成功、失敗與處理中狀態。
3. 取得獨立月球、流程圖、介面 mockup 與產品案例素材，取代設計稿裁切。
4. 壓縮大型 PNG，視需求轉換為 WebP 或 AVIF。
5. 在 Chrome、Safari、Edge 與行動裝置進行實際視覺測試。
6. 補上正式聯絡方式、隱私權政策、服務條款與 SEO 分享圖片。

## 13.Github公開網址

- 公開網址：[https://shane133442.github.io/shane_saleskit/](https://shane133442.github.io/shane_saleskit/)
- 目前狀態：部署中，待 GitHub Pages 完成發佈後即可公開瀏覽。
