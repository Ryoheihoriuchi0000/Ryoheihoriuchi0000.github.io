# Privacy Policy (iOS)

**Last updated:** October 23, 2026

SELECT (the "App") respects user privacy. This policy explains what information the iOS version of the App collects and how it is used.

---

## 1. Information We Collect

The following information is stored **only on your device** and is never sent to any server owned by the App developer.

- Apps registered to each tab (display name, bundle ID, icon URL, custom URL scheme)
- Custom item settings (label, icon, shortcut URL, website URL)
- Display preferences (tab icon/text style, widget colour, Enjoy-tab visibility)
- Sort order of categories and modes
- Language preference
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

## 4. iCloud Sync

Your data is stored in your own CloudKit Private Database (a private area under your Apple ID). This applies to every user.
Neither the developer nor any third party can access your CloudKit data.

---

## 5. Widget Launch

Tapping a tile in the widget hands the target app's bundle identifier to iOS LaunchServices to launch the app.
No network traffic is generated, and no information other than the target bundle identifier leaves the device.
Optionally, an integration named "SELECT Widgets" lets you launch user-authored Shortcuts. The default launch path is unaffected by whether you install it.

---

## 6. Network Activity

The App makes the following limited network requests only.

- `https://itunes.apple.com/search`: app metadata lookup (only while you are using "Add Item")
- Apple CDN: app icon image downloads
- Apple CloudKit: iCloud sync
- Google Firebase Authentication: measuring usage (see 6-1)
- Google Mobile Ads (AdMob): a banner ad below the editor screen and a full-screen ad when switching tabs (see 6-2)

What we do **not** do:
- No requests to any server owned by the App developer (we have no servers of our own)
- No analytics SDKs (no Google Analytics, Firebase Analytics, Crashlytics, Sentry, etc.)
- No in-app purchases other than the one-time "Remove Ads" (payment is handled by Apple; the developer never receives card or other payment details)
- No third-party SDKs other than Firebase Authentication and Google Mobile Ads (everything else is an Apple framework: CloudKit / WidgetKit / Shortcuts)

### 6-1. Measuring Usage (Firebase Authentication)

To understand roughly how many people use the App, it uses **anonymous authentication** from Google's **Firebase Authentication**.

- On first launch, a random string called an **anonymous ID** is issued.
- This ID is **never linked to your email address, name, phone number, or any other personal information**. There is no sign-in screen and no account registration.
- The developer can only see **aggregate numbers**: daily active users, monthly active users, and the total number of IDs issued. Individual users cannot be identified or tracked.
- **No record of your behaviour is transmitted** — not which features you use, nor which apps you register.
- The anonymous ID is issued per device, and reinstalling the App produces a different ID. You are never linked across devices as the same person.
- Data handling follows [Google's Privacy Policy](https://policies.google.com/privacy).
- Every feature of the App continues to work with no network connection.

### 6-2. Ads (Google Mobile Ads)

The App shows a banner ad below the editor screen and, every few tab switches in the editor, a full-screen ad, delivered with Google's **Google Mobile Ads SDK (AdMob)**.

- Ads appear only on the editor screen. Widgets, the Settings screen, and the first-launch introduction show no ads.
- To deliver ads, measure their performance, and prevent fraud, Google processes device information such as your IP address, device type, OS version, and records of ad impressions and taps.
- The advertising identifier (IDFA) is used only if you choose "Allow" for tracking. If you do not allow it, every feature still works. You can change this at any time in **iOS Settings → Privacy & Security → Tracking**.
- People who got the App while it was a paid app, and people who bought "Remove Ads", do not see ads.
- Data handling follows [How Google uses information from sites or apps that use its services](https://policies.google.com/technologies/partner-sites) and [Google's Privacy Policy](https://policies.google.com/privacy).

---

## 7. Disclosure to Third Parties

The App does not share collected information with third parties. Network requests to Apple (iTunes Search API, CloudKit) are governed by Apple's own privacy policy.
 The anonymous ID issued by Firebase Authentication is processed by Google solely to count users, and is never provided to any third party. To deliver ads, Google processes the information described in 6-2.
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
- `CloudKit`: iCloud sync
- `App Tracking Transparency`: asks for permission to track, used only to make ads more relevant (declining does not limit any feature)

The App **never requests** the following permissions:
- Camera, microphone, location, contacts, photos, Bluetooth, local network, notifications

---

## 10. Pricing

Every feature of the App is free. The App is supported by ads on the editor screen (see 6-2). The only in-app purchase is the one-time "Remove Ads", which stops ads from being shown. There are no subscriptions.

---

## 11. Deleting Your Data

You can reset all settings to their defaults from inside the Settings screen. For a full uninstall, use **iOS Settings → General → iPhone Storage → SELECT → Delete App**.

If iCloud sync is enabled, you can additionally remove the cloud copy from **Settings → [Your Name] → iCloud → Manage Storage → SELECT → Delete Data**.

The anonymous ID (see 6-1) is also lost from your device when you delete the App, and that ID is never used again. Because the ID itself contains nothing that identifies a person, no individual can be traced from any remaining record.

---

## 12. Changes to This Policy

This policy may be updated without prior notice. Significant changes will be announced in-app or on the store listing.

---

## 13. Contact

For questions about this policy, please use the developer contact details listed on the App Store.

---

日本語版: [プライバシーポリシー (iOS版)](./Select-PRIVACY_POLICY-ios) ・ 简体中文: [隐私政策](./Select-PRIVACY_POLICY-ios-zh-Hans) ・ 繁體中文: [隱私權政策](./Select-PRIVACY_POLICY-ios-zh-Hant) ・ العربية: [سياسة الخصوصية](./Select-PRIVACY_POLICY-ios-ar)
