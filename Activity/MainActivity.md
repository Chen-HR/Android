# MainActivity
## XML
```XML
<LayoutLable
  tools:context=".MainActivity"
>
```
## Java
`import`
```Java
import androidx.appcompat.app.AppCompatActivity;
import android.os.Bundle;
```
`MainActivity`
```Java
public class MainActivity extends AppCompatActivity {
  @Override
  protected void onCreate(Bundle savedInstanceState) {
    super.onCreate(savedInstanceState);
    setContentView(R.layout.activity_main);
    setTitle("Title");
  }
}
```
