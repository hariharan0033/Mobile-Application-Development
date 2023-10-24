# Ex.No:4 To create a two screens , first screen will take one number input from user. After click on Factorial button, second screen will open and it should display factorial of the same number using Explicit Intents.


## AIM:

To create a two screens , first screen will take one number input from user. After click on Factorial button, second screen will open and it should display factorial of the same number using Explicit Intents.


## EQUIPMENTS REQUIRED:

Latest Version Android Studio

## ALGORITHM:

1. Step 1: Open Android Stdio and then click on File -> New -> New project.
2. Step 2: Then type the Application name as implicit inetent and click Next.
3. Step 3: Then select the Minimum SDK as shown below and click Next.
4. Step 4: Then select the Empty Activity and click Next. Finally click Finish.
5. Step 5: Design layout in activity_main.xml.
6. Step 6: Display message give in MainActivity file.
7. Step 7: Save and run the application.
 

## PROGRAM:

```
/*
Program to print the text “ExplicitIntent”.
Developed by:HARIHARAN E
Registeration Number :212221040052
*/
```
## activity_main.xml:
```
<androidx.constraintlayout.widget.ConstraintLayout
xmlns:android="http://schemas.android.com/apk/res/android"
xmlns:app="http://schemas.android.com/apk/res-auto"
xmlns:tools="http://schemas.android.com/tools"
android:layout_width="match_parent"
android:layout_height="match_parent"
tools:context=".MainActivity">
<EditText
android:id="@+id/editTextTextPersonName"
android:layout_width="wrap_content"
android:layout_height="wrap_content"
android:layout_marginStart="60dp"
android:layout_marginTop="284dp"
android:ems="10"
android:inputType="textPersonName"
android:text=""
android:textSize="25sp"
app:layout_constraintStart_toStartOf="parent"
app:layout_constraintTop_toTopOf="parent" />
<Button
android:id="@+id/button"
android:layout_width="wrap_content"
android:layout_height="wrap_content"
android:layout_marginBottom="128dp"
android:onClick="Showdtag"
android:text="Factorial"
android:textSize="25sp"
app:layout_constraintBottom_toBottomOf="parent"
app:layout_constraintEnd_toEndOf="parent"
app:layout_constraintHorizontal_bias="0.506"
app:layout_constraintStart_toStartOf="parent"
app:layout_constraintTop_toBottomOf="@+id/editTextTextPersonName"
app:layout_constraintVertical_bias="0.831" />
</androidx.constraintlayout.widget.ConstraintLayout>
```
## MainActivty.java:
```
package com.example.myapplication;
import androidx.appcompat.app.AppCompatActivity;
import android.content.Intent;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.EditText;
public class MainActivity extends AppCompatActivity { EditText ed1; Button res;
<TextView
android:id="@+id/textView"
android:layout_width="wrap_content"
android:layout_height="wrap_content"
android:layout_marginBottom="52dp"
android:text="Enter a number:"
android:textSize="25sp"
app:layout_constraintBottom_toTopOf="@+id/editTextTextPersonName"
app:layout_constraintEnd_toEndOf="parent"
app:layout_constraintHorizontal_bias="0.497"
app:layout_constraintStart_toStartOf="parent" />
<TextView
android:id="@+id/textView4"
android:layout_width="wrap_content"
android:layout_height="wrap_content"
android:text="Factorial of a Number"
android:textSize="30sp"
app:layout_constraintBottom_toTopOf="@+id/textView"
app:layout_constraintEnd_toEndOf="parent"
app:layout_constraintHorizontal_bias="0.52"
app:layout_constraintStart_toStartOf="parent"
app:layout_constraintTop_toTopOf="parent"
app:layout_constraintVertical_bias="0.62" />
@Override
protected void onCreate(Bundle savedInstanceState) {
super.onCreate(savedInstanceState);
setContentView(R.layout.activity_main);
ed1 = findViewById(R.id.editTextTextPersonName);
}

```
## activity_main2.xml:
```
<androidx.constraintlayout.widget.ConstraintLayout
xmlns:android="http://schemas.android.com/apk/res/android"
res = findViewById(R.id.button);
res.setOnClickListener(new View.OnClickListener() {
@Override
public void onClick(View view) {
int num = Integer.parseInt(ed1.getText().toString());
int factorial = calculateFactorial(num);
Intent intent = new Intent(getApplicationContext(),
MainActivity2.class);
intent.putExtra("key", factorial);
startActivity(intent);
}
});
}
private int calculateFactorial(int number) {
int factorial = 1;
for (int i = 1; i <= number; i++) {
factorial *= i;
}
return factorial;
}
xmlns:app="http://schemas.android.com/apk/res-auto"
xmlns:tools="http://schemas.android.com/tools"
android:layout_width="match_parent"
android:layout_height="match_parent"
tools:context=".MainActivity2">
<TextView
android:id="@+id/textView3"
android:layout_width="wrap_content"
android:layout_height="wrap_content"
android:text=""
android:textSize="40dp"
app:layout_constraintBottom_toBottomOf="parent"
app:layout_constraintEnd_toEndOf="parent"
app:layout_constraintHorizontal_bias="0.464"
app:layout_constraintStart_toStartOf="parent"
app:layout_constraintTop_toTopOf="parent" />
<TextView
android:id="@+id/textView5"
android:layout_width="wrap_content"
android:layout_height="wrap_content"
android:text="Result:"
android:textSize="40dp"
app:layout_constraintBottom_toTopOf="@+id/textView3"
app:layout_constraintEnd_toEndOf="parent"
app:layout_constraintHorizontal_bias="0.465"
app:layout_constraintStart_toStartOf="parent"
app:layout_constraintTop_toTopOf="parent"
app:layout_constraintVertical_bias="0.825" />
</androidx.constraintlayout.widget.ConstraintLayout>
```
## MainActivty2.java:
```
package com.example.myapplication;
import androidx.appcompat.app.AppCompatActivity;
import android.content.Intent; import android.os.Bundle; import android.widget.TextView;
public class MainActivity2 extends AppCompatActivity { TextView getdata;
@Override
protected void onCreate(Bundle savedInstanceState) {
super.onCreate(savedInstanceState);
setContentView(R.layout.activity_main2);
getdata = findViewById(R.id.textView3);
Intent intent = getIntent();
int data = intent.getIntExtra("key",0);
getdata.setText(Integer.toString(data));
}

}
```

## OUTPUT
![Ex4-1](https://github.com/suryacse05/Mobile-Application-Development/assets/103128410/f47b0d4a-d362-4c60-9529-ccb65e8e65ae)
![ex4-2](https://github.com/suryacse05/Mobile-Application-Development/assets/103128410/f90bac81-362b-42ea-86a8-74fa14b3ae6b)




## RESULT
Thus a Simple Android Application create a Explicit Intents using Android Studio is developed and executed successfully.
