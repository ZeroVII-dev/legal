# The Nexus Privacy Policy

Last updated: 2026-07-09

This Privacy Policy explains how **The Nexus** ("the App") handles information when you use it on your Android device.

## 1) What this App is

The Nexus is an on-device Android home-screen launcher built for app developers, built natively with Kotlin and Jetpack Compose. It includes:

- A home screen with a live clock, calendar, and device/network telemetry panel
- Two or more user-defined "rails" of pinned apps (e.g. Deployments, Toolkit), with auto-detection of debuggable apps
- A swipe-up app drawer with search over your installed apps
- Per-app quick actions (copy package name, app info, hide, uninstall)
- Optional gestures (swipe down for notifications, double-tap to lock)
- An optional black wallpaper for the home and lock screens

The Nexus replaces your Android home screen (it is a launcher), but it does not require an account, does not include ads, and does not include any AI or chat features.

## 2) Data we collect

### 2.1 Data the App creates and stores on your behalf

The App stores and uses data generated purely from your own configuration, including:

- Which apps you have pinned, and to which rail
- The names, order, and configuration of your custom rails
- Which apps you have chosen to hide from the drawer
- Your display preferences (roman/24-hour clock, accent color, auto-detect toggle, wallpaper toggle, etc.)

None of this data describes you personally — it is app/package identifiers and your own settings choices.

### 2.2 Data stored by the App locally

All data above is stored **only on your device**, using Android's Jetpack **DataStore (Preferences)**. Nothing is uploaded to the developer or to any third party.

### 2.3 Data read from your device (not stored beyond display)

To show its telemetry panel and populate the app drawer/rails, the App reads, but does not persist beyond the current session:

- The list of apps installed on your device (via `PackageManager`), including package names, labels, icons, and whether an app is marked debuggable — used to populate the drawer and auto-detect Deployments
- Basic device info: Android version/API level, device model, RAM and storage usage, battery level, local IP address, Wi-Fi/cellular connection type, and ADB (USB/Wi-Fi) debug status
- None of this is sent anywhere; it is displayed to you on your own home screen

## 3) Network requests the App makes

The App does not have an account system, analytics SDK, or crash reporting service. It makes exactly two kinds of outbound network calls, both anonymous and both purely to power the telemetry panel:

- **Public IP lookup**: a request to `api.ipify.org` to display your public IP address. No other data is sent with this request.
- **Latency check**: a raw TCP connection attempt to a public DNS resolver (`8.8.8.8`, port 53) to measure round-trip time. No data is exchanged beyond the connection handshake.

Neither request includes any of your personal data, app list, or settings.

## 4) What we do NOT do

- **No telemetry / analytics**: the App does not send usage metrics to the developer.
- **No accounts, sign-in, or user identifiers**.
- **No third-party tracking** of your behavior inside the App.
- **No cloud sync**: your rails, settings, and hidden-apps list are never synchronized to any server.
- **No advertising**.
- **No selling of personal data** — the App has no personal data to sell.

## 5) Permissions the App requests, and why

| Permission | Purpose |
|---|---|
| `QUERY_ALL_PACKAGES` | Required for any launcher to enumerate and display your installed apps. |
| `INTERNET`, `ACCESS_NETWORK_STATE` | Powers the public-IP and latency telemetry described in §3, and detects your connection type. |
| `REQUEST_DELETE_PACKAGES` | Lets the per-app "Uninstall" action launch the system uninstall flow. |
| `SET_WALLPAPER` | Lets the App set (and, if you turn the setting off, reset) a black home/lock wallpaper. Opt-out anytime in Settings. |
| Accessibility service (opt-in, enabled manually by you in system settings) | Used **solely** to trigger the system "lock screen" action for the optional double-tap-to-lock gesture. The service does not read screen content, does not log events, and takes no other action. |

## 6) Security

All App data lives in Android's app-private storage, sandboxed by the OS from other apps. There is no server component, so there is no remote database to be compromised. You should still keep your device itself secure (screen lock, OS updates) — a compromised device can expose any app's local data, including this one's.

## 7) Sharing / exporting your data

The App does not include an export/import feature. Any "copy" actions (e.g. copying a package name or a telemetry value) place text on your device clipboard only, for your own use — nothing is transmitted.

### Data deletion

Because all App data is stored locally on your device, you have full control over it. You can delete it at any time by:

- Clearing **App Data** for The Nexus in Android system settings, or
- Uninstalling the App.

Note: if The Nexus is your active launcher, Android will prompt you to choose a new default home app before uninstalling.

## 8) Children's privacy

The Nexus is a developer productivity tool and is not directed at children. It collects no personal information from any user, and has no mechanism to identify a user's age. As described above, all data stays on-device.

## 9) Changes to this policy

We may update this policy from time to time. The "Last updated" date above will change accordingly.

## 10) Contact

For questions about this Privacy Policy, contact the developer at **zerovii.dev@gmail.com**.
