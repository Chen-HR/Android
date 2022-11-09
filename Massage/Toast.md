# Toast (Page 4-8)
## XML
none
## Java
`import`
```Java
import android.widget.Toast;
```
Declear
```java
private Toast MassageToast = Toast.makeText(MainActivity.this, "MassageToast", Toast.LENGTH_LONG);
```
`.makeText().show()`
```java
Toast toast = Toast.makeText(MainActivity.this, "Testing Toast", Toast.LENGTH_LONG);
toast.show();
```
```java
((Toast) Toast.makeText(MainActivity.this, "Testing Toast", Toast.LENGTH_LONG)).show();
```
```java
Toast.makeText(MainActivity.this, "Testing Toast", Toast.LENGTH_LONG).show();
```