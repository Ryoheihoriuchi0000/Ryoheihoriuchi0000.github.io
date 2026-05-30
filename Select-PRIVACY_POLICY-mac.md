# プライバシーポリシー

**最終更新日**: 2026年5月30日
**対象**: SELECT for macOS

SELECT(以下「本アプリ」)は、ユーザーのプライバシーを尊重します。本ポリシーは、本アプリが収集・利用・保存する情報について説明します。

---

## 1. 収集する情報

本アプリは以下の情報を **端末内および ユーザー自身の iCloud アカウント内のみ** で保持します。第三者サーバーには送信しません。

- ユーザーが各カテゴリに登録したアイテムの一覧
  - アプリのバンドル ID / 実行可能ファイルパス
  - URL / ショートカット名 / セキュリティスコープ付きブックマーク (ユーザー選択ファイル / フォルダ)
  - 表示ラベル、カスタムアイコン (SF Symbol 名)
- モード (Profile) ごとの設定
  - 名前、アイコン、各タブの並び順とピン状態
  - メニューバー / フローティングバーのラベル表示スタイル
- アプリ全体の設定
  - 言語 (`ja` / `en`)、iTunes Search の国コード (`jp` / `us` 等)
  - グローバルホットキー文字列、Dock アイコン表示、ログイン時起動の有無
  - フローティングバーの位置 / 常時最前面ピン状態

これらは Apple の **SwiftData** (端末内 SQLite ストア) と **CloudKit private database** に保存されます。

## 2. 端末上のアプリ情報

本アプリはランチャー機能のため、macOS の **Launch Services** および **`NSWorkspace`** API を通じてインストール済みアプリのバンドル ID、表示名、アイコンを参照します。

- アプリ一覧表示および起動のために必要最小限の情報のみ参照します
- 参照したアプリ情報を外部サーバーへ送信することはありません
- アプリの起動は標準 API (`NSWorkspace.openApplication(at:configuration:)` / `LSApplicationWorkspace`) のみを使用し、他アプリの内部状態にはアクセスしません

## 3. ファイル / フォルダへのアクセス

`path` 種別のアイテム (ユーザーが選択したファイル / フォルダ) を扱う際、macOS の **App Sandbox** が要求するセキュリティスコープ付きブックマーク (`URL.bookmarkData(options: .withSecurityScope, ...)`) を生成して保存します。

- ブックマークデータは本アプリの sandbox container 内および iCloud 同期データ内にのみ保管されます
- ブックマークが指すファイル / フォルダの **内容** は読み取りません(起動 / Finder で開く目的のみ)

## 4. ネットワーク通信

本アプリが行うネットワーク通信は以下のみです。

| 通信先 | 目的 | 個人情報送信 |
|---|---|---|
| **iTunes Search API** (`itunes.apple.com`) | App Store 公開アプリのアイコン画像取得 | なし(検索クエリは公開バンドル ID のみ) |
| **Apple CloudKit** (`*.icloud.com`) | private database への設定 / アイテム同期 | Apple ID 紐づきの暗号化通信、Apple のプライバシーポリシーが適用 |

- 解析ツール(Firebase Analytics、Crashlytics、Sentry 等)は **使用していません**
- 広告ネットワークは **一切ありません**
- 上記以外の任意の外部サーバーとは通信しません

## 5. iCloud 同期について

本アプリは Apple の **CloudKit private database** を使用して複数 Mac 間で設定とアイテムを自動同期します。

- 同期対象データは **ユーザー自身の iCloud アカウント内のみ** に保存されます。開発者および第三者はアクセスできません
- 同期データの暗号化、保存、アクセス制御はすべて Apple が管理し、Apple のプライバシーポリシーが適用されます
- iCloud にサインインしていない場合、本アプリは端末ローカルのみで動作します
- ユーザーは Apple ID の管理画面から、本アプリの iCloud データをいつでも削除できます

## 6. 第三者への提供

本アプリは収集した情報を第三者に提供しません。

## 7. 子どもの個人情報

本アプリは13歳未満の子どもから故意に個人情報を収集することはありません。

## 8. 権限 / Entitlements

本アプリは以下の macOS entitlement を使用します。

- `com.apple.security.app-sandbox`: App Store 配信に必須のサンドボックス制限
- `com.apple.security.files.user-selected.read-write`: `NSOpenPanel` でユーザーが選択したファイル / フォルダの読み書き
- `com.apple.security.files.bookmarks.app-scope`: セキュリティスコープ付きブックマークの解決
- `com.apple.security.network.client`: iTunes Search API および CloudKit との通信
- `com.apple.developer.icloud-services` (CloudKit): private database での設定同期
- `com.apple.developer.icloud-container-identifiers`: 専用 iCloud コンテナの利用

これら以外の権限(連絡先、位置情報、カメラ、マイク、自動化、フルディスクアクセス等)は **一切要求しません**。

## 9. データの削除

- アプリ内: 各アイテム / モードを編集モードから削除できます
- 端末ローカル: **Finder → 移動 → ライブラリへ移動 → Containers → `com.artemis.select.mac` フォルダを削除** で本アプリのすべてのローカルデータを削除できます
- iCloud: **システム設定 → Apple ID → iCloud → iCloud で同期するアプリを管理 → SELECT** から iCloud 上のデータを削除できます
- 本アプリ自体: **Finder → アプリケーション → SELECT.app をゴミ箱へ** で完全に削除できます

## 10. ランチャー機能について

本アプリは macOS の **メニューバー常駐型ランチャー** として動作します。

- 個人を識別する情報は収集しません
- メニューバー / フローティングバー上のすべての操作は端末内で完結します
- グローバルホットキー (例: `cmd+shift+0`) は Carbon Hot Key Manager 経由で OS に登録され、本アプリのフローティングバー表示切替にのみ使用されます。キー入力内容を記録 / 送信することはありません

## 11. ポリシーの変更

本ポリシーの内容は予告なく変更される場合があります。重要な変更がある場合は、アプリ内またはストアページで告知します。

## 12. お問い合わせ

本ポリシーに関するご質問は、Mac App Store の開発者連絡先までご連絡ください。

---

*このポリシーは Privacy Policy in Japanese です。English version available upon request.*
