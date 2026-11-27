SAOLauncherTheme
================

Here are a collection of themes for SAO Launcher.

To get started, install Gradle 9.9.2 and Android SDK 37. Open up (File -> Open) the repository root in Android Studio. Run `gradle assembleDebug` to build all seven themes.

Most of the images should be in `res/drawable-xxxhdpi` or `app/src/main/res/drawable-xxxhdpi`. As long as you don't change the dimensions of the images, they should work fine.

For colors, like text color, look in /res/values/colors.xml.

For sounds, look in /res/raw

For fonts, look in /assets

To change the name of the theme, look in /res/values/strings.xml. If you are creating a new theme, choose a unique package name for your app. The package name typically looks like com.xlythe.saolauncher.theme.XXXX.

Set `applicationId` in the theme module's `build.gradle`. ThemeEngine registers its file provider automatically using the `${applicationId}.FileProvider` authority.

If you also rename the Java package, update the module's `namespace`, the package declarations and folders under `src` or `app/src/main/java`, and any fully qualified activity names in AndroidManifest.xml.
