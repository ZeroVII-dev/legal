# LUNA Privacy Policy

Last updated: 2026-07-07

This Privacy Policy explains how **LUNA** (“the App”) handles information when you use it on your Android device.

## 1) What this App is
LUNA is an on-device life companion app built with Flutter. It includes:
- A quest system (Daily/Main/Challenge quests)
- A sequence + digestion + ascension system per pathway
- A habit streak tracker (Fortune pathway)
- A notes journal
- Reminders and full-screen alarms (local notifications)
- An AI companion (“LUNA”) powered by Mistral (via an API key you provide)
- An optional App Lock (PIN/biometric)

## 2) Data we collect
### 2.1 Data you enter and create in the App
The App stores and uses data you provide, including:
- Your profile (username, active pathways, primary pathway)
- Quest details (title/description/pathways/type/status, streak counters, reminders, etc.)
- Notes journal content
- Water logs (daily water glass count)
- Reminders settings you create (custom reminders)
- LUNA personality configuration (your editable JSON fields)
- Chat history with LUNA (stored locally)
- App lock configuration (whether enabled, timeout settings; PIN is stored securely)

### 2.2 Data stored by the App locally
All user content above is stored on your device using:
- **SQLite** (quests, sequences, reminders, notes, chat messages, collectibles, achievements, and daily logs)
- **SharedPreferences** (non-sensitive app settings, feature flags, and developer unlock state)
- **flutter_secure_storage** (for sensitive secrets such as your AI API key and the App Lock PIN)

### 2.3 API key
If you enable AI features, you paste your **Mistral API key** in Settings.
- The key is stored on-device using secure storage.
- The App uses your key only to call Mistral for generating responses.

### 2.4 AI prompts and responses (network request)
When you message LUNA, the App sends:
- Your user message
- A system prompt containing your configured LUNA personality and **a live snapshot** of your in-app progress (quests, streaks, sequence progress, water status)
- A portion of your chat history (your previous messages in the session)

Mistral returns the assistant response, which the App displays and may add to your local chat history.

## 3) What we do NOT do
- **No telemetry / analytics**: the App does not send usage metrics to the developer.
- **No third-party tracking** for user behavior inside the App.
- **No cloud sync**: your data is not synchronized to any server by the App.
- **No selling of personal data**.

## 4) Notifications (local only)
The App schedules local notifications using Android notification APIs and `flutter_local_notifications`.
- Notifications are delivered by your device OS.
- Notification content may include your reminder title/message.

When you tap certain notifications (e.g., quest reminders or alarms), the App navigates to the relevant screen.

The App may also schedule an in-app timer for foreground behavior while the app is open.

## 5) Security
### 5.1 On-device protection
- API key and App Lock PIN are stored using secure storage.
- Other app data is stored locally in SQLite / SharedPreferences.

### 5.2 Reasonable safeguards
You should still keep your device security enabled (lock screen, OS updates). Although data is stored locally, a compromised device can expose stored information.

## 6) Sharing / exporting your data
### 6.1 In-App export/import
Developer Options include:
- Export database (copy database snapshot to clipboard)
- Import database (restore database from JSON)

If you use these features, the content you export/import may contain your quests, notes, chat history, and other local data.

### 6.2 Sharing collectibles/relics
The App can generate an image and open your share sheet for collectibles and Wayfarer Relics.
- The shared content is generated from what you have in the App.
- The App does not automatically upload the image to a server; sharing is handled by your device OS and the apps you select.

### 6.3 User-initiated deletion (Data Deletion)
Because all your data is stored locally on your device, you have absolute control over it.

You can delete your entire data profile, notes, chat logs, and configuration settings at any time by either:
- Clearing **App Data** for LUNA in your Android system settings, or
- Uninstalling the App from your device.

If you used the Developer Options export/import features, you should treat any exported snapshots you made as personal data too.

## 7) Children’s privacy
LUNA is designed to be a safe environment for users of all ages.

Because the App operates entirely on-device and stores all data locally in an isolated SQLite database, the App does not collect, harvest, or transmit any personal information from children to the developer or any hidden third-party servers.

If AI features are used via a user-provided API key, prompts are processed directly through Mistral AI in accordance with their privacy standards.


## 8) Changes to this policy
We may update this policy from time to time. The “Last updated” date will change accordingly.

## 9) Contact
For questions about this Privacy Policy, you can contact the app creator via the email listed in the app’s About screen.
