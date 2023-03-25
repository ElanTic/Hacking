## Descripcion
Fix the syntax error in this Python script to print the flag. [Download Python script](https://artifacts.picoctf.net/c/25/fixme1.py)

## Pistas 
****** 
## Solucion
```
python3 fixme1.py 
  File "/home/jt/Desktop/seguridad/fixme1.py", line 20
    print('That is correct! Here\'s your flag: ' + flag)
IndentationError: unexpected indent
jt@jt-VirtualBox:~/Desktop/seguridad$ nano fixme1.py 
```
---
```python
flag = str_xor(flag_enc, 'enkidu'):
print('That is correct! Here\'s your flag: ' + flag)
```
---
```
jt@jt-VirtualBox:~/Desktop/seguridad$ python3 fixme1.py 
That is correct! Here's your flag: picoCTF{1nd3nt1ty_cr1515_6a476c8f}

```
## bandera
picoCTF{1nd3nt1ty_cr1515_6a476c8f}

## Notas adicionales 

## Referencias