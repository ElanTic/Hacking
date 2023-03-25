## Descripcion
Our flag printing service has started glitching! `$ nc saturn.picoctf.net 50363`

## Pistas 
****** 
## Solucion
```
jt@jt-VirtualBox:~/Desktop/seguridad$ cat > gcat.py
print(
^C
jt@jt-VirtualBox:~/Desktop/seguridad$ nc saturn.picoctf.net 50363 >> gcat.py

jt@jt-VirtualBox:~/Desktop/seguridad$ cat gcat.py
print(
'picoCTF{gl17ch_m3_n07_' + chr(0x61) + chr(0x34) + chr(0x33) + chr(0x39) + chr(0x32) + chr(0x64) + chr(0x32) + chr(0x65) + '}'
jt@jt-VirtualBox:~/Desktop/seguridad$ cat  >> gcat.py 
)
^C
jt@jt-VirtualBox:~/Desktop/seguridad$ python3 gcat.py
picoCTF{gl17ch_m3_n07_a4392d2e}
```
## bandera
picoCTF{gl17ch_m3_n07_a4392d2e}

## Notas adicionales 

## Referencias