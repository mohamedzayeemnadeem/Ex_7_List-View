## Ex.No:7 Develop an android application to display the programming languages with toast message using list view in android studio.

## AIM:
To create and develop the application to display the place name with image using list view in android studio

## EQUIPMENTS REQUIRED:
Android Studio(Latest Version)

## ALGORITHM:
## Step 1:Open Android Stdio and then click on File -> New -> New project.

Step 2: Then type the Application name as “listview″ and click Next.

Step 3: Then select the Minimum SDK as shown below and click Next.

Step 4: Then select the Empty Activity and click Next. Finally click Finish.

Step 5: Design layout in activity_main.xml.

Step 6: Get contacts details and Display details give in MainActivity file.

Step 7: Save and run the application.

## PROGRAM:
/*
Program to print the list of item.
Developed by:mohamed zayeem nadeem
Registeration Number :21222222040102
*/

## activity_main.xml:
```
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout
    xmlns:android="http://schemas.android.com/apk/res/android"
    android:orientation="vertical"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:padding="16dp">

    <ListView
        android:id="@+id/listView"
        android:layout_width="match_parent"
        android:layout_height="match_parent" />
</LinearLayout>

```

##MainActivity.java:
```
package com.example.listapp;

import android.os.Bundle;
import android.view.View;
import android.widget.AdapterView;
import android.widget.ArrayAdapter;
import android.widget.ListView;
import android.widget.Toast;
import androidx.appcompat.app.AppCompatActivity;

public class MainActivity extends AppCompatActivity {

    ListView listView;
    String[] languages = {
            "Python",
            "Java",
            "C",
            "C++",
            "SQL",
            "JavaScript",
            "Kotlin",
            "Swift",
            "Ruby",
            "Go",
            "PHP",
            "C#",
            "Dart",
            "TypeScript",
            "Perl",
            "R",
            "Scala",
            "Rust"
    };

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        listView = findViewById(R.id.listView);

        ArrayAdapter<String> adapter = new ArrayAdapter<>(this, android.R.layout.simple_list_item_1, languages);
        listView.setAdapter(adapter);

        // Set onItemClickListener to display Toast
        listView.setOnItemClickListener(new AdapterView.OnItemClickListener() {
            @Override
            public void onItemClick(AdapterView<?> parent, View view, int position, long id) {
                String selectedLanguage = languages[position];
                Toast.makeText(MainActivity.this, "Selected: " + selectedLanguage, Toast.LENGTH_SHORT).show();
            }
        });
    }
}
```
## OUTPUT
![Screenshot 2025-04-26 134321](https://github.com/user-attachments/assets/0e0f9508-ed60-4559-87b2-aaecbff3634d)

![Screenshot 2025-04-26 134327](https://github.com/user-attachments/assets/3805ee3b-0330-4a8c-a031-718ca458528b)


![Screenshot 2025-04-26 134341](https://github.com/user-attachments/assets/df068ea1-9732-4c86-ad3b-4118c8a0134f)


## RESULT
Thus a Simple Android Application to create and develop the application to display the programming languages with toast message using list view in android studio is developed and executed successfully.

