## Introducción
Decode this [message](https://jupiter.challenges.picoctf.org/static/14393e18d98fedbaedbc28896d7ef31a/message.wav) from the moon.

1.-How did pictures from the moon landing get sent back to Earth?
2.-What is the CMU mascot?, that might help select a RX option
## Descripción
```
┌──(kali㉿kali)-[~/monn]
└─$ sstv -d message.w -o result.png
usage: sstv [-h] [-d AUDIO_FILE] [-o OUTPUT_FILE] [-s SKIP] [-V]
            [--list-modes] [--list-audio-formats] [--list-image-formats]
sstv: error: argument -d/--decode: can't open 'message.w': [Errno 2] No such file or directory: 'message.w'
                                                                               
┌──(kali㉿kali)-[~/monn]
└─$ sstv -d message.wav -o result.png
[sstv] Searching for calibration header... Found!    
[sstv] Detected SSTV mode Scottie 1
[sstv] Decoding image...   [#############################################] 100%
[sstv] Drawing image data...
[sstv] ...Done!
                                                                               
┌──(kali㉿kali)-[~/monn]
└─$ open result.png
                                                                               
┌──(kali㉿kali)-[~/monn]
└─$ 





```

## Solución 
picoCTF{beep_boop_im_in_space}