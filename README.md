SAOLauncherTheme
================

          <h2 class="featurette-heading">How to write a theme</h2>
          <p class="lead">Download the <a href="https://github.com/Xlythe/SAOLauncherTheme">example app</a> to get started. It's dead simple, a theme is nothing but images and sounds.</p>
          <ul>
              <li>Start by replacing the images in res/drawable-xxhdpi (without changing their names) with your own versions.</li>
              <li>Next, if you want custom sounds, replace the mp3 files in res/raw.</li>
              <li>Thirdly, if you want the settings to be dark you don't have to do anything, but to make them white again you'll have to remove the line &lt;string name="app_theme"&gt; in res/values/strings.xml and res/values-v11/strings.xml. Note, your app name is in res/values/strings.xml as well.</li>
              <li>Lastly, change the package name. To do that, open AndroidManifest.xml to edit the 3rd line (package=...) to whatever you'd like.</li>
          </ul>
          <p class="lead">When your app is installed, it'll show up as an option in SAO Launcher.</p>
          <p class="lead">For a more detailed look into how it works, the following Intent Filter is how SAO Launcher detects your theme. If the user selects it, then SAO will attempt to pull images from your app before pulling from its own. That means if there are any images you don't want to theme, just leave them out.</p>
          <pre>
              <code>
&lt;activity
    android:name="com.xlythe.saolauncher.theme.Stub"
    android:label="@string/app_name" &gt;
    &lt;intent-filter&gt;
        &lt;action android:name="com.xlythe.saolauncher.THEME" /&gt;
    &lt;/intent-filter&gt;
&lt;/activity&gt;
              </code>
          </pre>
