SAOLauncherTheme
================

How to write a them

Download the [example app](https://github.com/Xlythe/SAOLauncherTheme) to get started. It's dead simple, a theme is nothing but images and sounds.

- Start by replacing the images in res/drawable-xxhdpi (without changing their names) with your own versions.
- Next, if you want custom sounds, replace the mp3 files in res/raw.
- Thirdly, if you want the settings to be dark you don't have to do anything, but to make them white again you'll have to remove the line &lt;string name="app_theme"&gt; in res/values/strings.xml and res/values-v11/strings.xml. Note, your app name is in res/values/strings.xml as well.
- Lastly, change the package name. To do that, open AndroidManifest.xml to edit the 3rd line (package=...) to whatever you'd like.

When your app is installed, it'll show up as an option in SAO Launcher.

For a more detailed look into how it works, the following Intent Filter is how SAO Launcher detects your theme. If the user selects it, then SAO will attempt to pull images from your app before pulling from its own. That means if there are any images you don't want to theme, just leave them out.
<code>
&lt;activity
    android:name="com.xlythe.saolauncher.theme.Stub"
    android:label="@string/app_name" &gt;
    &lt;intent-filter&gt;
        &lt;action android:name="com.xlythe.saolauncher.THEME" /&gt;
    &lt;/intent-filter&gt;
&lt;/activity&gt;
</code>
