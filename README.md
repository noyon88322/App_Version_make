## Make App Version Screen

.xml

   ```bash



    <com.facebook.shimmer.ShimmerFrameLayout
        android:id="@+id/shimmer_view_container"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"


        app:layout_constraintEnd_toEndOf="@+id/circleImageView2"
        app:layout_constraintStart_toStartOf="@+id/circleImageView2"
        app:layout_constraintTop_toBottomOf="@+id/circleImageView2">

        <TextView
            android:id="@+id/tv_about_name"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_marginTop="16dp"
            android:text="Earning App"
            android:fontFamily="@font/roboto_bold"
            android:textColor="@color/white"

            android:textSize="@dimen/_30ssp"
            android:textStyle="bold" />


    </com.facebook.shimmer.ShimmerFrameLayout>


   ```

   ## java

java

   ```bash

package com.example.watchandearn;

import androidx.appcompat.app.AppCompatActivity;

import android.os.Build;
import android.os.Bundle;
import android.widget.TextView;

import com.karumi.dexter.BuildConfig;

public class About extends AppCompatActivity {

    private TextView tv_about_name;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_about);

        tv_about_name = findViewById(R.id.tv_about_name);

        String versonName = BuildConfig.VERSION_NAME;
        int versonCode = BuildConfig.VERSION_CODE;
        String version = "Version "+versonName+"."+versonCode;
        tv_about_name.setText(version);


    }
}

   ```
