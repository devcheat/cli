ConvertTo 60fps
===

```shell
ffmpeg -hide_banner -hwaccel_device 0 -hwaccel cuda 
-i input.mp4 
-filter:v "minterpolate='mi_mode=mci:mc_mode=aobmc:vsbmc=1:fps=60" 
-ac 6 -map 0 -c:a ac3 
output_60fps.mp4

```
