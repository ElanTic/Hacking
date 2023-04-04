## Descripcion
We found this [file](https://mercury.picoctf.net/static/da18eed3d15fd04f7b076bdcecf15b27/tunn3l_v1s10n). Recover the flag

## Pistas 
****** 
## Solucion
```
jt@jt-VirtualBox:~/Desktop/seguridad/tunelv$ hexeditor tunn3l_v1s10n 

File: tunn3l_v1s10n               ASCII Offset: 0x0000000B / 0x002C268D (%00)  M
00000000  42 4D 8E 26  2C 00 00 00   00 00 28 00  00 00 28 00   BM.&,.....(...(.
00000010  00 00 6E 04  00 00 32 01   00 00 01 00  18 00 00 00   ..n...2.........
00000020  00 00 58 26  2C 00 25 16   00 00 25 16  00 00 00 00   ..X&,.%...%.....

jt@jt-VirtualBox:~/Desktop/seguridad/tunelv$ hexeditor out 

File: out                     ASCII Offset: 0x00000000 / 0x002C268D (%00)  
00000000  42 4D 8E 26  2C 00 00 00   00 00 28 00  00 00 28 00 .&,.....(...(.
00000010  00 00 6E 04  00 00 32 04   00 00 01 00  18 00 00 00 n...2.........

jt@jt-VirtualBox:~/Desktop/seguridad/tunelv$ open out 
```
## bandera
picoCTF{qu1t3_a_v13w_2020}

## Notas adicionales 

## Referencias