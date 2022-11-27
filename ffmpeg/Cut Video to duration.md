Cut Video to duration
===
```shell
ffmpeg -hide_banner -hwaccel_device 0 -hwaccel cuda 
-ss 00:14:00.0 
-i input.mp4 -c copy -t 00:24:00.0 input_cut.mp4
```
