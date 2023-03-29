## Descripcion
We found this [file](https://jupiter.challenges.picoctf.org/static/ab30fcb7d47364b4190a7d3d40edb551/mystery). Recover the flag.
## Pistas 
****** 
## Solucion
```
jt@jt-VirtualBox:~/Desktop/seguridad$ xxd -l 32 mystery 
00000000: 8965 4e34 0d0a b0aa 0000 000d 4322 4452  .eN4........C"DR
00000010: 0000 066a 0000 0447 0802 0000 007c 8bab  ...j...G.....|..




jt@jt-VirtualBox:~/Desktop/seguridad$ hexeditor  mystery 


File: mystery2                    ASCII Offset: 0x00000000 / 0x000318BB (%00)  
00000000  89 50 4E 47  0D 0A 1A 0A   00 00 00 0D  43 22 44 52   .PNG........C"DR
00000010  00 00 06 6A  00 00 04 47   08 02 00 00  00 7C 8B AB   ...j...G.....|..
00000020  78 00 00 00  01 73 52 47   42 00 AE CE  1C E9 00 00   x....sRGB.......

jt@jt-VirtualBox:~/Desktop/seguridad$ pngcheck -v mystery2
File: mystery2 (202940 bytes)
  invalid chunk name "C"DR" (43 22 44 52)
ERRORS DETECTED in mystery2
jt@jt-VirtualBox:~/Desktop/seguridad$ hexeditor mystery2


File: mystery2                    ASCII Offset: 0x00000000 / 0x000318BB (%00)  
00000000  89 50 4E 47  0D 0A 1A 0A   00 00 00 0D  49 48 44 52   .PNG........IHDR
00000010  00 00 06 6A  00 00 04 47   08 02 00 00  00 7C 8B AB   ...j...G.....|..



```
## bandera
picoCTF{}

## Notas adicionales 

## Referencias