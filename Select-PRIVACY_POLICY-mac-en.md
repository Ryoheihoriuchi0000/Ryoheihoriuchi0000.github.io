# Privacy Policy

**Last updated**: May 30, 2026
**Target**: SELECT for macOS

SELECT (the “App”) respects your privacy. This policy explains what information the App collects, uses, and stores.

---

## 1. Information We Collect

The App stores the following information **only on your device and within your own iCloud account**. It is not sent to any third-party server.

- The list of items you registered under each category
  - App bundle ID / executable path
  - URL / Shortcut name / security-scoped bookmarks (user-selected files / folders)
  - Display label and custom icon (SF Symbol name)
- Per-mode (Profile) settings
  - Name, icon, tab order, and per-tab pin state
  - Menu bar / floating bar label-display style
- App-wide settings
  - Language (`ja` / `en`), iTunes Search country code (`jp` / `us`, etc.)
  - Global hotkey string, Dock icon visibility, Launch-at-login flag
  - Floating bar position / always-on-top pin state

These are stored in Apple's **SwiftData** (a local SQLite store inside the App's container) and in your **CloudKit private database**.

## 2. Information About Installed Apps

For its launcher functionality, the App uses macOS **Launch Services** and **`NSWorkspace`** APIs to read installed apps' bundle IDs, display names, and icons.

- Only the minimum information needed to list and launch apps is read
- This information is never transmitted to any external server
- App launching uses only the standard APIs (`NSWorkspace.openApplication(at:configuration:)` / `LSApplicationWorkspace`); the App does not access the internal state of other apps

## 3. File / Folder Access

When you register a `path`-type item (a file or folder you choose), the App generates and stores a security-scoped bookmark required by macOS **App Sandbox** (`URL.bookmarkData(options: .withSecurityScope, ...)`).

- Bookmark data is kept only inside the App's sandbox container and within your iCloud-synced data
- The App does not read the **contents** of the bookmarked files / folders (only opens them in Finder or launches them)

## 4. Network Communication

The only network connections the App makes are:

| Destination | Purpose | Personal info sent |
|---|---|---|
| **iTunes Search API** (`itunes.apple.com`) | Fetch icon images of App Store apps | None (queries contain only public bundle IDs) |
| **Apple CloudKit** (`*.icloud.com`) | Syncing settings / items to your private database | Encrypted via your Apple ID; Apple's Privacy Policy applies |

- The App uses **no analytics tools** (Firebase Analytics, Crashlytics, Sentry, etc.)
- The App contains **no advertising networks**
- The App does not communicate with any other external servers

## 5. About iCloud Sync

The App uses Apple's **CloudKit private database** to automatically sync settings and items across multiple Macs.

- Synced data is stored **only in your own iCloud account**. The developer and third parties cannot access it
- Encryption, storage, and access control of the synced data are entirely managed by Apple, and Apple's Privacy Policy applies
- If you are not signed in to iCloud, the App operates locally only
- You can delete the App's iCloud data at any time from your Apple ID management page

## 6. Disclosure to Third Parties

The App does not provide collected information to any third party.

## 7. Children's Privacy

The App does not knowingly collect personal information from children under 13.

## 8. Permissions / Entitlements

The App uses the following macOS entitlements:

- `com.apple.security.app-sandbox`: App Sandbox restriction required for App Store distribution
- `com.apple.security.files.user-selected.read-write`: Read/write access to files / folders the user picks via `NSOpenPanel`
- `com.apple.security.files.bookmarks.app-scope`: Resolving security-scoped bookmarks
- `com.apple.security.network.client`: Communication with iTunes Search API and CloudKit
- `com.apple.developer.icloud-services` (CloudKit): Settings sync via the private database
- `com.apple.developer.icloud-container-identifiers`: Use of the dedicated iCloud container

No other permissions (contacts, location, camera, microphone, automation, full disk access, etc.) are **requested under any circumstance**.

## 9. Deleting Data

- In-app: Each item / mode can be deleted from edit mode
- Local: Delete the **`com.artemis.select.mac`** folder under **Finder → Go → Go to Library → Containers** to remove all local data of the App
- iCloud: From **System Settings → Apple ID → iCloud → Manage Apps Using iCloud → SELECT**, delete the App's iCloud data
- The App itself: Move **SELECT.app** to Trash from **Finder → Applications** for complete removal

## 10. About Launcher Functionality

The App runs as a **menu-bar-resident launcher** for macOS.

- It does not collect personally identifying information
- All operations on the menu bar / floating bar are completed entirely on your device
- The global hotkey (e.g., `cmd+shift+0`) is registered with the OS via Carbon Hot Key Manager and is used **only to toggle the App's floating bar**. The App does not log or transmit key input

## 11. Changes to This Policy

The contents of this policy may change without prior notice. When significant changes occur, the App or its store page will provide an announcement.

## 12. Contact

For questions about this policy, please use the developer contact information on the Mac App Store.

---

*This is the English version. 日本語版もあります (`Select-PRIVACY_POLICY-mac.md`).*
