# FloatingActionButton 
## XML
Main
```XML
<com.google.android.material.floatingactionbutton.FloatingActionButton
  android:id="@+id/fab"
  android:layout_width="wrap_content"
  android:layout_height="wrap_content"
  android:layout_gravity="bottom|end"
  android:layout_marginEnd="@dimen/fab_margin"
  android:layout_marginBottom="16dp"
  app:srcCompat="@android:drawable/ic_dialog_email"
/>
```
## Java
`import`
```Java
import com.google.android.material.floatingactionbutton.FloatingActionButton;
```
Declear
```java
FloatingActionButton fab;
```
Link
```java
fab = (FloatingActionButton) findViewById(R.id.fab);
```
`setOnClickListener`
```java
fab.setOnClickListener(new View.OnClickListener() 
  {
    @Override public void onClick(View view) {}
  });
```