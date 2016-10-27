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