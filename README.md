# Incomplete-Android-studio
This will contain the codings that are presently there for the front end

Main login activity XML

<?xml version="1.0" encoding="utf-8"?>
<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:background="@drawable/background"
    tools:context=".MainActivity">

    <TextView
        android:id="@+id/signin"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="Sign In"
        android:textColor="@color/white"
        android:textSize="35dp"
        android:textStyle="bold"
        android:layout_margin="50dp"
        android:gravity="center" />

    <EditText
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:id="@+id/username"
        android:hint="Username"
        android:textColor="@color/white"
        android:textColorHint="@color/white"
        android:background="#25ffffff"
        android:layout_below="@+id/signin"
        android:layout_margin="10dp"
        android:padding="20dp"
        android:drawableLeft="@drawable/ic_baseline_person_outline_24"
        android:drawablePadding="20dp" />

    <EditText
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:id="@+id/password"
        android:hint="Password"
        android:textColor="@color/white"
        android:textColorHint="@color/white"
        android:background="#25ffffff"
        android:layout_below="@+id/username"
        android:layout_margin="10dp"
        android:padding="20dp"
        android:drawableLeft="@drawable/ic_baseline_lock_24"
        android:drawablePadding="20dp" />

    <Button
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:id="@+id/loginbtn"
        android:layout_below="@id/password"
        android:text="LOGIN"
        android:backgroundTint="@color/purple_200"
        android:layout_centerHorizontal="true"
        android:layout_margin="21dp"
        />




</RelativeLayout>




Java Coding

package com.example.kaofficiallogin;

import androidx.appcompat.app.AppCompatActivity;

import android.content.Intent;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.TextView;
import android.widget.Toast;

import com.google.android.material.button.MaterialButton;

public class MainActivity extends AppCompatActivity {

    private Button loginbtn;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        TextView username = (TextView) findViewById(R.id.username);
        TextView password = (TextView) findViewById(R.id.password);



        Button loginbtn = (Button) findViewById(R.id.loginbtn);
        loginbtn.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                openNavigateActivity();
            }
        });
        //admin and admin


    }

    public void openNavigateActivity() {
        Intent intent = new Intent(this, NavigateActivity.class);
        startActivity(intent);


    }
}
