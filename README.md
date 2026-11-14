# Echo (Capacitor, Android)

Requirements: Node 20+, Android Studio (with an SDK + emulator or a USB-debugging phone), JDK 21 (bundled with Android Studio).

## Build steps
1. `npm install`
2. `npx cap add android`      (creates the android/ folder, one time)
3. `npx cap sync android`     (run after every change to www/)
4. `npx cap open android`     (opens Android Studio)
5. In Android Studio press Run ▶ to test on a device/emulator.

## Make an installable APK
Android Studio → Build → Build Bundle(s) / APK(s) → Build APK(s).
For the Play Store: Build → Generate Signed Bundle (AAB).

## Before publishing
- Change `appId` in capacitor.config.json (e.g. com.yourname.echo) BEFORE step 2.
- Replace the launcher icon: Android Studio → right-click res → New → Image Asset.
- The game lives in www/index.html (single file, no build step). The extended word list (~37k words) is embedded in it.
