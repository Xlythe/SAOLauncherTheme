# SAO Launcher themes

Open the repository root in Android Studio with Android SDK 37 installed. Build all seven themes with `./gradlew assembleDebug`, or select one module, for example `./gradlew :SAOAwesomeTheme:assembleDebug`. Each module produces an independently installable APK.

To customize a theme, edit its existing resources. Images live in the drawable density directories, colors in `res/values/colors.xml`, sounds in `res/raw` and fonts in `assets` or `res/font`. Keep drawable dimensions and nine-patch borders intact when replacing artwork. The older projects use `res` directly, while others use `app/src/main/res`.

For a new theme, choose a unique `applicationId` in its module's `build.gradle` and update the name in `res/values/strings.xml`. Keep the launcher theme intent filter and application metadata. Themes with a file provider use ThemeEngine's provider and the authority `${applicationId}.FileProvider`, which Gradle expands when it builds the APK. Install the APK and select it in the launcher's theme settings.
