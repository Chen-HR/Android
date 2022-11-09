# ListView (Page 7-2) (Ch07)
## XML
Main
```XML
<ListView
  android:id="@+id/ViewList"
  <!-- android:layout_{width,height}={"wrap_content","match_parent"} -->
  <!-- android:layout_margin{Start,End,Top,Bottom}="10dp" -->
  <!-- android:{horizontalSpacing,verticalSpacing}="10dp" -->
  <!-- android:numColumns="3" -->
  <!-- android:padding="10dp" -->
  <!-- app:layout_margin{Start,End,Top,Bottom}="8dp" -->
  <!-- app:layout_constraint{Start,End,Top,Bottom}_to{Start,End,Top,Bottom}Of="@+id/component" -->
/>
```
## Java
`import`
```Java
import android.view.View;
import android.widget.ListView;
import android.widget.AdapterView;
import android.widget.ArrayAdapter;
```
Declear
```java
private ListView ViewList;
```
Link
```java
ViewList= (ListView) findViewById(R.id.ViewList);
```
`set`
```java
ViewList.setAdapter(new ArrayAdapter<String>(this,android.R.layout.simple_list_item_1,Items));
ViewList.setOnItemClickListener(new ListView.OnItemClickListener()
  {
    @Override public void onItemClick(AdapterView<?> parent, View view, int position, long id){}
  });
ViewList.setSelector(R.color.green);
```