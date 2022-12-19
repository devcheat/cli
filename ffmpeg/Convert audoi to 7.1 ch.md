Convert audio to 7.1 ch
===

```shell
#!/bin/bash

echo "Convert Movie Audio to 7.1 Channel audio"

INPUT=$1
OUTPUT=$2

ffmpeg -i "${INPUT}" -filter_complex "[0:a]pan=7.1(side)|FL = FL|FR = FR|LFE < FL+FR|SL = FL|SR = FR|FC < FL*0.5 + FR*0.5|BC < FL*0.5 + FR*0.5[a]" -map 0 -map -0:a -map "[a]" -c copy -c:a flac "${OUTPUT}"

echo "File coneverted to: ${OUTPUT}"
```
