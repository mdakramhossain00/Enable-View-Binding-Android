# Enable-View-Binding-Android
Enable View Binding Android
//build.gradle module:app 
android {
    ...
    viewBinding {
        enabled = true
    }
}

//Enable View Binding for Activities: xml file:

tools:viewBindingIgnore="false"
//MainActivity.java

import com.example.databinding.databinding.ActivityMainBinding;

public class MainActivity extends AppCompatActivity {
    private ActivityMainBinding binding;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        binding = ActivityMainBinding.inflate(getLayoutInflater());
        View view = binding.getRoot();
        setContentView(view);

        // Now, you can access views using `binding` (e.g., binding.textView.setText("Hello, View Binding!"))
    }
}
