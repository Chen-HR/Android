# Spinner (Page 5-25) (Ch05_ex3)
## XML
Main
```XML
<Spinner
  android:id="@+id/Botton_Spinner"
  <!-- android:layout_{width,height}={"wrap_content","match_parent"} -->
  <!-- android:background="#FFFFFF" -->
  <!-- app:layout_margin{Start,End,Top,Bottom}="8dp" -->
  <!-- app:layout_constraint{Start,End,Top,Bottom}_to{Start,End,Top,Bottom}Of="@+id/component" -->
/>
```
## Java
`import`
```Java
import android.view.View;
import android.widget.Spinner;
import android.widget.AdapterView;
import android.widget.ArrayAdapter;
```
Declear
```java
private Spinner  Botton_Spinner;
```
Link
```java
Botton_Spinner = (Spinner) findViewById(R.id.Botton_Spinner);
```
`setOnCheckedChangeListener`
```java
ArrayAdapter<CharSequence> Adapter = ArrayAdapter.createFromResource(MainActivity.this, R.array.Name,android.R.layout.simple_spinner_item);
                           Adapter.setDropDownViewResource(android.R.layout.simple_spinner_dropdown_item);
Botton_Spinner.setAdapter(Adapter);
Botton_Spinner.setOnItemSelectedListener(spnPreferListener);
private Spinner.OnItemSelectedListener spnPreferListener = new Spinner.OnItemSelectedListener() 
  {
    @Override public void onNothingSelected(AdapterView<?> parent) {}
    @Override public void onItemSelected(AdapterView<?> parent, View v, int position, long id) {}
  };
```
```java
ArrayAdapter<CharSequence> Adapter = ArrayAdapter.createFromResource(MainActivity.this, R.array.Name,android.R.layout.simple_spinner_item);
                           Adapter.setDropDownViewResource(android.R.layout.simple_spinner_dropdown_item);
Botton_Spinner.setAdapter(Adapter);
Botton_Spinner.setOnItemSelectedListener(spnPreferListener);
Botton_Spinner.setOnItemSelectedListener(new Spinner.OnItemSelectedListener() 
  {
    @Override public void onNothingSelected(AdapterView<?> parent) {}
    @Override public void onItemSelected(AdapterView<?> parent, View view, int position, long id) {}
  });
```