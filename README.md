# Php
Php important questions 
MAD Practical exam questions.






1.	Write a program to place Name, Age, Mobile number linearly(vertical) on the display screen using Linear layout 
Xml Code:
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:gravity="center_horizontal"
    tools:context=".MainActivity">

    <TextView
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Name: John Doe" />

    <TextView
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Age: 30" />

    <TextView
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Mobile: 1234567890" />

</LinearLayout>           
                                      
2.	Write a program to place Name, Age, Mobile number linearly(vertical) on the display screen using Absolute layout.
Xml Code:
<?xml version="1.0" encoding="utf-8"?>
<AbsoluteLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent">

    <TextView
        android:id="@+id/nameTextView"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Name: John Doe"
        android:layout_x="20dp"
        android:layout_y="20dp" />

    <TextView
        android:id="@+id/ageTextView"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Age: 30"
        android:layout_x="20dp"
        android:layout_y="60dp" />

    <TextView
        android:id="@+id/mobileTextView"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Mobile: 1234567890"
        android:layout_x="20dp"
        android:layout_y="100dp" />

</AbsoluteLayout>

3.	Write a program to display 5 students basic information in a table form using Table layout.
Xml code
     <?xml version="1.0" encoding="utf-8"?>
<TableLayout
xmlns:android="http://schemas.android.com/apk/res/android" android:layout_width="match_parent" android:layout_height="match_parent">
<TableLayout
android:layout_width="match_parent" android:layout_height="wrap_content">

<!-- Header row -->
<TableRow>
<TextView
android:text="Name" android:layout_weight="1"/>
<TextView
android:text="Age" android:layout_weight="1"/>
<TextView
android:text="Gender" android:layout_weight="1"/>
<TextView
android:text="Grade" android:layout_weight="1"/>
<TextView
android:text="Address" android:layout_weight="2"/>
</TableRow>

<!-- Student rows -->
<TableRow>
<TextView
android:text="Dhiraj" android:layout_weight="1"/>
<TextView
android:text="20" android:layout_weight="1"/>
 
<TextView
android:text="Male" android:layout_weight="1"/>
<TextView
android:text="12th" android:layout_weight="1"/>
<TextView
android:text="123 Main St, Anytown, USA" android:layout_weight="2"/>
</TableRow>

<TableRow>
<TextView
android:text="Hiren" android:layout_weight="1"/>
<TextView
android:text="19" android:layout_weight="1"/>
<TextView
android:text="Male" android:layout_weight="1"/>
<TextView
android:text="11th" android:layout_weight="1"/>
<TextView
android:text="456 Oak St, Anytown, USA" android:layout_weight="2"/>
</TableRow>

<TableRow>
<TextView
android:text="Pragati" android:layout_weight="1"/>
<TextView
android:text="18" android:layout_weight="1"/>
<TextView
android:text="Female" android:layout_weight="1"/>
<TextView
android:text="10th" android:layout_weight="1"/>
<TextView
android:text="789 Maple St, Anytown, USA" android:layout_weight="2"/>
</TableRow>

<TableRow>
<TextView
android:text="Abhijjet" android:layout_weight="1"/>
<TextView
android:text="21" android:layout_weight="1"/>
<TextView
android:text="Male" android:layout_weight="1"/>
<TextView
android:text="12th" android:layout_weight="1"/>
<TextView
android:text="246 Elm St, Anytown, USA" android:layout_weight="2"/>
</TableRow>

<TableRow>
<TextView
 
android:text="Sarth" android:layout_weight="1"/>
<TextView
android:text="19" android:layout_weight="1"/>
<TextView
android:text="Male" android:layout_weight="1"/>
<TextView
android:text="11th" android:layout_weight="1"/>
<TextView
android:text="135 Pine St, Anytown, USA" android:layout_weight="2"/>
</TableRow>

</TableLayout>

</TableLayout>

