## Descripcion
Run the `runme.py` script to get the flag. Download the script with your browser or with `wget` in the webshell. [Download runme.py Python script](https://artifacts.picoctf.net/c/34/runme.py)

## Pistas 
****** 
## Solucion
```
jt@jt-VirtualBox:~/Desktop/seguridad$ wget https://artifacts.picoctf.net/c/34/runme.py
--2023-03-25 16:01:50--  https://artifacts.picoctf.net/c/34/runme.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 18.160.124.34, 18.160.124.119, 18.160.124.38, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|18.160.124.34|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 270 [application/octet-stream]
Saving to: ‘runme.py’

runme.py            100%[===================>]     270  --.-KB/s    in 0s      

2023-03-25 16:01:51 (25.0 MB/s) - ‘runme.py’ saved [270/270]

jt@jt-VirtualBox:~/Desktop/seguridad$ python3 runme.py 
picoCTF{run_s4n1ty_run}


```
## bandera
picoCTF{run_s4n1ty_run}

## Notas adicionales 

## Referencias