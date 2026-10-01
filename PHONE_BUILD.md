# JARVIS V5.1 — build directly on your Samsung Galaxy F23 5G

This edition is prepared for an on-device Android build environment such as AndroidIDE.

## Recommended setup
- AndroidIDE (on the phone)
- JDK 17
- Android SDK Platform 35
- Android SDK Build-Tools 34.x/35.x as available in the IDE
- Gradle 8.7 + Android Gradle Plugin 8.6.1

AGP 8.6 supports API 35 and uses JDK 17; Gradle 8.7 is the matching Gradle version for AGP 8.6. See Android's compatibility tables.

## Build
1. Extract this ZIP to a normal writable folder, for example `Download/JARVIS_V5_1`.
2. Open the folder containing `settings.gradle.kts` in AndroidIDE.
3. Allow Gradle sync and install/download any missing SDK packages it offers.
4. Select the `app` module.
5. Build the **debug APK** (`assembleDebug`).
6. Install the APK from `app/build/outputs/apk/debug/app-debug.apk`.

## First launch
- Allow microphone access.
- Enable JARVIS Notification Access only if you want notification reading.
- Tap SETTINGS to configure an HTTPS AI backend. Without a backend, local commands and offline basic replies still work.
- Tap HANDS-FREE and say `Hey JARVIS, open YouTube`.

## Important
The app's hands-free feature is a speech-recognition wake-phrase gate, not a dedicated low-power offline wake-word chip/engine. Android may show a persistent microphone foreground-service notification.