4.	Write a program to accept username and password from the end user using Text View and edit Text.
Xml Code:
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:padding="16dp"
    tools:context=".MainActivity">

    <TextView
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Username:" />

    <EditText
        android:id="@+id/usernameEditText"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:hint="Enter your username" />

    <TextView
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Password:" />

    <EditText
        android:id="@+id/passwordEditText"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:hint="Enter your password"
        android:inputType="textPassword" />

    <Button
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Login"
        android:onClick="onLoginClick" />

</LinearLayout>

Java code:

import android.os.Bundle;
import android.view.View;
import android.widget.EditText;
import android.widget.Toast;

import androidx.appcompat.app.AppCompatActivity;

public class MainActivity extends AppCompatActivity {

    private EditText usernameEditText, passwordEditText;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        // Initialize EditText views
        usernameEditText = findViewById(R.id.usernameEditText);
        passwordEditText = findViewById(R.id.passwordEditText);
    }

    public void onLoginClick(View view) {
        String username = usernameEditText.getText().toString().trim();
        String password = passwordEditText.getText().toString().trim();

        // Perform your login logic here
        // For this example, we'll display a toast with the entered username and password
        String message = "Username: " + username + "\nPassword: " + password;
        Toast.makeText(this, message, Toast.LENGTH_SHORT).show();
    }
}










5.	Write a program to create a toggle button to display ON/OFF Bluetooth on the display screen.
Xml Code:
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
              android:layout_width="match_parent"
              android:layout_height="match_parent"
              android:orientation="vertical"
              android:padding="16dp">

    <TextView
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="Bluetooth"/>

    <ToggleButton
            android:id="@+id/toggleButton"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:textOff="OFF"
            android:textOn="ON"/>
</LinearLayout>

Java code:

import android.bluetooth.BluetoothAdapter;
import android.os.Bundle;
import android.widget.CompoundButton;
import android.widget.Toast;
import android.widget.ToggleButton;

import androidx.appcompat.app.AppCompatActivity;

public class MainActivity extends AppCompatActivity {
    private BluetoothAdapter bluetoothAdapter;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        bluetoothAdapter = BluetoothAdapter.getDefaultAdapter();

        if (bluetoothAdapter == null) {
            Toast.makeText(this, "Bluetooth not supported", Toast.LENGTH_SHORT).show();
            finish();
        }

        ToggleButton toggleButton = findViewById(R.id.toggleButton);

        toggleButton.setOnCheckedChangeListener(new CompoundButton.OnCheckedChangeListener() {
            @Override
            public void onCheckedChanged(CompoundButton compoundButton, boolean isChecked) {
                if (isChecked) {
                    // Turn on Bluetooth
                    if (!bluetoothAdapter.isEnabled()) {
                        bluetoothAdapter.enable();
                        Toast.makeText(MainActivity.this, "Bluetooth turned ON", Toast.LENGTH_SHORT).show();
                    }
                } else {
                    // Turn off Bluetooth
                    if (bluetoothAdapter.isEnabled()) {
                        bluetoothAdapter.disable();
                        Toast.makeText(MainActivity.this, "Bluetooth turned OFF", Toast.LENGTH_SHORT).show();
                    }
                }
            }
        });
    }
}






6.	Write a program to create a login form for a social networking site
Xml code 
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android" android:orientation="vertical"
android:layout_width="match_parent" android:layout_height="match_parent">

<EditText
android:id="@+id/username" android:layout_width="match_parent" android:layout_height="wrap_content" android:hint="Username"/>

<EditText
android:id="@+id/password" android:layout_width="match_parent" android:layout_height="wrap_content" android:hint="Password" android:inputType="textPassword"/>

<Button
android:id="@+id/login_button" android:layout_width="match_parent" android:layout_height="wrap_content" android:text="Log In"/>

</LinearLayout>

