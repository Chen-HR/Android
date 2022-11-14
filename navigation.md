# navigation 
## XML
<!-- Main
```XML
``` -->
none
## Java
`import`
```Java
import androidx.navigation.NavController;
import androidx.navigation.Navigation;
import androidx.navigation.ui.AppBarConfiguration;
import androidx.navigation.ui.NavigationUI;
```
Declear
```java
private AppBarConfiguration appBarConfiguration;
```
Link
```java
NavController navController = Navigation.findNavController(this, R.id.nav_host_fragment_content_main);
appBarConfiguration = new AppBarConfiguration.Builder(navController.getGraph()).build();
NavigationUI.setupActionBarWithNavController(this, navController, appBarConfiguration);
```
`onSupportNavigateUp()`
```java
@Override public boolean onSupportNavigateUp() 
  {
    NavController navController = Navigation.findNavController(this, R.id.nav_host_fragment_content_main);
    return NavigationUI.navigateUp(navController, appBarConfiguration) || super.onSupportNavigateUp();
  }
```