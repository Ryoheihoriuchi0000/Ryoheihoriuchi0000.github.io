# Support

## SELECT Support Page

Thank you for using SELECT.

## Contact

For questions, bug reports, or feature requests, please reach out to the email below.

**Email:** select2026@outlook.jp

Including "SELECT feedback" in the subject line helps us respond faster.

## Frequently Asked Questions

**Q. SELECT flashes briefly when I tap a widget tile**
A. iOS widget extensions can't call custom URL schemes directly, so by default a tap is routed through SELECT before reaching the target app. To eliminate this flash, install the **SELECT Widgets** shortcut into Apple's Shortcuts app **once**. You can do this from Settings → Faster Widget Launches in the app, or from the onboarding screen titled "Speed up launches".

**Q. Tapping a widget tile does nothing**
A. Please check the following in order:
- Is the "SELECT Widgets" shortcut installed in Shortcuts.app? (Settings → Faster Widget Launches)
- Is the target app installed on this device?
- Long-press the widget on the home screen → Edit Widget → make sure the correct mode is selected

**Q. The app I want to register doesn't appear in search**
A. SELECT uses Apple's iTunes Search API to look up apps in the App Store. Try switching the storefront (Settings → App Search → Search Country/Region). If it still doesn't show up, the app may not be available on that store.

**Q. The picker says "URL scheme not found" (old versions)**
A. v1.x and later no longer require a URL scheme. The SELECT Widgets shortcut launches apps by bundle ID directly, so every App Store app can be added and launched.

**Q. How do I cancel Pro?**
A. SELECT Pro is a **one-time purchase**, not a subscription. Once bought it remains active permanently. If you bought it by mistake, please request a refund through App Store support.

**Q. How do I restore Pro on a new device?**
A. Tap Settings → Pro → Restore Purchases inside the app. Pro will reactivate on any device signed in to the same Apple ID.

**Q. How does iCloud sync work?**
A. When Pro is enabled, your registered apps and mode settings sync across your Apple devices via iCloud. You can enable/disable sync from iOS Settings → [Your Name] → iCloud → SELECT.

**Q. Is there a limit on how many apps a widget can show?**
A. Due to iOS widget constraints, a single page can display roughly 5–7 apps for a Large widget. If you register more, a "→" page-arrow appears at the top of the widget to cycle through pages. The Pro folder feature lets you group apps into sub-categories for further organization.

**Q. How do I add another mode (profile)?**
A. Tap the mode name at the top of the editor (e.g. "Outing"), then "Add Mode" at the bottom of the sheet. **Multiple modes is a Pro feature.**

**Q. How do I delete an item?**
A. Three options:
- **Swipe**: swipe right-to-left on a row and tap "Delete"
- **Selection mode**: tap the "Select" button at the top, pick items, tap "Delete"
- **Tap a row**: opens the rename screen (label only, doesn't delete)

Deletions can't be undone.

**Q. Can I move or copy items between tabs / modes?**
A. Enter selection mode, pick the items you want, then tap "Move" or "Copy" to open a destination picker (any tab in any mode).

**Q. Can I lock the widget colour?**
A. Settings → Widget Color lets you choose Fixed White / Fixed Dark / Match Device. The choice applies to every mode.

**Q. The iOS 18 "Tinted" home-screen mode washes out the widget colours**
A. iOS 18's Tinted display mode is an Apple feature — every widget visible on the home screen is recoloured. SELECT applies `widgetAccentedRenderingMode(.fullColor)` to app artwork to preserve original colours where possible, but background tints can't be fully opted out of (Apple behaviour).

**Q. Can I switch widget tabs between icons and text?**
A. Yes — Settings → Tab display → Icon / Text. The setting applies to both the in-app editor and the home-screen widget.

**Q. Can I hide the icons and show app names only?**
A. Open the mode-switch sheet (tap the mode name at the top), then toggle "Show app icons" off for that specific mode. Each mode owns its own setting.

**Q. Can I hide the Enjoy tab?**
A. Yes — the mode-switch sheet has a "Hide Enjoy tab" toggle per mode. Turning it on collapses the tab bar to 4 tabs while preserving any items you had registered there.

**Q. How do I completely delete my data?**
A. Uninstalling the app (iOS Settings → General → iPhone Storage → SELECT → Delete App) removes all on-device data. If you had iCloud sync enabled, also delete from iOS Settings → [Your Name] → iCloud → Manage Storage → SELECT → Delete Data.

**Q. How do I change the app's language?**
A. iOS Settings → General → Language & Region for system-wide language, or iOS Settings → SELECT → Language for an app-only override.

---

Last updated: May 19, 2026

日本語版: [サポート (iOS)](./Select-SUPPORT-ios)