Java Code
import android.os.Bundle; 
import android.view.View;
import android.widget.Button; 
import android.widget.EditText; 
import android.widget.Toast;
import androidx.appcompat.app.AppCompatActivity;
import java.util.HashMap;
public class LoginActivity extends AppCompatActivity {
private EditText mUsername; private EditText mPassword; private Button mLoginButton;

// Define a HashMap of username and password combinations
private HashMap<String, String> userCredentials = new HashMap<String, String>() {{
put("user1", "password1");
put("user2", "password2");
put("user3", "password3");
}};

@Override
protected void onCreate(Bundle savedInstanceState) { super.onCreate(savedInstanceState); setContentView(R.layout.activity_main);

mUsername = findViewById(R.id.username); mPassword = findViewById(R.id.password); mLoginButton = findViewById(R.id.login_button);

mLoginButton.setOnClickListener(new View.OnClickListener() { @Override
public void onClick(View v) {
String username = mUsername.getText().toString(); String password = mPassword.getText().toString();

// Check if the username and password combination is valid
if (userCredentials.containsKey(username) && userCredentials.get(username).equals(password)) {
// If the login is successful, show a toast message
Toast.makeText(LoginActivity.this, "Login successful!", Toast.LENGTH_SHORT).show();
} else {
// If the login is unsuccessful, show a toast message
Toast.makeText(LoginActivity.this, "Invalid username or password", Toast.LENGTH_SHORT).show();
}
}
});
}
}

7.	Write a program to show five checkboxes and toast selected checkbox.
Xml Code:
<LinearLayout
    xmlns:android="http://schemas.android.com/apk/res/android"
    android:orientation="vertical"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:padding="16dp">

    <CheckBox
        android:id="@+id/checkBox1"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Checkbox 1" />

    <CheckBox
        android:id="@+id/checkBox2"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Checkbox 2" />

    <CheckBox
        android:id="@+id/checkBox3"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Checkbox 3" />

    <CheckBox
        android:id="@+id/checkBox4"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Checkbox 4" />

    <CheckBox
        android:id="@+id/checkBox5"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Checkbox 5" />

    <Button
        android:id="@+id/submitButton"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="Submit" />

</LinearLayout>
Java code:

import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.CheckBox;
import android.widget.Toast;

import androidx.appcompat.app.AppCompatActivity;

public class MainActivity extends AppCompatActivity {

    private CheckBox checkBox1, checkBox2, checkBox3, checkBox4, checkBox5;
    private Button submitButton;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        checkBox1 = findViewById(R.id.checkBox1);
        checkBox2 = findViewById(R.id.checkBox2);
        checkBox3 = findViewById(R.id.checkBox3);
        checkBox4 = findViewById(R.id.checkBox4);
        checkBox5 = findViewById(R.id.checkBox5);
        submitButton = findViewById(R.id.submitButton);

        submitButton.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                StringBuilder selectedCheckBoxes = new StringBuilder();
                if (checkBox1.isChecked()) {
                    selectedCheckBoxes.append("Checkbox 1\n");
                }
                if (checkBox2.isChecked()) {
                    selectedCheckBoxes.append("Checkbox 2\n");
                }
                if (checkBox3.isChecked()) {
                    selectedCheckBoxes.append("Checkbox 3\n");
                }
                if (checkBox4.isChecked()) {
                    selectedCheckBoxes.append("Checkbox 4\n");
                }
                if (checkBox5.isChecked()) {
                    selectedCheckBoxes.append("Checkbox 5\n");
                }

                if (selectedCheckBoxes.length() > 0) {
                    // Display the selected checkboxes in a toast message
                    Toast.makeText(MainActivity.this, "Selected checkboxes:\n" + selectedCheckBoxes.toString(), Toast.LENGTH_LONG).show();
                } else {
                    Toast.makeText(MainActivity.this, "No checkbox selected", Toast.LENGTH_SHORT).show();
                }
            }
        });
    }
}




