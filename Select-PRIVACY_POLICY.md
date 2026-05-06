# プライバシーポリシー

**最終更新日**: 2026年5月5日

SELECT(以下「本アプリ」)は、ユーザーのプライバシーを尊重します。本ポリシーは、本アプリが収集・利用する情報について説明します。

---

## 1. 収集する情報

本アプリは以下の情報を**端末内のみで**保持し、外部に送信しません。

- ユーザーが各カテゴリに割り当てたアプリの一覧(パッケージ名、表示名)
- カスタムスロットの設定(ラベル、アイコン、ショートカット名)
- 表示設定(時刻・日付・カレンダー・Playカテゴリ・アプリ一覧の表示/非表示)
- カテゴリ・モードの並び順
- カスタムテーマ色、背景色、背景画像のURI
- 言語設定
- Pro 機能の購入状態

これらは Android の DataStore(端末ローカルストレージ)に保存されます。

## 2. 端末上のアプリ情報

本アプリはランチャー機能のため、Android の `PackageManager` API を通じてインストール済みアプリのアイコンとラベルを参照します。

- アプリ一覧表示および起動のために必要最小限の情報のみ参照します
- 参照したアプリ情報を外部送信することはありません
- 本アプリは Google Play の `<queries>` 宣言で許可されたアプリ(`MAIN/LAUNCHER` インテントを宣言しているアプリ)のみを列挙します

## 3. ネットワーク通信

本アプリはインターネット接続を行いません。

- サーバーへのデータ送信なし
- 外部APIの呼び出しなし
- 解析ツール(Firebase Analytics、Crashlytics 等)なし
- 広告ネットワークなし

唯一の例外として、**Google Play 課金処理**(Pro 版購入時)では Google Play Billing Library が Google のサーバーと通信します。これは Google が提供する標準機能であり、本アプリ自身が個人情報を送信するものではありません。

## 4. 第三者への提供

本アプリは収集した情報を第三者に提供しません。

## 5. 子どもの個人情報

本アプリは13歳未満の子どもから故意に個人情報を収集することはありません。

## 6. 権限

本アプリは以下の権限を使用します:

- `com.android.vending.BILLING`: Google Play 課金処理(Pro 版購入時)
- `<queries>` 宣言: ランチャー機能のため、インストール済みアプリの基本情報を参照

これら以外の権限(連絡先、位置情報、カメラ、マイク等)は一切要求しません。

## 7. データの削除

設定画面から「すべてデフォルトに戻す」ですべての設定を初期化できます。完全削除する場合は、端末の **設定 > アプリ > Select > ストレージ > データを消去** を実行してください。

## 8. ホームランチャー機能について

本アプリは Android の **ホームランチャー(Home Launcher)** として動作します。デフォルトホームアプリに設定すると、ホームボタン押下時に本アプリが起動します。

- 個人を識別する情報は収集しません
- ホーム画面上のすべての操作は端末内で完結します
- 設定 > アプリ > 既定のアプリ > ホームアプリ で他のランチャーに変更できます

## 9. ポリシーの変更

本ポリシーの内容は予告なく変更される場合があります。重要な変更がある場合は、アプリ内またはストアページで告知します。

## 10. お問い合わせ

本ポリシーに関するご質問は、Google Play ストアの開発者連絡先までご連絡ください。

---

*このポリシーは Privacy Policy in Japanese です。English version available upon request.*

# Privacy Policy

**Last updated:** May 5, 2026

SELECT (the "App") respects user privacy. This policy explains what information the App collects and how it is used.

---

## 1. Information We Collect

The App stores the following information **only on your device** and never transmits it externally:

- The list of apps you assign to each category (package name, display name)
- Custom slot settings (label, icon, shortcut name)
- Display settings (visibility of time, date, calendar, Play category, app drawer)
- Order of categories and modes
- Custom theme color, background color, background image URI
- Language settings
- Pro feature purchase status

This data is stored locally using Android's DataStore (on-device storage only).

## 2. App Information on the Device

As a launcher, the App reads the icons and labels of installed apps via Android's `PackageManager` API.

- Only the minimum information needed to display and launch apps is accessed.
- Information about installed apps is never transmitted externally.
- The App enumerates only those apps permitted by the `<queries>` declaration in the Android Manifest (apps that declare a `MAIN/LAUNCHER` intent).

## 3. Network Communication

The App does not make any internet connections.

- No data is sent to any server.
- No external APIs are called.
- No analytics tools (e.g., Firebase Analytics, Crashlytics) are used.
- No advertising networks are integrated.

The only exception is **Google Play billing** (when purchasing the Pro version): the Google Play Billing Library communicates with Google's servers. This is a standard feature provided by Google, and the App itself does not transmit any personal information.

## 4. Sharing with Third Parties

The App does not share any collected information with third parties.

## 5. Children's Personal Information

The App does not knowingly collect personal information from children under 13.

## 6. Permissions

The App requests the following permissions:

- `com.android.vending.BILLING`: For Google Play billing (when purchasing the Pro version).
- `<queries>` declaration: For launcher functionality, to read basic information about installed apps.

No other permissions (contacts, location, camera, microphone, etc.) are requested.

## 7. Data Deletion

You can reset all settings via "Reset all to defaults" in the settings screen. To remove all data completely, go to **Settings > Apps > SELECT > Storage > Clear data** on your device.

## 8. About the Home Launcher Function

The App functions as an Android **home launcher**. When set as the default home app, it launches when you press the home button.

- The App does not collect personally identifiable information.
- All operations on the home screen are completed on-device.
- You can switch back to another launcher via Settings > Apps > Default apps > Home app.

## 9. Changes to This Policy

This policy may be updated without prior notice. Significant changes will be announced in the App or on the store page.

## 10. Contact

For questions about this policy, please contact the developer via the contact information on the Google Play Store.

---

*Japanese version available on request / 日本語版もご利用いただけます。*
