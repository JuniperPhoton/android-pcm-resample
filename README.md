android-pcm-resample
====================

Android resample library written in Java ported from JSSRC.

## Note

The original repo is lack of detailed description on usage, so I fork it and try to add some details.

Currently, the `downsample` and `upsample` have too many params, which all has a blur concept about itself.

However, the C program should work as expected. The original author has compiled a c program for both Windows and macOS, you can use it to resample your wav file.

To figure out the params used in `downsample` and `upsample`, you can print them in the original `sample.c` and use them as a input in your code.

## Compile

In mac, you use gcc to compile the program using:

```
$> make
```

Then use it to convert a wav with 44100hz to 48000hz.

```
$> ./ssrc_hp --rate 48000 "./input.wav" "./output.wav"
```
