# Ex.No:1 To create a HelloWorld Activity using all lifecycles methods to display messages.


## AIM:

To create a HelloWorld Activity using all lifecycles methods to display messages using Android Studio.

## EQUIPMENTS REQUIRED:

Latest Version Android Studio

## ALGORITHM:

Step 1: Open Android Stdio and then click on File -> New -> New project.

Step 2: Then type the Application name as HelloWorld and click Next. 

Step 3: Then select the Minimum SDK as shown below and click Next.

Step 4: Then select the Empty Activity and click Next. Finally click Finish.

Step 5: Design layout in activity_main.xml.

Step 6: Display message give in MainActivity file.

Step 7: Save and run the application.

## PROGRAM:
```
/*
Program to print the text “Hello World”.
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
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">

    <TextView
        android:layout_width="250dp"
        android:layout_height="50dp"
        android:text="Hello World!"
        android:textSize="100px"
        android:textStyle="italic"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.591"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.499" />

</androidx.constraintlayout.widget.ConstraintLayout>
```
MainActivity.java:
```
package com.example.helloworld;

import androidx.appcompat.app.AppCompatActivity;
import android.os.Bundle;
import android.util.Log;
import android.widget.Toast;

public class MainActivity extends AppCompatActivity {

    private static final String TAG = "HelloWorldActivity";

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        Log.d(TAG, "onCreate: ");
        Toast.makeText(this, "onCreate", Toast.LENGTH_SHORT).show();
    }

    @Override
    protected void onStart() {
        super.onStart();
        Log.d(TAG, "onStart: ");
        Toast.makeText(this, "onStart", Toast.LENGTH_SHORT).show();
    }

    @Override
    protected void onResume() {
        super.onResume();
        Log.d(TAG, "onResume: ");
        Toast.makeText(this, "onResume", Toast.LENGTH_SHORT).show();
    }

    @Override
    protected void onPause() {
        super.onPause();
        Log.d(TAG, "onPause: ");
        Toast.makeText(this, "onPause", Toast.LENGTH_SHORT).show();
    }

    @Override
    protected void onStop() {
        super.onStop();
        Log.d(TAG, "onStop: ");
        Toast.makeText(this, "onStop", Toast.LENGTH_SHORT).show();
    }

    @Override
    protected void onDestroy() {
        super.onDestroy();
        Log.d(TAG, "onDestroy: ");
        Toast.makeText(this, "onDestroy", Toast.LENGTH_SHORT).show();
    }

    @Override
    protected void onRestart() {
        super.onRestart();
        Log.d(TAG, "onRestart: ");
        Toast.makeText(this, "onRestart", Toast.LENGTH_SHORT).show();
    }
}
```
## OUTPUT

<img src="https://github.com/hariharan0033/Mobile-Application-Development/assets/125666185/b32ed47c-f82e-4e53-8cb2-44fccfa5cd27" alt="LifeCycleMethod_1" width="20%" height="auto">

<img src="https://github.com/hariharan0033/Mobile-Application-Development/assets/125666185/7979d0cd-1762-4012-a599-6bf8842f29c7" alt="LifeCycleMethod_2" width="20%" height="auto">

<img src="https://github.com/hariharan0033/Mobile-Application-Development/assets/125666185/baa185e0-e033-4d3a-9bcd-ba6de7ca0f54" alt="LifeCycleMethod_3" width="20%" height="auto">

<img src="https://github.com/hariharan0033/Mobile-Application-Development/assets/125666185/b01a475b-4570-4ebd-8e99-817718c541b9" alt="LifeCycleMethod_4" width="20%" height="auto">

<img src="https://github.com/hariharan0033/Mobile-Application-Development/assets/125666185/7ec9fac4-af47-4094-9af0-55d9b9d32227" alt="LifeCycleMethod_5" width="20%" height="auto">

<img src="https://github.com/hariharan0033/Mobile-Application-Development/assets/125666185/bfda1577-9dee-464e-8b6a-ef864c55bcca" alt="LifeCycleMethod_6" width="20%" height="auto">

<img src="https://github.com/hariharan0033/Mobile-Application-Development/assets/125666185/3ad4b95a-46d7-482c-955f-5cb8adc424f7" alt="LifeCycleMethod_7" width="20%" height="auto">



## RESULT
Thus a Simple Android Application create a HelloWorld Activity using all lifecycles methods to display messages using Android Studio is developed and executed successfully.
