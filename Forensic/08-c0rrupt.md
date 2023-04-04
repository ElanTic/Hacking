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

jt@jt-VirtualBox:~/Desktop/seguridad$ pngcheck -v mystery2
File: mystery2 (202940 bytes)
  chunk IHDR at offset 0x0000c, length 13
    1642 x 1095 image, 24-bit RGB, non-interlaced
  chunk sRGB at offset 0x00025, length 1
    rendering intent = perceptual
  chunk gAMA at offset 0x00032, length 4: 0.45455
  chunk pHYs at offset 0x00042, length 9: 5669x5669 pixels/meter (144 dpi)
:  invalid chunk length (too large)
ERRORS DETECTED in mystery2

File: mystery2                                  ASCII Offset: 0x00000000 / 0x000318BB (%00)  
00000000  89 50 4E 47  0D 0A 1A 0A   00 00 00 0D  49 48 44 52                 .PNG........IHDR
00000010  00 00 06 6A  00 00 04 47   08 02 00 00  00 7C 8B AB                 ...j...G.....|..
00000020  78 00 00 00  01 73 52 47   42 00 AE CE  1C E9 00 00                 x....sRGB.......
00000030  00 04 67 41  4D 41 00 00   B1 8F 0B FC  61 05 00 00                 ..gAMA......a...
00000040  00 09 70 48  59 73 00 00   16 25 00 00  16 25 01 49                 ..pHYs...%...%.I
00000050  52 24 F0 00  00 FF A5 49   44 41 54 78  5E EC BD 3F                 R$.....IDATx^..?
00000060  8E 64 CD 71  BD 2D 8B 20   20 80 90 41  83 02 08 D0 


```
## bandera
picoCTF{c0rrupt10n_1847995}

## Notas adicionales 

## Referencias