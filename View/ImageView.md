# ImageView (Page 6-7) (Ch06_ex1)
## XML
Main
```XML
<ImageView
  android:id="@+id/ViewImage"
  <!-- android:layout_{width,height}={"wrap_content","match_parent"} -->
  <!-- android:src="@drawable/Image" -->
  <!-- android:scaleType="fitCenter" -->
  <!-- app:layout_margin{Start,End,Top,Bottom}="8dp" -->
  <!-- app:layout_constraint{Start,End,Top,Bottom}_to{Start,End,Top,Bottom}Of="@+id/component" -->
/>
```
## Java
`import`
```Java
import android.widget.ImageView;
```
Declear
```java
private ImageView ViewImage ;
```
Link
```java
ViewImage = (ImageView) findViewById(R.id.ViewImage);
```
`void setImageResource()`
```java
ViewImage.setImageResource(R.drawable.Image);
```