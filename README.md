# AWS Flashcards Android App

This Android Studio project wraps the provided AWS flashcard HTML in a native Android WebView app.

## Run locally

1. Open this folder in Android Studio.
2. Let Android Studio sync Gradle.
3. Connect your Samsung Galaxy S24 or start an emulator.
4. Click **Run**.

## Build APK locally

Android Studio: **Build > Build Bundle(s) / APK(s) > Build APK(s)**.

CLI, after Gradle is installed/configured:

```bash
gradle assembleDebug
```

The APK will be at:

```text
app/build/outputs/apk/debug/app-debug.apk
```

## Build with GitHub Actions

This repo includes `.github/workflows/android-build.yml`.

After pushing to GitHub:

1. Open the repo on GitHub.
2. Go to **Actions**.
3. Select **Build Android APK**.
4. Run the workflow manually, or push to `main`/`master`.
5. Download the APK from the workflow run under **Artifacts**: `AWSFlashcards-debug-apk`.

## Notes

- The app is portrait-first and responsive for small, medium, and tablet screens.
- The flashcard data remains embedded in `app/src/main/assets/index.html`, so the main deck works offline.
- Internet permission is included only for any future external assets or API calls.
- The GitHub workflow builds a debug APK. For Play Store release, add signing configuration and build a release APK or AAB.
