# Build JARVIS V5.1 from your Android phone (no PC)

The easiest phone-only method is GitHub Actions. GitHub's hosted runner provides the Linux machine, JDK, Android SDK and Gradle; your Galaxy only needs a browser.

## What you need
- A GitHub account
- The JARVIS V5.1 project files
- Chrome/Samsung Internet on your phone

## Method A — upload the project to a GitHub repository
1. Create a new GitHub repository.
2. Upload the contents of this `JARVIS_V5` folder, including `.github/workflows/build-apk.yml`.
3. Open the repository's **Actions** tab.
4. Select **Build JARVIS APK**.
5. Tap **Run workflow**.
6. Wait for the green check.
7. Open the completed workflow run and scroll to **Artifacts**.
8. Download `JARVIS-V5.1-debug-apk` to your phone.
9. Extract the artifact ZIP and install the APK.

## If GitHub's mobile upload UI makes folders difficult
Use GitHub in Chrome with **Desktop site** enabled. Upload the project files while preserving their paths.

## Important
- Do not upload an OpenAI API key into the repository.
- The workflow builds a debug APK; it is suitable for testing on your phone.
- The workflow uses JDK 17, Android API 35, build-tools 35.0.0 and Gradle 8.7.
