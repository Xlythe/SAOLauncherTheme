SAOLauncherTheme
================

Here are a collection of themes for SAO Launcher. Some open in Eclipse, others in Android Studio.

To get started, you will need either Eclipse or Android Studio. Google either "Android Studio" or "Eclipse ADT Bundle" and you'll find them. The themes that have files like .gradle need Android Studio. The ones without need Eclipse.

Open up (File -> Open) one of the themes to get started. Most of the images should be in (/app/src/main)/res/xxxhdpi. As long as you don't change the dimensions of the images, they should work fine.

For colors, like text color, look in /res/values/colors.xml.

For sounds, look in /res/raw

For fonts, look in /assets

To change the name of the theme, look in /res/values/strings.xml. You will also need to change the package name, which is a unique identifier for your app. The package name typically looks like com.xlythe.saolauncher.theme.XXXX. It appears in a few places, but in general you have to change it...

In AndroidManifest.xml

<manifest xmlns:android="http://schemas.android.com/apk/res/android"
    package="com.xlythe.saolauncher.theme.XXXX"

<provider
    android:name=".FileProvider"
    android:authorities="com.xlythe.saolauncher.theme.XXXX.FileProvider"

In /java or /src (Depends on Android Studio vs Eclipse)

The folders will look like /com/xlythe/saolauncher/theme/XXXX

The .java files, at the very top, "package com.xlythe.saolauncher.theme.XXXX"