8.	Write a program to display circular progress bar.
Xml Code:
<?xml version="1.0" encoding="utf-8"?>
<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:padding="16dp"
    tools:context=".MainActivity">

    <ProgressBar
        android:id="@+id/progressBar"
        style="?android:attr/progressBarStyleLarge"
        android:layout_width="100dp"
        android:layout_height="100dp"
        android:layout_centerInParent="true" />

</RelativeLayout>



Java code:
import android.os.Bundle;
import android.os.Handler;
import android.view.View;
import android.widget.ProgressBar;

import androidx.appcompat.app.AppCompatActivity;

public class MainActivity extends AppCompatActivity {

    private ProgressBar progressBar;
    private Handler handler;
    private int progressStatus;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        // Initialize ProgressBar view
        progressBar = findViewById(R.id.progressBar);

        handler = new Handler();
    }

    public void onStartProgressClick(View view) {
        progressStatus = 0;

        // Show the progress bar
        progressBar.setVisibility(View.VISIBLE);

        // Reset the progress to 0
        progressBar.setProgress(progressStatus);

        // Start the progress in a separate thread
        new Thread(() -> {
            while (progressStatus < 100) {
                progressStatus += 1;

                // Update the progress bar
                handler.post(() -> progressBar.setProgress(progressStatus));

                try {
                    // Add a delay to simulate progress
                    Thread.sleep(50);
                } catch (InterruptedException e) {
                    e.printStackTrace();
                }
            }

            // Hide the progress bar when progress is complete
            handler.post(() -> progressBar.setVisibility(View.GONE));
        }).start();
    }
}




9.	Write a program to display 15 buttons using Grid view.
Xml Code:
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:padding="16dp"
    tools:context=".MainActivity">

    <GridView
        android:id="@+id/gridView"
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        android:numColumns="3"
        android:verticalSpacing="16dp"
        android:horizontalSpacing="16dp" />

</LinearLayout>

Java code:

import android.os.Bundle;
import android.view.View;
import android.widget.AdapterView;
import android.widget.ArrayAdapter;
import android.widget.Button;
import android.widget.GridView;
import android.widget.Toast;

import androidx.appcompat.app.AppCompatActivity;

public class MainActivity extends AppCompatActivity {

    private GridView gridView;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        // Initialize GridView
        gridView = findViewById(R.id.gridView);

        // Create an array of button labels
        String[] buttonLabels = new String[15];
        for (int i = 0; i < 15; i++) {
            buttonLabels[i] = "Button " + (i + 1);
        }

        // Create an ArrayAdapter to populate the GridView with buttons
        ArrayAdapter<String> adapter = new ArrayAdapter<>(this, android.R.layout.simple_list_item_1, buttonLabels);

        // Set the adapter on the GridView
        gridView.setAdapter(adapter);

        // Set item click listener on the GridView
        gridView.setOnItemClickListener(new AdapterView.OnItemClickListener() {
            @Override
            public void onItemClick(AdapterView<?> parent, View view, int position, long id) {
                String buttonLabel = adapter.getItem(position);
                Toast.makeText(MainActivity.this, "Clicked " + buttonLabel, Toast.LENGTH_SHORT).show();
            }
        });
    }
}

10.	Write a program to display a toast message.
Xml Code:
<?xml version="1.0" encoding="utf-8"?>
<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:padding="16dp"
    tools:context=".MainActivity">

    <Button
        android:id="@+id/toastButton"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Show Toast"
        android:layout_centerInParent="true" />

</RelativeLayout>

Java code:

import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.Toast;

import androidx.appcompat.app.AppCompatActivity;

public class MainActivity extends AppCompatActivity {

    private Button toastButton;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        // Initialize Button view
        toastButton = findViewById(R.id.toastButton);

        // Set click listener on the button
        toastButton.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                // Show a toast message
                Toast.makeText(MainActivity.this, "Hello, Toast!", Toast.LENGTH_SHORT).show();
            }
        });
    }
}
