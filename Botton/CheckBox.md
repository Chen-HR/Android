# CheckBox (Page 3-25) (Ch05_ex1)
## XML
Main
```XML
<CheckBox
  android:id="@+id/Botton_CheckBox"
  <!-- android:layout_{width,height}={"wrap_content","match_parent"} -->
  <!-- android:text="Botton_CheckBox" -->
  <!-- android:textSize="20sp" -->
  <!-- android:textColor="#000000" -->
  <!-- app:layout_margin{Start,End,Top,Bottom}="8dp" -->
  <!-- app:layout_constraint{Start,End,Top,Bottom}_to{Start,End,Top,Bottom}Of="@+id/component" -->
/>
```
## Java
`import`
```Java
import android.widget.CheckBox;
import android.widget.CompoundButton;
```
Declear
```java
private CheckBox Botton_CheckBox;
```
Link
```java
Botton_CheckBox = (CheckBox) findViewById(R.id.Botton_CheckBox);
```
`bool isChecked()`
```java
Botton_CheckBox.isChecked()
```
`setOnCheckedChangeListener`
```java
Botton_CheckBox.setOnCheckedChangeListener(Listener);
private CheckBox.setOnCheckedChangeListener Listener = new CheckBox.setOnCheckedChangeListener() 
  {
    @Override public void onCheckedChanged(CompoundButton buttonView, boolean isChecked) {}
  };
```
```java
Botton_CheckBox.setOnCheckedChangeListener(new CheckBox.setOnCheckedChangeListener() 
  {
    @Override public void onCheckedChanged(CompoundButton buttonView, boolean isChecked) {}
  });
```
```java
Botton_CheckBox.setOnCheckedChangeListener((CompoundButton buttonView, boolean isChecked)->{});
```