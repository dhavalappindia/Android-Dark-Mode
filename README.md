<b>add below line in your Manifest file</b>
<application android:configChanges="uiMode">


<b>add below code in your main luncher activity file</b>

/*----------------------------for dark mode support---------------------------------------*/

        int currentNightMode =  Configuration.UI_MODE_NIGHT_MASK;
        switch (currentNightMode) {
            case Configuration.UI_MODE_NIGHT_NO:
                // Night mode is not active, we're using the light theme
                AppCompatDelegate.setDefaultNightMode(AppCompatDelegate.MODE_NIGHT_NO); //For night mode theme

                break;
            case Configuration.UI_MODE_NIGHT_YES:
                // Night mode is active, we're using dark theme
                AppCompatDelegate.setDefaultNightMode(AppCompatDelegate.MODE_NIGHT_YES); //For night mode theme

                break;
        }
        
        
        
<b>add below code lines in your style.xml file</b>

     <style name="AppTheme" parent="Theme.AppCompat.DayNight">
    
        <!-- Customize your theme here. -->
        <item name="colorPrimary">@color/colorPrimary</item>
        <item name="colorPrimaryDark">@color/colorPrimaryDark</item>
        <item name="colorAccent">@color/colorAccent</item>
        <!--<item name="android:statusBarColor">@color/colorPrimaryDark</item>-->
        <!--<item name="android:navigationBarColor">@color/white</item>-->
        <!--<item name="android:windowLightStatusBar">true</item>-->
    </style>
    
    
<b>create new directory in res values-night and create colors.xml file</b>
    <resources>
      <color name="colorPrimary">#FF9D00</color>
      <color name="colorPrimaryDark">#FF8E00</color>
      <color name="colorAccent">#FF9D00</color>
    </resources>
