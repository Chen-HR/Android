# ActivityMainBinding 
## XML
<!-- Main
```XML
``` -->
none
## Java
`import` while:
```Java
package ${package_name};
```
`import` then:
```Java
import ${package_name}.databinding.ActivityMainBinding;
```
Declear
```java
private ActivityMainBinding binding;
```
Link
```java
binding = ActivityMainBinding.inflate(getLayoutInflater());
```
in `onCreate()`
```java
//  setContentView(R.layout.activity_main);
    setContentView(binding.getRoot());
//  setSupportActionBar(findViewById(R.id.toolbar));
    setSupportActionBar(binding.toolbar);
```
using in `setOnClickListener`
```java
//  findViewById(R.id.fab).setOnClickListener(new View.OnClickListener() 
//    {@Override public void onClick(View view) {}});
    binding.fab.setOnClickListener(new View.OnClickListener() 
      {@Override public void onClick(View view) {}});
```