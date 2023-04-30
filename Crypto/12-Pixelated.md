## Descripcion
I have these 2 images, can you make a flag out of them? [scrambled1.png](https://mercury.picoctf.net/static/1594c3f1980e3fb93df09a6d02f53904/scrambled1.png) [scrambled2.png](https://mercury.picoctf.net/static/1594c3f1980e3fb93df09a6d02f53904/scrambled2.png)

## Pistas 
****** 
## Solucion
```
jt@jt-VirtualBox:~/Desktop/repos/files$ convert scrambled1.png scrambled2.png -compose Add -composite flag.png
jt@jt-VirtualBox:~/Desktop/repos/files$ open flag.png 
```
## bandera
picoCTF{1b867c3e}

## Notas adicionales 

## Referencias