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
## Java
<!-- `import`
```Java
import androidx.appcompat.app.AppCompatActivity;
``` -->
Declear
```java
public class MainActivity extends AppCompatActivity 
  {
    @Override protected void onCreate(Bundle savedInstanceState) {}
    @Override public boolean onCreateOptionsMenu(Menu menu) {}
    @Override public boolean onOptionsItemSelected(MenuItem item) {}
  }
```
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
`setOnClickListener`
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
