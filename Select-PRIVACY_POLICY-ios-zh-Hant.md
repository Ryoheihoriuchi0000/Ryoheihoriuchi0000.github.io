# 隱私權政策 (iOS)

**最後更新日期：** 2026年10月23日

SELECT（以下簡稱「本 App」）尊重使用者隱私。本政策說明本 App iOS 版會收集哪些資訊以及如何使用。

---

## 1. 我們收集的資訊

以下資訊**僅儲存在您的裝置上**，絕不會傳送至本 App 開發者所擁有的任何伺服器。

- 登錄到各標籤頁的 App（顯示名稱、Bundle ID、圖示 URL、自訂 URL scheme）
- 自訂項目的設定（標籤、圖示、捷徑 URL、網站 URL）
- 顯示偏好（標籤頁圖示／文字樣式、小工具顏色、「享受」標籤頁的顯示狀態）
- 分類與模式的排列順序
- 語言偏好
- 是否已安裝 SELECT Widgets 捷徑

資料儲存在 iOS 的 **SwiftData**（本機儲存空間）與 **App Group** 容器（`group.com.artemis.select.ios`）中。使用 App Group 是為了讓主 App 與小工具延伸功能共用同一份資料。

---

## 2. App 搜尋 (iTunes Search API)

當您點一下「加入項目」來登錄 App 時，本 App 會呼叫 Apple 公開的 **iTunes Search API**（`https://itunes.apple.com/search`）。

- 傳送：**僅您輸入的搜尋字詞**（例如「LINE」）
- 接收：App 名稱、Bundle ID、圖示 URL、App Store URL 等
- 搜尋字詞絕不會儲存在本 App 開發者的伺服器上（本 App 沒有自己的伺服器）
- Apple 對該 API 呼叫的記錄受 Apple 自身的隱私權政策規範

您登錄的 App 會儲存到本機 SwiftData 儲存空間，並顯示在小工具上。

---

## 3. App 圖示快取

登錄 App 時，其圖示會從 Apple 的 CDN 下載，並快取在 App Group 容器中。

- 來源：Apple CDN 端點（例如 `is1-ssl.mzstatic.com`）
- 儲存位置：App Group 容器內的 `Icons/{bundleId}.png`
- 目的：不需網路往返即可即時呈現小工具
- 與第三方分享：絕不

---

## 4. iCloud 同步

您的資料儲存在您本人的 CloudKit 私人資料庫（Apple ID 名下的私人區域）中。這適用於所有使用者。
開發者及任何第三方皆無法存取您的 CloudKit 資料。

---

## 5. 小工具啟動

點一下小工具中的方塊時，會將目標 App 的 Bundle ID 交給 iOS LaunchServices 來啟動該 App。
不會產生任何網路通訊，除目標 Bundle ID 外不會有任何資訊離開裝置。
此外，選用的「SELECT Widgets」整合功能可讓您啟動自建的捷徑。是否安裝不影響預設的啟動方式。

---

## 6. 網路活動

本 App 僅進行以下有限的網路請求。

- `https://itunes.apple.com/search`：查詢 App 資訊（僅在使用「加入項目」時）
- Apple CDN：下載 App 圖示圖片
- Apple CloudKit：iCloud 同步
- Google Firebase Authentication：統計使用人數（見 6-1）
- Google Mobile Ads (AdMob)：在編輯畫面底部顯示的橫幅廣告（見 6-2）

我們**不會**做的事：
- 不向本 App 開發者所擁有的任何伺服器發出請求（我們沒有自己的伺服器）
- 不使用分析 SDK（無 Google Analytics、Firebase Analytics、Crashlytics、Sentry 等）
- 除買斷型「移除廣告」外無 App 內購買（付款由 Apple 處理，開發者不會收到信用卡等付款資訊）
- 除 Firebase Authentication 與 Google Mobile Ads 外不使用第三方 SDK（其餘皆為 Apple 框架：CloudKit / WidgetKit / 捷徑）

### 6-1. 統計使用人數 (Firebase Authentication)

為了大致了解有多少人在使用本 App，本 App 使用 Google **Firebase Authentication** 的**匿名驗證**。

