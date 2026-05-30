# Support

## SELECT for macOS Support Page

Thank you for using SELECT.

## Contact

For questions, bug reports, or feature requests, please reach out to the email below.

**Email:** russell2026@outlook.jp

Including "SELECT for macOS feedback" in the subject line helps us respond faster.

## Frequently Asked Questions

**Q. There are too many menu-bar icons / they get in the way**
A. Each tab's menu-bar visibility can be toggled individually in **Settings → Menu Bar** (per-tab toggles). The SELECT app icon (♻) always stays — turning off unnecessary tabs makes things tidier.

**Q. Can I make the menu-bar icons simpler?**
A. Yes — pick **Simple icon** in Settings → Menu Bar → Label display. The phone / brain glyphs drop out, leaving just the arrow + a capsule outline. The setting is **per mode**, so switching modes also switches the style automatically.

**Q. How do I show / hide the floating bar?**
A. The default global hotkey **`cmd + shift + 0`** toggles it. You can also toggle "Show at launch" in Settings → Floating Bar to control its launch-time state. While visible, the menu-bar ♻ icon's dropdown menu has a toggle as well.

**Q. The floating bar disappears behind other windows**
A. Click the pin button (📌) on the right end of the floating bar to enable Always on Top. When pinned off, the bar behaves like a normal window and falls behind other apps.

**Q. Can I move the floating bar?**
A. Drag it anywhere on the screen — the position auto-saves after 0.2 seconds and is restored on the next launch. If an external display is disconnected and the bar would land off-screen, it snaps back to the top-left of the main display.

**Q. How do I change the global hotkey?**
A. In Settings → Floating Bar → Hotkey, type a new combination in the format `<modifier>+...+<key>` (e.g., `cmd+ctrl+space`). Allowed keys: cmd / shift / ctrl / opt + 0–9 / a–z / space / return / tab / esc. The change takes effect immediately. **The hotkey is global across modes** (app-wide).

**Q. The global hotkey doesn't work**
A. Another app may have already registered the same combination at the OS level. Try a different combination. The default `cmd+shift+0` was chosen to avoid colliding with common combos like `cmd+shift+s` (Save As).

**Q. Finder / Mail / built-in apps won't launch**
A. As of v1.x, these launch via the path-type item. In the item editor, check that "App path" is correctly populated (e.g., `/System/Library/CoreServices/Finder.app`).

**Q. How do I hide the Dock icon?**
A. Turn off **Settings → Window → Show in Dock**. When off, SELECT is also removed from the Cmd+Tab switcher and runs as a **menu-bar + floating-bar only** background process.

**Q. Can SELECT launch automatically at login?**
A. Yes — toggle **Settings → Window → Launch at login**. SELECT is then registered in your macOS Login Items.

**Q. How do I add another mode (profile)?**
A. Use the **Add** button at the top of the sidebar. There is no IAP gating on the Mac version — modes are unlimited. **When you create a new mode, the settings of the currently-active mode (menu-bar / floating-bar styles, per-tab visibility) are automatically copied** so you don't start from scratch.

**Q. How do I rename or change a mode's icon?**
A. The **Edit** button at the top of the sidebar opens a sheet for renaming and picking an SF Symbol icon. The Built-in mode (the initial default) can also be edited; only deletion is restricted.

**Q. Why are menu-bar and floating-bar settings stored per mode?**
A. That's intentional — different modes are for different situations, so the display style (simple vs. default icons) and the set of visible tabs are scoped per mode. The hotkey and the floating-bar position / pin state remain app-global.

**Q. Is iCloud sync required?**
A. No — if you're not signed in to iCloud, SELECT operates locally only. When signed in, syncing happens automatically. Synced data is stored in your own CloudKit Private Database; the developer and third parties have no access.

**Q. How do I migrate data to another Mac?**
A. The simplest path is **iCloud sync** (automatic if you're signed in with the same Apple ID on both Macs). For manual migration, use **Settings → Support → Export to JSON** on the source Mac and **Import from JSON** on the destination.

**Q. What happens to existing data when I import JSON?**
A. Import uses UUID-based upsert. **Items / modes with the same UUID are overwritten; new UUIDs are added.** If you want a clean replace, delete local data first, then import.

**Q. The app I want isn't showing up in search**
A. SELECT uses Apple's iTunes Search API. Check that **Settings → Language & Region → Country code** matches the App Store storefront where the app is published (e.g., `jp` for Japan, `us` for the United States).

**Q. How do I delete an item?**
A. Right-click an item row and choose Delete, or enter edit mode, select items, and delete them in bulk.

**Q. Can I move or copy items between tabs / modes?**
A. Enter edit mode, select items, then tap **Move** or **Copy** to open a destination picker. Drag-and-drop into folders is also supported.

**Q. How do I completely delete my data?**
A. Three steps for a full wipe:
- Local: Delete the folder **`com.artemis.select.mac`** under **Finder → Go → Go to Library → Containers**
- iCloud: From **System Settings → Apple ID → iCloud → Manage Apps Using iCloud → SELECT**, delete the iCloud data
- App: Move **SELECT.app** to Trash from **Finder → Applications**

**Q. How do I change the app's language?**
A. **Settings → Language → 日本語 / English**. The change applies after restarting the app. This is a per-app setting and is independent from your macOS system language.

**Q. The "Hotkey" text field stays focused inside Settings**
A. Fixed in v1.x. Please reopen the Settings window. If the issue reproduces, please get in touch.

---

Last updated: May 30, 2026

日本語版: [サポート (macOS)](./Select-SUPPORT-mac)
