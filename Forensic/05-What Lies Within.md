## Descripcion
There's something in the [building](https://jupiter.challenges.picoctf.org/static/011955b303f293d60c8116e6a4c5c84f/buildings.png). Can you retrieve the flag?

## Pistas 
****** 
## Solucion
```
jt@jt-VirtualBox:~/Downloads$ zsteg -a buildings.png | grep picoCTF{
b1,rgb,lsb,xy       .. text: "picoCTF{h1d1ng_1n_th3_b1t5}"
jt@jt-VirtualBox:~/Downloads$ 
```
## bandera
picoCTF{h1d1ng_1n_th3_b1t5}

## Notas adicionales 

## Referencias