- 首次啟動時，會核發一個稱為**匿名 ID** 的隨機字串。
- 此 ID **絕不會與您的電子郵件地址、姓名、電話號碼或任何其他個人資訊連結**。沒有登入畫面，也不需要註冊帳號。
- 開發者只能看到**彙總數字**：每日活躍使用者數、每月活躍使用者數，以及已核發的 ID 總數。無法識別或追蹤個別使用者。
- **不會傳輸任何行為記錄**——既不包括您使用了哪些功能，也不包括您登錄了哪些 App。
- 匿名 ID 依裝置核發，重新安裝本 App 會產生不同的 ID。不會在裝置之間將您連結為同一人。
- 資料處理遵循 [Google 隱私權政策](https://policies.google.com/privacy)。
- 即使沒有網路連線，本 App 的所有功能也能繼續使用。

### 6-2. 廣告 (Google Mobile Ads)

本 App 會在編輯畫面底部顯示橫幅廣告，廣告由 Google 的 **Google Mobile Ads SDK (AdMob)** 提供。

- 僅在編輯畫面底部顯示廣告。小工具、設定畫面與首次啟動時的說明畫面不顯示廣告。
- 為提供廣告、衡量廣告成效及防止詐騙，Google 會處理裝置資訊（IP 位址、裝置型號、作業系統版本、廣告曝光與點按記錄等）。
- 僅在您選擇「允許追蹤」時才會使用廣告識別碼 (IDFA)。即使不允許，所有功能也能照常使用。您可以隨時在 **iOS 設定 → 隱私權與安全性 → 追蹤** 中變更。
- 在本 App 收費期間取得本 App 的使用者，以及購買了「移除廣告」的使用者，不會看到廣告。
- 資料處理遵循 [Google 如何使用採用其服務的網站或應用程式中的資訊](https://policies.google.com/technologies/partner-sites) 與 [Google 隱私權政策](https://policies.google.com/privacy)。

---

## 7. 向第三方揭露

本 App 不會與第三方分享收集到的資訊。向 Apple 發出的網路請求（iTunes Search API、CloudKit）受 Apple 自身的隱私權政策規範。
Firebase Authentication 核發的匿名 ID 僅由 Google 用於統計使用者數，絕不會提供給任何第三方。為提供廣告，Google 會處理 6-2 中所述的資訊。

---

## 8. 兒童個人資訊

本 App 不會在知情的情況下收集 13 歲以下兒童的個人資訊。

---

## 9. 權限與功能

本 App 使用以下 iOS 功能。

- `LSApplicationQueriesSchemes`：用於在裝置上進行 `canOpenURL` 檢查的 URL scheme 清單（不涉及網路通訊）
- `App Group`（`group.com.artemis.select.ios`）：主 App 與小工具延伸功能之間的共用資料儲存空間
- `WidgetKit`：呈現主畫面小工具
- `AppIntents`：定義小工具內的按鈕動作
- `CloudKit`：iCloud 同步
- `App Tracking Transparency`：要求追蹤許可，僅用於讓廣告更符合您的興趣（不允許也不會限制任何功能）

本 App **絕不會要求**以下權限：
- 相機、麥克風、位置、聯絡人、照片、藍牙、區域網路、通知

---

## 10. 費用

本 App 的所有功能皆免費。本 App 的營運費用由編輯畫面底部顯示的橫幅廣告支持（見 6-2）。唯一的 App 內購買項目是買斷型「移除廣告」，購買後將不再顯示廣告。沒有訂閱。

---

## 11. 刪除您的資料

您可以在設定畫面中將所有設定還原為預設值。如需完全解除安裝，請前往 **iOS 設定 → 一般 → iPhone 儲存空間 → SELECT → 刪除 App**。

若已啟用 iCloud 同步，還可以在 **設定 → [您的姓名] → iCloud → 管理儲存空間 → SELECT → 刪除資料** 中移除雲端副本。

刪除本 App 後，匿名 ID（見 6-1）也會從您的裝置上消失，且該 ID 不會再被使用。由於 ID 本身不含任何可識別個人的資訊，無法從任何殘留記錄追溯到個人。

---

## 12. 本政策的變更

本政策可能在未事先通知的情況下更新。重大變更將在 App 內或商店頁面公告。

---

## 13. 聯絡方式

如對本政策有任何疑問，請透過 App Store 上列出的開發者聯絡方式與我們聯繫。

---

日本語版: [プライバシーポリシー (iOS版)](./Select-PRIVACY_POLICY-ios) ・ English: [Privacy Policy (iOS)](./Select-PRIVACY_POLICY-ios-en)
