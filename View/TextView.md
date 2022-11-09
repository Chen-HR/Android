# TextView (Page 3-11)
## XML
Main
```XML
<TextView
  android:id="@+id/ViewText"
  <!-- android:layout_{width,height}={"wrap_content","match_parent"} -->
  <!-- android:text="TextView" -->
  <!-- android:textSize="20sp" -->
  <!-- android:textColor="#000000" -->
  <!-- app:layout_margin{Start,End,Top,Bottom}="8dp" -->
  <!-- app:layout_constraint{Start,End,Top,Bottom}_to{Start,End,Top,Bottom}Of="@+id/component" -->
/>
```
## Java
`import`
```Java
import android.widget.EditText;
import android.text.TextWatcher;
import android.text.Editable;
```
Declear
```java
private TextView ViewText;
```
Link
```java
ViewText = (TextView) findViewById(R.id.ViewText);
```
`setText`
```java
ViewText.setText("ViewText");
```