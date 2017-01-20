[![JitPack](https://jitpack.io/v/rosenpin/android-material-play-pause-view.svg)](https://jitpack.io/#rosenpin/android-material-play-pause-view)

Add this to your project build.gradle
```	gradle
allprojects {
		repositories {
			...
			maven { url 'https://jitpack.io' }
		}
}
```
 
 Add this to your module build.gradle
 ```gradle
dependencies {
    compile 'com.github.rosenpin:android-material-play-pause-view:1.1'
}
 ```


`MaterialPlayPauseView` that toggle play/pause with material animation

This an improvements of the [Alex Lockwood's PlayPauseView](https://github.com/alexjlockwood/material-pause-play-animation).
It add this features:
* Possibility to specify the view's size and colors
* Save Instance State
* Toggle/change state with or without animation

<div  align="center">    
<img src="https://raw.githubusercontent.com/OHoussein/android-material-play-pause-view/master/media/demo.gif" alt="demo" align=center />
</div>
 

###**Usage Sample**

####Gradle
compile 'com.github.ohoussein.playpauseview:playpauseview:1.0.0'

#### layout
```xml
    <com.ohoussein.playpause.PlayPauseView
        android:id="@+id/play_pause_view"
        android:layout_width="200dp"
        android:layout_height="200dp"
        android:clickable="true"
        android:foreground="?android:selectableItemBackground"
        app:fill_color="#e1e1e1"
        app:pause_bg="#00a2ed"
        app:play_bg="#001eff" />
```

* pause_bg : the background for the pause status
* play_bg : the background for the play status
* fill_color: the icon's color

#### Java
```java
        PlayPauseView view = (PlayPauseView) findViewById(R.id.play_pause_view);
        view.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                view.toggle();
            }
        });

```

You can use also `PlayPauseView#change(boolean isPlay)` to change play/pause with animation

#License

The MIT License (MIT)

Copyright 2016 OHoussein

Copyright (c) 2015 Alex Lockwood

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
