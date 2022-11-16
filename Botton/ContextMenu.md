# ContextMenu (Page 8-17)
## XML
<!-- Main
```XML
``` -->
## Java
`import`
```Java
import android.view.View;
import android.view.MenuItem;
import android.view.ContextMenu;
```
Link 
```java
registerForContextMenu(View);
```
`onCreateContextMenu`
```java
@Override public void onCreateContextMenu(ContextMenu menu, View view, ContextMenu.ContextMenuInfo menuInfo) 
  {
    super.onCreateContextMenu(menu, view, menuInfo);
    // ...
  }
```
`onContextItemSelected`
```java
@Override public boolean onContextItemSelected(MenuItem item)
  {
    // ...
    return super.onContextItemSelected(item);
  }
```
