# Privacy Policy

**Last updated:** October 10, 2026

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

This data is stored locally using Android's DataStore (on-device storage only).

## 2. App Information on the Device

As a launcher, the App reads the icons and labels of installed apps via Android's `PackageManager` API.

- Only the minimum information needed to display and launch apps is accessed.
- Information about installed apps is never transmitted externally.
- The App enumerates only those apps permitted by the `<queries>` declaration in the Android Manifest (apps that declare a `MAIN/LAUNCHER` intent).

## 3. Network Communication

The only network connection the App makes is **Firebase Authentication** (to measure usage — see below). The developer operates no server of their own.

The following are **not used**:

- In-app purchases (every feature of the App is free; there is no billing at all)
- Analytics tools (Google Analytics, Firebase Analytics, Crashlytics, etc.)
- Advertising networks
- Any other external server

### 3-1. Measuring Usage (Firebase Authentication)

To understand roughly how many people use the App, it uses **anonymous authentication** from Google's **Firebase Authentication**.

- On first launch, a random string called an **anonymous ID** is issued.
- This ID is **never linked to your email address, name, phone number, or any other personal information**. There is no sign-in screen and no account registration.
- The developer can only see **aggregate numbers**: daily active users, monthly active users, and the total number of IDs issued. Individual users cannot be identified or tracked.
- **No record of your behaviour is transmitted** — not which features you use, nor which apps you register.
- The anonymous ID is issued per device, and reinstalling the App produces a different ID. You are never linked across devices as the same person.
- Data handling follows [Google's Privacy Policy](https://policies.google.com/privacy).
- Every feature of the App continues to work with no network connection.

## 4. Sharing with Third Parties

The App does not share any collected information with third parties. The anonymous ID issued by Firebase Authentication is processed by Google solely to count users, and is never provided to any third party.

## 5. Children's Personal Information

The App does not knowingly collect personal information from children under 13.

## 6. Permissions

The App requests the following permissions:

- `android.permission.INTERNET`: For Firebase Authentication (added automatically by the Firebase libraries).
- `<queries>` declaration: For launcher functionality, to read basic information about installed apps.

No other permissions (contacts, location, camera, microphone, etc.) are requested.

## 7. Data Deletion

You can reset all settings via "Reset all to defaults" in the settings screen. To remove all data completely, go to **Settings > Apps > SELECT > Storage > Clear data** on your device.

The anonymous ID is also lost from your device when you clear the data or delete the App, and that ID is never used again. Because the ID itself contains nothing that identifies a person, no individual can be traced from any remaining record.

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
