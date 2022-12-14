# AppBarLayout.Toolbar.Menu (Page 8-9)
## XML
Main
```XML
<com.google.android.material.appbar.AppBarLayout
  android:layout_width="match_parent"
  android:layout_height="wrap_content"
  android:theme="@style/ThemeOverlay.AppCompat.Dark.ActionBar"
  app:layout_constraintTop_toTopOf="parent"
>
  <androidx.appcompat.widget.Toolbar
    android:id="@+id/toolbar"
    android:layout_width="match_parent"
    android:layout_height="?attr/actionBarSize"
    android:background="?attr/colorPrimary"
    app:popupTheme="@style/ThemeOverlay.AppCompat.Light"
  />
</com.google.android.material.appbar.AppBarLayout>
```
<!-- add in `res/value/styles.xml` `<resources></resources>`
```XML
<style name="AppTheme.AppBarOverlay" parent="ThemeOverlay.AppCompat.Dark.ActionBar" />
<style name="AppTheme.PopupOverlay" parent="ThemeOverlay.AppCompat.Light" />
``` -->
---
> refer: https://stackoverflow.com/questions/41586347/do-not-request-window-feature-support-action-bar

add in `res/value/themes.xml` `<resources><style></style></resources>`
```XML
<item name="windowActionBar">false</item>
<item name="windowNoTitle">true</item>
```
for ERROR
```log
E/AndroidRuntime: FATAL EXCEPTION: main
    Process: ${PackageName}, PID: 22921
    java.lang.RuntimeException: Unable to start activity ComponentInfo{${PackageName}/${PackageName}.MainActivity}:  
        java.lang.IllegalStateException: This Activity already has an action bar supplied by the window decor. Do not request Window.FEATURE_SUPPORT_ACTION_BAR and set windowActionBar to false in your theme to use a Toolbar instead.
    Caused by: 
        java.lang.IllegalStateException: This Activity already has an action bar supplied by the window decor. Do not request Window.FEATURE_SUPPORT_ACTION_BAR and set windowActionBar to false in your theme to use a Toolbar instead.
```
add in `res/value/themes.xml` `<resources></resources>`
```XML
  <style name="Theme.${app_name}.NoActionBar">
    <item name="windowActionBar">false</item>
    <item name="windowNoTitle">true</item>
  </style>
```
add in `manifests/AndroidManifest.xml` `<manifest><application><activity></activity></application></manifest>` Attributes
```XML
android:theme="@style/Theme.${app_name}.NoActionBar"
```
for ERROR
```log
E/AndroidRuntime: FATAL EXCEPTION: main
    Process: ${PackageName}, PID: 22921
    java.lang.RuntimeException: Unable to start activity ComponentInfo{${PackageName}/${PackageName}.MainActivity}:  
        java.lang.IllegalStateException: This Activity already has an action bar supplied by the window decor. Do not request Window.FEATURE_SUPPORT_ACTION_BAR and set windowActionBar to false in your theme to use a Toolbar instead.
    Caused by: 
        java.lang.IllegalStateException: This Activity already has an action bar supplied by the window decor. Do not request Window.FEATURE_SUPPORT_ACTION_BAR and set windowActionBar to false in your theme to use a Toolbar instead.
```
## Java
<!-- `import`
```Java
import androidx.appcompat.app.AppCompatActivity;
``` -->
<!-- Declear
```java
public class MainActivity extends AppCompatActivity 
  {
    @Override protected void onCreate(Bundle savedInstanceState) {}
    @Override public boolean onCreateOptionsMenu(Menu menu) {}
    @Override public boolean onOptionsItemSelected(MenuItem item) {}
  }
``` -->
<!-- Link
```java
``` -->
set in `onCreate()`
```java
setContentView(R.layout.activity_main);
setSupportActionBar(findViewById(R.id.toolbar));
```
`onCreateOptionsMenu()`
```java
@Override public boolean onCreateOptionsMenu(Menu menu) 
  {
    // Inflate the menu; this adds items to the action bar if it is present.
    getMenuInflater().inflate(R.menu.menu_main, menu);
    return true;
  }
```
`setOnClickListener()`
```java
@Override public boolean onOptionsItemSelected(MenuItem item) 
  {
    // Handle action bar item clicks here. The action bar will automatically handle clicks on the Home/Up button, 
    // so long as you specify a parent activity in AndroidManifest.xml.
    int id = item.getItemId();
    Log.d("menu", "onOptionsItemSelected");
    //noinspection SimplifiableIfStatement
    if (id == R.id.action_settings) 
      return true;
    return super.onOptionsItemSelected(item);
  }
```
