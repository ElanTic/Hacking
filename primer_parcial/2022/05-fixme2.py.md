## Descripcion
Fix the syntax error in the Python script to print the flag. [Download Python script](https://artifacts.picoctf.net/c/6/fixme2.py)
## Pistas 
****** 
## Solucion
```
python3 fixme2.py 
  File "/home/jt/Desktop/seguridad/fixme2.py", line 22
    if flag = "":
       ^^^^^^^^^
SyntaxError: invalid syntax. Maybe you meant '==' or ':=' instead of '='?
jt@jt-VirtualBox:~/Desktop/seguridad$ nano fixme2.py 

```
---
```python
if flag == "":
  print('String XOR encountered a problem, quitting.')
```
---
```
jt@jt-VirtualBox:~/Desktop/seguridad$ python3 fixme2.py 
That is correct! Here's your flag: picoCTF{3qu4l1ty_n0t_4551gnm3nt_f6a5aefc}

```
## bandera
picoCTF{3qu4l1ty_n0t_4551gnm3nt_f6a5aefc}

## Notas adicionales 

## Referencias