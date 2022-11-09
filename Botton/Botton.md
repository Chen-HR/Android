# Botton (Page 3-25)
## XML
Main
```XML
<Botton
  android:id="@+id/Botton_Botton"
  <!-- android:layout_{width,height}={"wrap_content","match_parent"} -->
  <!-- android:text="Botton_Botton" -->
  <!-- android:textSize="20sp" -->
  <!-- android:textColor="#000000" -->
  <!-- app:layout_margin{Start,End,Top,Bottom}="8dp" -->
  <!-- app:layout_constraint{Start,End,Top,Bottom}_to{Start,End,Top,Bottom}Of="@+id/component" -->
/>
```
## Java
`import`
```Java
import android.widget.Button;
```
Declear
```java
private Botton Botton_Botton;
```
Link
```java
Botton_Botton = (Botton) findViewById(R.id.Botton_Botton);
```
`setOnClickListener`
```java
Botton_Botton.setOnClickListener(Listener);
private Button.OnClickListener Listener = new Button.OnClickListener() 
  {
    @Override public void onClick(View view) {}
  };
```
```java
Botton_Botton.setOnClickListener(new Button.OnClickListener() 
  {
    @Override public void onClick(View view) {}
  });
```
```java
Botton_Botton.setOnClickListener((View view)->{});
```