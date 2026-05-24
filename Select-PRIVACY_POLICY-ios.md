# プライバシーポリシー (iOS版)

**最終更新日**: 2026年5月24日

SELECT (以下「本アプリ」) は、ユーザーのプライバシーを尊重します。本ポリシーは、本アプリの iOS 版が収集・利用する情報について説明します。

---

## 1. 収集する情報

本アプリは以下の情報を **端末内のみ** で保持し、本アプリ自身が外部サーバーへ送信することはありません。

- ユーザーが各タブに登録したアプリの一覧 (アプリ名、bundle ID、アイコン URL、URL Scheme)
- カスタムアイテムの設定 (ラベル、アイコン、ショートカット URL、Web サイト URL)
- 表示設定 (タブのアイコン/テキスト表示、ウィジェット色、Enjoy タブの表示/非表示)
- カテゴリ・モードの並び順
- 言語設定
- Pro 機能の購入状態
- SELECT Widgets ショートカットのインストール完了フラグ

これらは iOS の **SwiftData** (端末ローカルストレージ) と **App Group** コンテナ (`group.com.artemis.select.ios`) に保存されます。App Group はメインアプリとウィジェット拡張が同一データを参照するために使われます。

---

## 2. アプリ検索 (iTunes Search API)

ユーザーが「アイテム追加」からアプリを登録する際、Apple が公開している **iTunes Search API** (`https://itunes.apple.com/search`) を呼び出します。

- 送信内容: **ユーザーが入力した検索語のみ** (例: 「PayPay」)
- 受信内容: アプリ名、bundle ID、アイコン URL、App Store URL 等
- 検索クエリは本アプリのサーバーには一切保存されません (本アプリは独自サーバーを持っていません)
- Apple 側のログは Apple のプライバシーポリシーに準じます

検索結果から登録されたアプリ情報は、端末内の SwiftData に保存され、ウィジェットで表示するために使用されます。

---

## 3. アプリアイコンのキャッシュ

アプリを登録すると、Apple の CDN からそのアプリのアイコン画像をダウンロードし、端末内の **App Group コンテナ内** にキャッシュします。

- ダウンロード先: Apple の CDN (`is1-ssl.mzstatic.com` など、Apple 公開エンドポイント)
- 保存場所: 端末内 `Icons/{bundleId}.png`
- 用途: ウィジェット表示時の高速描画 (ネットワーク不要)
- 第三者への送信: なし

---

## 4. iCloud 同期

データは CloudKit Private Database (Apple ID 配下のプライベート領域) に保存・同期されます。Pro 版の有無に関わらず、全てのユーザーが iCloud 同期の対象です。
本アプリの開発者を含む第三者は、ユーザーの CloudKit データに一切アクセスできません。

---

## 5. ウィジェット起動 (Shortcuts.app 連携)

ウィジェットのタイルをタップすると、対象アプリの bundle identifier を iOS の LaunchServices に渡してアプリを起動します。
ネットワーク通信は発生せず、起動先の bundle identifier 以外の情報は外部へ送信されません。
任意機能として、ユーザー自作の Shortcuts を起動できるよう「SELECT Widgets」という名前のショートカット連携も提供しています。これを利用しない通常の起動経路には影響しません。
---

## 6. ネットワーク通信

本アプリは以下の限定された通信のみを行います。

- `https://itunes.apple.com/search`: アプリ検索 (ユーザーが「アイテム追加」ボタンを押した時のみ)
- Apple CDN: アプリアイコン画像のダウンロード
- Apple CloudKit: Pro 版の iCloud 同期 (有効時のみ)
- Apple StoreKit: Pro 版購入時の課金処理

それ以外:
- 本アプリ開発者のサーバーへの送信: **一切なし** (独自サーバー無し)
- 解析ツール (Firebase Analytics、Crashlytics、Sentry 等): **なし**
- 広告ネットワーク: **なし**
- 第三者の SDK: **なし** (Apple 純正の StoreKit / CloudKit / WidgetKit / Shortcuts のみ)

---

## 7. 第三者への提供

本アプリは収集した情報を第三者に提供しません。Apple との通信 (iTunes Search API、CloudKit、StoreKit) は Apple のプライバシーポリシーに準じて処理されます。

---

## 8. 子どもの個人情報

本アプリは 13 歳未満の子どもから故意に個人情報を収集することはありません。

---

## 9. 権限と機能

本アプリは以下の iOS 機能を使用します。

- `LSApplicationQueriesSchemes`: 端末内の `canOpenURL` 判定用に URL Scheme 一覧を登録 (実際の通信は行わない)
- `App Group` (`group.com.artemis.select.ios`): メインアプリとウィジェット拡張間のデータ共有
- `WidgetKit`: ホーム画面ウィジェットの提供
- `AppIntents`: ウィジェット内ボタンの動作定義
- `CloudKit`: Pro 版の iCloud 同期 (有効時のみ)
- `StoreKit`: Pro 版購入処理

以下の権限は **一切要求しません**:
- カメラ、マイク、位置情報、連絡先、写真、Bluetooth、ローカルネットワーク、通知

---

## 10. 課金処理

Pro 版の購入は Apple の **App Store / StoreKit** を経由します。

- 課金主体: Apple Inc.
- 支払い方法: Apple ID に登録された支払い方法
- 本アプリは購入結果の検証のみを行い、決済情報 (カード番号等) には一切アクセスしません
- 領収書やお問い合わせは App Store 経由でご対応ください

---

## 11. データの削除

設定画面から「すべてデフォルトに戻す」ですべての設定を初期化できます。完全削除する場合は、iOS の **設定 → 一般 → iPhone ストレージ → SELECT → App を削除** を実行してください。

iCloud 同期を有効にしている場合は、上記に加えて **設定 → ユーザー名 → iCloud → ストレージを管理 → SELECT → データを削除** で iCloud 側のデータも削除できます。

---

## 12. ポリシーの変更

本ポリシーの内容は予告なく変更される場合があります。重要な変更がある場合は、アプリ内の通知またはストアページで告知します。

---

## 13. お問い合わせ

本ポリシーに関するご質問は、App Store の開発者連絡先までご連絡ください。

---

English version: [Privacy Policy (iOS)](./Select-PRIVACY_POLICY-ios-en)
