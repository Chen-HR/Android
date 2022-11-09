# RadioGroup (Page 5-15) (Ch05_ex2)
## XML
Main
```XML
<RadioGroup
  android:id="@+id/Botton_RadioGroup"
  <!-- android:layout_{width,height}={"wrap_content","match_parent"} -->
  <!-- app:layout_margin{Start,End,Top,Bottom}="8dp" -->
  <!-- app:layout_constraint{Start,End,Top,Bottom}_to{Start,End,Top,Bottom}Of="@+id/component" -->
>
  <RadioButton
    android:id="@+id/Button_RadioButton"
    <!-- android:layout_{width,height}={"wrap_content","match_parent"} -->
    <!-- android:text="O" -->
    <!-- android:textSize="24sp" -->
    <!-- android:textColor="#0000FF"  -->
  />
<RadioGroup>
```
## Java
`import`
```Java
import android.widget.RadioGroup;
import android.widget.RadioButton;
```
Declear
```java
private RadioGroup  Botton_RadioGroup ;
private RadioButton Button_RadioButton;
```
Link
```java
Botton_RadioGroup  = (RadioGroup ) findViewById(R.id.Botton_RadioGroup );
Button_RadioButton = (RadioButton) findViewById(R.id.Button_RadioButton);
```
`setOnCheckedChangeListener`
```java
RadGup_blood.setOnCheckedChangeListener(Listener);
private RadioGroup.OnCheckedChangeListener Listener = new RadioGroup.OnCheckedChangeListener() 
  {
    @Override public void onCheckedChanged(CompoundButton buttonView, boolean isChecked) {}
  };
```
```java
RadGup_blood.setOnCheckedChangeListener(new RadioGroup.OnCheckedChangeListener()
  {
    @Override public void onCheckedChanged(RadioGroup group, int checkedId) {}
  });
```
```java
RadGup_blood.setOnCheckedChangeListener((RadioGroup group, int checkedId)->{});
```