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
