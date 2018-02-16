<h1>Introduction</h1>

INTUZ is presenting a Audio Trimmer component, which lets you trim your audio files on the fly in Android. You can record your audio and get start to trim!
Please follow below steps to integrate this control in your next project.

<br>
<h1>Features</h1>
- Ability to record your audio and trim it.
- Ability to play selected range of audio before trimming.
- After trimming if you don’t like the audio then you can get the original file again by pressing “Reset”.


<br>
<img src="Screenshots/audiotrimmer_.gif" width=500 alt="Screenshots/audio_trimmer.png">

<h1>Getting Started</h1>

> Permission and declaration in AndroidManifest.xml file

```
    <uses-permission android:name="android.permission.RECORD_AUDIO" />
    <uses-permission android:name="android.permission.WRITE_EXTERNAL_STORAGE" />
    <uses-permission android:name="android.permission.READ_EXTERNAL_STORAGE" />
```
> Declare AudioTrimmerActivity with transparent theme

```
    <activity
            android:name=".AudioTrimmerActivity"
            android:screenOrientation="portrait"
            android:theme="@style/Theme.Transparent" />
```

> Declare transparent style in styles.xml

```
    <style name="Theme.Transparent" parent="Theme.AppCompat.Light.NoActionBar">
        <item name="android:windowIsTranslucent">true</item>
        <item name="android:windowBackground">@android:color/transparent</item>
        <item name="android:windowContentOverlay">@null</item>
        <item name="android:windowNoTitle">true</item>
        <item name="android:windowIsFloating">false</item>
        <item name="android:backgroundDimEnabled">false</item>
    </style>
```

> Start AudioTrimmerActivity with startActivityForResult :

```
    startActivityForResult(new Intent(MainActivity.this, AudioTrimmerActivity.class), 1);

```

> Handle your onActivityResult for getting trimmed Audio Path:

```
    if (requestCode == 1) {
        if (resultCode == RESULT_OK) {
            if (data != null) {
                String path = data.getExtras().getString("INTENT_AUDIO_FILE");
                
            }
        }
    }
```

> To change displayed colors

```
   Change declared colors in colors.xml
```
> To modify layout of trimmer

```
    Modify activity_audio_trim.xml file
```

<h1>Bugs and Feedback</h1>

For bugs, questions and discussions please use the Github Issues.

<br>
<h1>License</h1>

Copyright (c) 2018 Intuz Solutions Pvt Ltd.
<br><br>
Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:
<br><br>
THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

<h1></h1>
<a href="http://www.intuz.com">
<img src="Screenshots/logo.jpg">
</a>
