# MAD-workshop4

## Design a simple application to display/play the video in android activity or view using raw folder.

## AIM:
To design a simple application to display/play the video in android activity or view using raw folder.



## PROGRAM:
```
/*
Submitted by: ASHMI S
Register number: 212221040021
*/
```
## activity_main.xml:
```
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout
    xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:padding="50dp"

    tools:context=".MainActivity">

    <TextView
        android:id="@+id/textView"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="BEAUTY OF THE BUTTERFLIES"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.126" />

    <VideoView
        android:id="@+id/videoView"
        android:layout_width="285dp"
        android:layout_height="410dp"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/textView" />

</androidx.constraintlayout.widget.ConstraintLayout>
```

## MainActivity.java:
```
package com.example.workshop4;


import androidx.appcompat.app.AppCompatActivity;
import android.net.Uri;
import android.os.Bundle;
import android.widget.MediaController;
import android.widget.VideoView;
public class MainActivity extends AppCompatActivity
{ @Override
protected void onCreate(Bundle savedInstanceState)
{ super.onCreate(savedInstanceState);
    setContentView(R.layout.activity_main);
    VideoView videoView = findViewById(R.id.videoView);
    MediaController mediaController = new MediaController(this);
    mediaController.setAnchorView(videoView); videoView.setMediaController(mediaController);
    videoView.setVideoURI(Uri.parse("android.resource://" + getPackageName() + "/" + R.raw.butterfly));
    videoView.start();
}
}

```

## OUTPUT:

![Screenshot (380)](https://github.com/ashmistalin/MAD--Wrorkshop4/assets/103128410/9e3ca2fe-57ca-4e28-82c7-1d61e76a7283)
![Screenshot (379)](https://github.com/ashmistalin/MAD--Wrorkshop4/assets/103128410/96b7d06d-7b35-480d-b578-2a02b28ee9e2)

## RESULT:
Thus designing a simple application to display/play the video in android activity or view using raw folder is completed.

