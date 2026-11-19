# Happy Elephant — Android starter project

A native Kotlin Android starter for the Happy Elephant property catalogue.

## Included
- Four UI languages: Russian, Ukrainian, Bulgarian and English.
- Device-language detection on first launch, with a manual language selector.
- Sale/rent filtering and text search.
- Local favourites.
- Admin area: first launch asks you to create a PIN (minimum 6 digits); afterwards it gates add/delete listing actions.
- Euro price display and a dark-green/gold visual direction.

## Build an APK
1. Install Android Studio (current stable) on a computer.
2. Open this folder in Android Studio.
3. Allow Android Studio to install the Android SDK platform 35 and the matching build tools if prompted.
4. Select **Build → Build Bundle(s) / APK(s) → Build APK(s)**.
5. Android Studio will show the generated APK location, usually `app/build/outputs/apk/debug/app-debug.apk`.

This source archive does not contain a prebuilt APK or Gradle wrapper. The project has not been compiled or device-tested in this environment.

## Important limitations before publishing
- Listings, favourites and the admin PIN are stored locally on one device. There is no cloud database, cross-device sync, image upload, or remote admin website yet.
- The local PIN screen is a basic device-side gate, **not production-grade authentication**. For a public app, move admin authentication and listing management to a secure backend (for example Firebase or your own API), store passwords as salted hashes on the server, and apply authorization rules there.
- WhatsApp and Telegram buttons are placeholders. Add your official phone number and channel URLs before release.
- Do not put real customer data or confidential credentials in this starter project.

## Package
`com.happyelephant.app`

## Cloud APK build (GitHub Actions)

This project includes `.github/workflows/build-apk.yml`. After the project is uploaded to a GitHub repository:
1. Open the repository on GitHub.
2. Choose **Actions** and run **Build Happy Elephant APK** (or push to `main`).
3. When the workflow finishes successfully, open its run and download the artifact named `happy-elephant-debug-apk`.
4. Inside the downloaded ZIP is `app-debug.apk`.

You will need a GitHub account and one initial upload of the project. The workflow automates compilation; it does not publish the app to Google Play. This workflow has been added to the source archive but has not been executed or verified in this environment.
