# Android APK

The project is packaged with Capacitor. The APK is built automatically by GitHub Actions for pushes to `main` and `arena/**`, or can be started with **Actions → Build Android APK → Run workflow**.

Download `chronicles-of-eldoria-debug-apk` from the completed workflow run, then install `app-debug.apk` on an Android device. Android may ask to allow installation from the browser or file manager.

To build locally with Node.js 22, Java 21, and Android SDK installed:

```sh
npm ci
npm run android:sync
cd android
./gradlew assembleDebug
```

The resulting APK is `android/app/build/outputs/apk/debug/app-debug.apk`. This is a debug APK for testing and direct installation; a Play Store release requires a separately signed release build.
