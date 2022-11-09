# GridView (Page 6-14) (Ch06_ex2)
## XML
Main
```XML
<GridView
  android:id="@+id/ViewGrid"
  <!-- android:layout_{width,height}={"wrap_content","match_parent"} -->
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
import android.view.ViewGroup;
import android.widget.AdapterView;
import android.widget.BaseAdapter;
```
Declear
```java
private GridView  ViewGrid;
```
Link
```java
ViewGrid = (GridView) findViewById(R.id.ViewGrid);
```
`set`
```java
ViewGrid.setAdapter(new Adapter(this));
ViewGrid.setOnItemClickListener(new AdapterView.OnItemClickListener() 
  {
    @Override public void onItemClick(AdapterView<?> parent, View view, int position, long id) {}
  });
class Adapter extends BaseAdapter 
  {
    private Context context;
    public Adapter(Context context) {context=c;}
    @Override public int getCount() {return length;}
    @Override public Object getItem(int position) {return position;}
    @Override public long getItemId(int position) {return position;}
    @Override public View getView(int position, View convertView, ViewGroup parent) {return view;}
  }
```