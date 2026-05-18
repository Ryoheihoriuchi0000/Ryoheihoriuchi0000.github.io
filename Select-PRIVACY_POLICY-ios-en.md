# Privacy Policy (iOS)

**Last updated:** May 19, 2026

SELECT (the "App") respects user privacy. This policy explains what information the iOS version of the App collects and how it is used.

---

## 1. Information We Collect

The following information is stored **only on your device** and is never sent to any server owned by the App developer.

- Apps registered to each tab (display name, bundle ID, icon URL, custom URL scheme)
- Custom item settings (label, icon, shortcut URL, website URL)
- Display preferences (tab icon/text style, widget colour, Enjoy-tab visibility)
- Sort order of categories and modes
- Language preference
- Pro purchase status
- Whether the SELECT Widgets shortcut has been installed

Data is persisted in iOS **SwiftData** (local storage) and the **App Group** container (`group.com.artemis.select.ios`). The App Group is used so the main app and the widget extension can share the same data.

---

## 2. App Search (iTunes Search API)

When you tap "Add Item" to register an app, the App calls Apple's public **iTunes Search API** (`https://itunes.apple.com/search`).

- Sent: **only the search query you typed** (e.g. "PayPay")
- Received: app name, bundle ID, icon URL, App Store URL, etc.
- The query is never stored on the App developer's servers (the App has no servers of its own)
- Apple's logging of the API call is governed by Apple's own privacy policy

Apps you register are saved into the local SwiftData store and rendered on your widgets.

---

## 3. App Icon Cache

When you register an app, its icon is downloaded from Apple's CDN and cached inside the App Group container.

- Source: Apple CDN endpoints (e.g. `is1-ssl.mzstatic.com`)
- Stored at: `Icons/{bundleId}.png` inside the App Group container
- Purpose: instant widget rendering without a network round-trip
- Shared with third parties: never

---

## 4. iCloud Sync (Pro feature only)

When you purchase Pro and enable iCloud sync, your SwiftData store is encrypted and saved to your own **CloudKit Private Database** (a private area under your own Apple ID), and synced across your Apple devices.

- Storage: Apple CloudKit, in your personal iCloud account
- Access: **only you**. Neither the App developer nor any third party can access your CloudKit data.
- Encryption: TLS in transit, Apple-managed encryption at rest
- Disable: iOS Settings → [Your Name] → iCloud → SELECT (turn off)

Free users never use this feature; data stays entirely on-device.

---

## 5. Widget Launch (Shortcuts.app integration)

Tapping a tile in the widget launches the target app via Apple's built-in **Shortcuts.app**.

- Path: SELECT widget → SELECT host app (briefly) → Shortcuts.app → target app
- Sent: only the **bundle identifier** of the target app (e.g. `jp.ne.paypay.app`)
- Everything happens entirely on the device
- Nothing is sent to Apple servers nor to the App developer

This requires installing a shortcut named **SELECT Widgets** into Shortcuts.app one time. The shortcut is an Apple-signed definition file distributed via iCloud.

---

## 6. Network Activity

The App makes the following limited network requests only.

- `https://itunes.apple.com/search`: app metadata lookup (only while you are using "Add Item")
- Apple CDN: app icon image downloads
- Apple CloudKit: iCloud sync (only when enabled, Pro only)
- Apple StoreKit: Pro purchase processing

What we do **not** do:
- No requests to any server owned by the App developer (we have no servers of our own)
- No analytics SDKs (no Firebase Analytics, Crashlytics, Sentry, etc.)
- No advertising networks
- No third-party SDKs other than Apple frameworks (StoreKit / CloudKit / WidgetKit / Shortcuts)

---

## 7. Disclosure to Third Parties

The App does not share collected information with third parties. Network requests to Apple (iTunes Search API, CloudKit, StoreKit) are governed by Apple's own privacy policy.

---

## 8. Children's Personal Information

The App does not knowingly collect personal information from children under 13.

---

## 9. Permissions and Capabilities

The App uses the following iOS capabilities.

- `LSApplicationQueriesSchemes`: A list of URL schemes used for `canOpenURL` checks on-device (no network traffic involved)
- `App Group` (`group.com.artemis.select.ios`): Shared data store between the main app and the widget extension
- `WidgetKit`: Renders home-screen widgets
- `AppIntents`: Defines button actions inside widgets
- `CloudKit`: iCloud sync (only when enabled, Pro only)
- `StoreKit`: In-app purchase processing

The App **never requests** the following permissions:
- Camera, microphone, location, contacts, photos, Bluetooth, local network, notifications

---

## 10. In-App Purchases

Pro purchases go through Apple's **App Store / StoreKit**.

- Seller of record: Apple Inc.
- Payment method: as registered to your Apple ID
- The App only verifies the resulting receipt and never has access to your card details
- Receipts and support requests are handled by the App Store

---

## 11. Deleting Your Data

You can reset all settings to their defaults from inside the Settings screen. For a full uninstall, use **iOS Settings → General → iPhone Storage → SELECT → Delete App**.

If iCloud sync is enabled, you can additionally remove the cloud copy from **Settings → [Your Name] → iCloud → Manage Storage → SELECT → Delete Data**.

---

## 12. Changes to This Policy

This policy may be updated without prior notice. Significant changes will be announced in-app or on the store listing.

---

## 13. Contact

For questions about this policy, please use the developer contact details listed on the App Store.

---

日本語版: [プライバシーポリシー (iOS版)](./Select-PRIVACY_POLICY-ios)
