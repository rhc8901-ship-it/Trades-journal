RC Trading Journal - Android APK rebuild patch

Upload/replace these files in the ROOT of your existing GitHub repository:
- index.html
- package.json
- capacitor.config.json
- voice-bridge-entry.js
- assets/icon.png
- .github/workflows/build-apk.yml

Keep your existing manifest.json, sw.js, icon-192.png and icon-512.png in the repository root.

Then open GitHub Actions > Build RC Android APK > Run workflow.
The workflow now always includes the native speech-recognition plugin and creates Android launcher icon resources from assets/icon.png.
Download the RC-Trading-Journal-APK artifact and extract app-debug.apk.

IMPORTANT:
- This is a DEBUG APK for personal testing, not a Play Store release.
- The new APK has the same application ID: com.rohanchauhan.tradesjournal.
- Install it over the existing app if Android allows the update. Do not uninstall the old app first, because uninstalling may erase locally stored journal data. If Android reports a signature conflict, export/backup your app data before uninstalling the old build.
- Voice recognition requires an Android speech-recognition provider (commonly Google app / Speech Services) and an active internet connection may be required depending on the provider and language.
