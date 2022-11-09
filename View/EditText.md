# EditText (Page 3-19)
## XML
Main
```XML
<EditText
  android:id="@+id/TextEdit"
  <!-- android:layout_{width,height}={"wrap_content","match_parent"} -->
  <!-- android:text="TextEdit" -->
  <!-- android:textSize="20sp" -->
  <!-- android:textColor="#000000" -->
  <!-- app:layout_margin{Start,End,Top,Bottom}="8dp" -->
  <!-- app:layout_constraint{Start,End,Top,Bottom}_to{Start,End,Top,Bottom}Of="@+id/component" -->
/>
```
Attributes (Page 3-20)
```
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
  private EditText TextEdit;
```
Link
```java
    TextEdit = (EditText) findViewById(R.id.TextEdit);
```
`addTextChangedListener`
```java
TextEdit.addTextChangedListener(new TextWatcher() 
  {
    @Override public void beforeTextChanged(CharSequence string, int start, int count, int after) {}
    @Override public void onTextChanged(CharSequence string, int start, int before, int count) {}
    @Override public void afterTextChanged(Editable string) {}
  });
```