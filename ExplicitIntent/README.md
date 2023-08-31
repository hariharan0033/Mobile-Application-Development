# Ex.No:4 To create a two screens , first screen will take one number input from user. After click on Factorial button, second screen will open and it should display factorial of the same number using Explicit Intents.


## AIM:

To create a two screens , first screen will take one number input from user. After click on Factorial button, second screen will open and it should display factorial of the same number using Explicit Intents.


## EQUIPMENTS REQUIRED:

Latest Version Android Studio

## ALGORITHM:



## PROGRAM:
```
/*
Program to print the text “ExplicitIntent”.
Developed by: HARIHARAN E
Registeration Number : 212221040052
*/
```

activity_main.xml:
```
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:id="@+id/constraintLayout"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">

    <TextView
        android:id="@+id/textView"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="DIVIDER"
        android:textColor="#C2185B"
        android:textSize="50sp"
        android:textStyle="bold"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.194" />

    <TextView
        android:id="@+id/firstNumberLabel1"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Enter the first number:"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintEnd_toEndOf="parent" />
    <EditText
        android:id="@+id/etNumber1"
        android:layout_width="230dp"
        android:layout_height="67dp"
        android:ems="10"
        android:inputType="number"
        android:hint="E.g., 123"
        app:layout_constraintBottom_toTopOf="@+id/etNumber2"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.497"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/textView"
        app:layout_constraintVertical_bias="0.659" />

    <TextView
        android:id="@+id/firstNumberLabel2"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Enter the first number:"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintEnd_toEndOf="parent" />
    <EditText
        android:id="@+id/etNumber2"
        android:layout_width="236dp"
        android:layout_height="64dp"
        android:ems="10"
        android:inputType="number"
        android:hint="E.g., 123"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.497"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/textView"
        app:layout_constraintVertical_bias="0.387" />

    <Button
        android:id="@+id/button"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Divide"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/etNumber2"
        app:layout_constraintVertical_bias="0.257" />

</androidx.constraintlayout.widget.ConstraintLayout>
```

MainActivity.java:
```
package com.example.explicitindent;

import androidx.appcompat.app.AppCompatActivity;
import android.os.Bundle;
import android.content.Intent;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.EditText;
import android.widget.TextView;
public class MainActivity extends AppCompatActivity {
    private EditText firstNumberEditText, secondNumberEditText;
    private Button calculateButton;
    private TextView resultTextView;
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        firstNumberEditText = findViewById(R.id.etNumber1);
        secondNumberEditText = findViewById(R.id.etNumber2);
        calculateButton = findViewById(R.id.button);
        resultTextView = findViewById(R.id.Result); // Assuming you meant to find a TextView

        calculateButton.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                String firstNumberString =
                        firstNumberEditText.getText().toString();
                String secondNumberString =
                        secondNumberEditText.getText().toString();
                double firstNumber = Double.parseDouble(firstNumberString);
                double secondNumber =Double.parseDouble(secondNumberString);
                double result = firstNumber / secondNumber;
                Intent intent = new Intent(MainActivity.this,
                        MainActivity2.class);
                intent.putExtra("result", result);
                startActivity(intent);
            }
        });
    }
}
```
activity_main2.xml:

```
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:background="@color/white"
    tools:context=".MainActivity2">

    <TextView
        android:id="@+id/Result"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:scrollbarAlwaysDrawVerticalTrack="true"
        android:text="Result"
        android:textColor="#C2185B"
        android:textSize="48sp"
        android:textStyle="bold"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.499" />
</androidx.constraintlayout.widget.ConstraintLayout>
```
MainActivity2.java:
```
package com.example.explicitindent;

import androidx.appcompat.app.AppCompatActivity;
import android.content.Intent;
import android.os.Bundle;
import android.widget.TextView;
public class MainActivity2 extends AppCompatActivity {
    private TextView resultTextView;
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main2);
        resultTextView = findViewById(R.id.Result);
        Intent intent = getIntent();
        if (intent != null) {
            double result = intent.getDoubleExtra("result", 0);
            resultTextView.setText("Result: " + result);
        } else {
            resultTextView.setText("Result: Not Available");
        }

    }}
```
## OUTPUT






## RESULT
Thus a Simple Android Application create a Explicit Intents using Android Studio is developed and executed successfully.


