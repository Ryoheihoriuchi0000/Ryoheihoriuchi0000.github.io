[日本語](stadius-privacy.html)

# Privacy Policy

**Studypress** (iOS, hereinafter "the App") protects users' personal information appropriately in accordance with this Privacy Policy.

Last updated: October 24, 2026

---

## 1. Information We Collect

The App collects the following information in order to provide its service.

### 1-1. Information you provide directly
- Email address (only if you sign up with email authentication)
- Display name
- Your choice of profile icon
- Booked slots (day of the week, time, and whether weekly or one-time)
- Weekly goal (number of slots)
- "To-Do", "Penalty" and "Supporter" (only if you use Studypress Pro and set them yourself)

### 1-2. Information provided by authentication providers
- If you use Sign in with Apple: the private relay email address or your real email address provided by Apple (as you choose)

### 1-3. Information collected automatically
- User identifier (UID) issued by Firebase Authentication
- Account creation date and time
- Attendance records (time present in each slot and the ○ / △ / ✕ result)
- Level and team
- Time zone and display language settings
- Advertising identifier (IDFA; only if you allow tracking on your device) and records of ad impressions and interactions (only on iPhone and iPad, when you are not using Studypress Pro)

The App does not collect any other activity history, location information, contacts or similar data.

---

## 2. Handling of Camera Video

During a slot, your device's camera video is blurred and then reduced to **64×64 pixels** before it is sent.

- The reduction is done on your device; video at its original resolution never leaves your device
- Because of this reduction, the original video cannot be restored
- The relay server discards each image as soon as it has delivered it to the members of the same slot, and neither stores nor records it
- There is no recording feature
- The operator cannot view the video
- Audio is not handled. The App does not ask for microphone permission

Presence is judged only by the time you were in your seat. The App does not judge concentration or anything else from the content of the video.

---

## 3. Purposes of Use

The information collected is used only for the following purposes.

- Authentication and account management for the App
- Recording booked slots and attendance, and sharing them within your team
- Notifications before a slot starts
- Determining whether the weekly goal was achieved or not achieved
- Responding to misuse and violations of the terms
- Improving the service and considering the development of new features
- Fulfilling legal obligations

On iPhone and iPad, the App uses Google AdMob to display ads. The advertising identifier, approximate location estimated from your IP address, and records of ad impressions and interactions are used by Google to deliver ads and measure their effectiveness. No other data is used for advertising or marketing purposes. You can change tracking permission at any time in your device's Settings > Privacy & Security > Tracking.

---

## 4. Provision to Third Parties

Except where required by law, we do not provide the information collected to third parties.

The App uses the following external services, and the information above is stored on their respective servers.

| Service | Provider | Purpose |
| --- | --- | --- |
| Firebase Authentication | Google LLC | Authentication and account management |
| Cloud Firestore | Google LLC | Storage of schedules, attendance and team information |
| Firebase Cloud Messaging | Google LLC | Slot start notifications |
| Cloud Functions | Google LLC | Weekly result processing and calendar feed delivery |
| Stripe | Stripe, Inc. | Penalty payments (only if set) |
| Google AdMob | Google LLC | Ad delivery (iPhone and iPad only; not shown with Studypress Pro) |

---

## 5. Payment Information

Payment method information is handled only if you set a "Penalty" in Studypress Pro.

- Payment method information is held by **Stripe, Inc.**
- The only data stored on the operator's servers are the customer ID and payment method ID issued by Stripe, the card brand name, and the last 4 digits of the card number
- **The operator never receives the card number itself**
- The operator does not hold any money in advance. A charge is made only once it is confirmed that the weekly goal was not reached
- You can remove the payment method at any time in the App's settings

---

## 6. Calendar Sync

Calendar sync is **turned off by default**. The following takes place only if you turn it on in Settings.

### 6-1. Apple Calendar
- The App creates a dedicated calendar named "Studypress" on your device and writes slots only to that calendar
- What is written is not sent to the operator's servers
- **The App neither reads nor writes events in any other calendar**
- When you turn sync off, the dedicated calendar it created is deleted along with its contents

### 6-2. Google Calendar / Outlook
- The App issues a subscription URL and places the start times of your upcoming slots on the operator's servers
- **This URL has no authentication.** Anyone who knows the URL can view the start times of your slots
- Only start times and durations are placed there; names, email addresses, teams and attendance records are not included
- You can disable the subscription URL at any time in the App's settings. Once disabled, the data placed there can no longer be accessed

---

## 7. Retention Period and Deletion

When you delete your account, the information linked to you is deleted.

- You can delete your account from "Settings" → "Delete Account" in the App
- Your schedule, attendance records, level and team information are all erased
- Records of reports may be retained for a certain period to deal with misuse

---

## 8. Device Permissions

| Permission | Purpose |
| --- | --- |
| Camera | Used only to relay video during a slot |
| Notifications | Used only for alerts before a slot starts |
| Calendars | Used only when calendar sync is turned on. Limited to reading and writing the dedicated "Studypress" calendar |
| Microphone | Not used (permission is not requested) |

---

## 9. Age Restriction

Persons under the age of 13 may not use the App.

---

## 10. Contact

For questions about this Policy, please contact us at the address below.

**Email:** russell2026@outlook.jp

---

Effective date: September 13, 2026
