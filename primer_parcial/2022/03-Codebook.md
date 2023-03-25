## Descripcion
Run the Python script `code.py` in the same directory as `codebook.txt`.

-   [Download code.py](https://artifacts.picoctf.net/c/2/code.py)
-   [Download codebook.txt](https://artifacts.picoctf.net/c/2/codebook.txt)

## Pistas 
****** 
## Solucion
```
jt@jt-VirtualBox:~/Desktop/seguridad$ wget https://artifacts.picoctf.net/c/2/code.py
--2023-03-25 16:11:15--  https://artifacts.picoctf.net/c/2/code.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 18.160.124.108, 18.160.124.119, 18.160.124.34, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|18.160.124.108|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1278 (1.2K) [application/octet-stream]
Saving to: ‘code.py’

code.py             100%[===================>]   1.25K  --.-KB/s    in 0s      

2023-03-25 16:11:15 (248 MB/s) - ‘code.py’ saved [1278/1278]

jt@jt-VirtualBox:~/Desktop/seguridad$ wget https://artifacts.picoctf.net/c/2/codebook.txt
--2023-03-25 16:11:34--  https://artifacts.picoctf.net/c/2/codebook.txt
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 18.160.124.119, 18.160.124.34, 18.160.124.38, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|18.160.124.119|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 27 [application/octet-stream]
Saving to: ‘codebook.txt’

codebook.txt        100%[===================>]      27  --.-KB/s    in 0s      

2023-03-25 16:11:34 (8.04 MB/s) - ‘codebook.txt’ saved [27/27]

jt@jt-VirtualBox:~/Desktop/seguridad$ python3 code.py 
picoCTF{c0d3b00k_455157_7d102d7a}

```
## bandera
picoCTF{c0d3b00k_455157_7d102d7a}

## Notas adicionales 

## Referencias