## Descripcion
The flag is somewhere on this web application not necessarily on the website. Find it. Check [this](http://saturn.picoctf.net:64271/) out.
## Pistas 
****** 
## Solucion
```
User-agent *
Disallow: /cgi-bin/
Think you have seen your flag or want to keep looking.

ZmxhZzEudHh0;anMvbXlmaW
anMvbXlmaWxlLnR4dA==
svssshjweuiwl;oiho.bsvdaslejg
Disallow: /wp-admin/
```

```
jt@jt-VirtualBox:~/Desktop/repos/files$ echo anMvbXlmaWxlLnR4dA | base64 -d
js/myfile.txtbase64: invalid input
jt@jt-VirtualBox:~/Desktop/repos/files$ 

```
http://saturn.picoctf.net:64271/js/myfile.txt
## bandera
picoCTF{Who_D03sN7_L1k5_90B0T5_032f1c2b}
## Notas adicionales 

## Referencias