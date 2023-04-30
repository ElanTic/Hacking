## Descripcion
How about some hide and seek heh? Look at this image [here](https://artifacts.picoctf.net/c/240/atbash.jpg).

## Pistas 
****** 
## Solucion
```
jt@jt-VirtualBox:~/Desktop/repos/files$ steghide extract -sf atbash.jpg 
Enter passphrase: 
wrote extracted data to "encrypted.txt".
jt@jt-VirtualBox:~/Desktop/repos/files$ cat encrypted.txt 
krxlXGU{zgyzhs_xizxp_xz00558y}
```

https://gchq.github.io/CyberChef/#recipe=Atbash_Cipher()&input=a3J4bFhHVXt6Z3l6aHNfeGl6eHBfeHowMDU1OHl9

## bandera
picoCTF{atbash_crack_ca00558b}

## Notas adicionales 

## Referencias