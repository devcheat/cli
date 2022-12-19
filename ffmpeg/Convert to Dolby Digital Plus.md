Convert to Dolby Digital Plus
===

```shell
#!/bin/bash


IN=$1
OUT=$2

echo -e "Converting ${IN} to 2.1 channel to Dolby Digital Plus Movie "

ffmpeg -i "${IN}" -filter_complex "[0:a]pan=2.1|FL=FL|FR=FR|LFE<FL+FR[a]" -map 0 -map -0:a -map "[a]" -c copy -c:a eac3 "${OUT}"

```

