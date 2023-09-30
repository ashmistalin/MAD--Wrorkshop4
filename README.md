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

![image](https://github.com/ashmistalin/MAD-workshop2/assets/103128410/c657f09f-2cdb-44b3-8419-68ff810648d6)
![image](https://github.com/ashmistalin/MAD-workshop2/assets/103128410/6a5f1c2d-9243-44bf-a3d8-646f47eeeaf1)
![image](https://github.com/ashmistalin/MAD-workshop2/assets/103128410/2706d183-85f9-4978-a1a2-dc22aca4a919)

