ConvertTo 1080p Dolby Digital
===

```shell
ffmpeg -hwaccel_device 0 -hwaccel cuda 
-i "input.mp4" 
-vf scale=-1:1080 -c:v hevc_nvenc -preset fast
-ac 6 -map 0 -c:a ac3 
"FHD_60FPS_DD_output.mp4"
```
