# Weather App

Weather app demonstrating API integration and geolocation.

## What's included
- Minimal React Native project structure
- `App.js` with placeholder UI
- `README` with setup and APK build instructions

## Quick start
1. Install dependencies (use Yarn or npm):

```bash
npm install
# or
# yarn install
```

2. Run Metro bundler:

```bash
npm run start
```

3. Run on Android (connected device or emulator):

```bash
npm run android
```

## Build APK (debug)
Make sure you have Android Studio and Android SDK installed.

From project root:

```bash
cd android
./gradlew assembleDebug
```

Debug APK path:

```
android/app/build/outputs/apk/debug/app-debug.apk
```

## Build APK (release)
1. Generate a signing key (if you don't have one):

```bash
keytool -genkey -v -keystore release-key.keystore -alias your-key-alias -keyalg RSA -keysize 2048 -validity 10000
```

2. Place `release-key.keystore` into `android/app` and add signing config to `android/app/build.gradle` (see React Native docs).

3. Build release:

```bash
cd android
./gradlew assembleRelease
```

Release APK path:

```
android/app/build/outputs/apk/release/app-release.apk
```

## GitHub repo
Create the repo and push:

```bash
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/akhilbhumar/weather-app.git
git push -u origin main
```

Replace placeholders (package name, app name) before publishing. For Play Store, prefer generating an AAB:

```bash
cd android
./gradlew bundleRelease
```

## Notes
- These templates are intentionally minimal. Add navigation, state management, and native modules as needed.
- For iOS builds you need Xcode and macOS.

---

If you want, I can generate sample components/screens for this app (e.g., task list, add task screen) and include screenshots in README.
