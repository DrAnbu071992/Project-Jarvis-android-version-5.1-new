# JARVIS V5.1 — Android-only build edition

Built specifically to make JARVIS easier to compile and run directly on a Samsung Galaxy F23 5G using an on-device Android development environment.

## V5.1 changes
- Phone-friendly Gradle settings: lower memory pressure and limited workers.
- Conservative Android Gradle Plugin 8.6.1 / Gradle 8.7 pairing.
- Android API 35 target retained.
- Offline/basic assistant fallback when no AI backend is configured.
- Notification reading from the locally stored latest notification.
- Wake-phrase preference is now honored by the hands-free service.
- HTTPS-only backend policy (`usesCleartextTraffic=false`).
- Settings for backend URL, assistant name, wake phrase and sensitive-action confirmation.
- Existing local commands: YouTube, WhatsApp, Chrome, Google search, SMS composer, dialer and alarms.
- Local conversation memory with clear-memory control.

## Build on the phone
See `PHONE_BUILD.md`.

### Recommended toolchain
AndroidIDE + JDK 17 + Android SDK 35 + AGP 8.6.1 + Gradle 8.7.

Android's official compatibility documentation states AGP 8.6 supports API 35 and requires JDK 17; AGP 8.6 uses Gradle 8.7. 

## AI backend
JARVIS V5.1 deliberately does not embed a long-lived AI API key. Configure your own HTTPS backend in JARVIS Settings. The backend accepts:

POST `/v1/jarvis/respond`

```json
{"message":"...","memory":["..."],"notifications":[]}
```

and returns:

```json
{"reply":"..."}
```

Without a backend, local phone commands and basic offline replies remain available.
