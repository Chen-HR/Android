# Snackbar 
- refer to: [Ken@www.uuu.com.tw: Snackbar replaces Toast](https://www.uuu.com.tw/Public/content/article/17/171127tips.htm)
## XML
none
## Java
`import`
```Java
import com.google.android.material.snackbar.Snackbar;
```
<!-- Declear
```java
``` -->
`.makeText()`
```java
Snackbar.make(contentView, "Snackbar content", Snackbar.LENGTH_LONG);
```
`setAction()`
```java
Snackbar.setAction("OK", new View.OnClickListener() 
          {
            @Override public void onClick(View view) {}
          })
```
`.show()`
```java
Snackbar.show();
```