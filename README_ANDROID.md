# FMSmedia Hub — Android build scaffold

This repository scaffold wraps the existing `index.html` website in a Capacitor Android app and builds a test APK using GitHub Actions.

## App identity
- App name: FMSmedia Hub
- Android package ID: `com.fmsmedia.hub`
- Website source: root `index.html`
- Web asset folder: generated `www/`

## GitHub phone setup
1. Open your repository: `https://github.com/FMSmediahub/Fmsmedia_hub`
2. Add these scaffold files/folders to the repository (upload files from this ZIP).
3. Keep your existing root `index.html`; do not overwrite it with a placeholder.
4. Commit the uploaded files to the `main` branch.
5. Open the repository's **Actions** tab.
6. Select **Build FMSmedia Hub Android** and wait for the run to finish green.
7. Open the completed workflow run, scroll to **Artifacts**, and download `FMSmedia-Hub-debug-APK`.
8. Extract the ZIP artifact and install `app-debug.apk` on your Android phone. Android may ask you to allow installing unknown apps for the browser/file manager you use.

## What this build is
This workflow creates a **debug APK for testing**. It is not a signed Play Store release. A Google Play release requires a release signing key and an Android App Bundle (`.aab`); we'll set that up separately and safely.

## Notes
- This is a starter scaffold, not a full native Android project committed to the repository.
- The workflow creates the Android project in GitHub Actions each time it runs.
- The website's assets and linked files should use relative paths and be committed to the repository.
- If your website uses external APIs, embeds, or remote links, test them in the app before release.
