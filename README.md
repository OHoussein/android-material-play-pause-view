`MaterialPlayPauseView` that toggle play/pause with material animation




###**Usage Sample**

in layout xml
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

In Activity
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
Copyright 2016 OHoussein

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.