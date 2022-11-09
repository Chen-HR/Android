# AlertDialog (Page 4-15)
## XML
none
## Java
`import`
```Java
import android.content.DialogInterface;
import android.app.AlertDialog;
```
Declear
```java
private AlertDialog.Builder MassageAlertDialog = AlertDialog.Builder(MainActivity.this);
```
`.makeText().show()`
```java
private AlertDialog.Builder MassageAlertDialog = AlertDialog.Builder(MainActivity.this);
MassageAlertDialog.setTitle("Confirmation window");
MassageAlertDialog.setIcon(R.mipmap.ic_launcher);
MassageAlertDialog.setMessage("You clicked botton \""+(((Button)findViewById(view.getId())).getText().toString())+"\"");
MassageAlertDialog.setPositiveButton("Confirm", new DialogInterface.OnClickListener() {});
MassageAlertDialog.setNegativeButton("Cancel" , new DialogInterface.OnClickListener() {});
MassageAlertDialog.show();
```
```java
new MassageAlertDialog.Builder(MainActivity.this)
                      .setTitle("MassageAlertDialog Title")
                      .setIcon(R.mipmap.ic_launcher)
                      .setMessage("MassageAlertDialog Message")
                      .setPositiveButton("Confirm", new DialogInterface.OnClickListener() {})
                      .setNegativeButton("Cancel" , new DialogInterface.OnClickListener() {})
                      .show();
```