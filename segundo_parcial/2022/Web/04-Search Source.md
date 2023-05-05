## Descripcion
The developer of this website mistakenly left an important artifact in the website source, can you find it? The website is [here](http://saturn.picoctf.net:52523/)

## Pistas 
****** 
## Solucion
```
jt@jt-VirtualBox:~/Desktop/repos/files$ wget -m http://saturn.picoctf.net:52523/
jt@jt-VirtualBox:~/Desktop/repos/files$ cd saturn.picoctf.net\:52523/
jt@jt-VirtualBox:~/Desktop/repos/files/saturn.picoctf.net:52523$ grep -r . -e picoCTF{
./css/style.css:/** banner_main picoCTF{1nsp3ti0n_0f_w3bpag3s_ec95fa49} **/

```
## bandera
picoCTF{1nsp3ti0n_0f_w3bpag3s_ec95fa49}
## Notas adicionales 

## Referencias