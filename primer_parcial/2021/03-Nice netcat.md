## Descripcion
There is a nice program that you can talk to by using this command in a shell: `$ nc mercury.picoctf.net 43239`, but it doesn't speak English...

## Pistas 
****** 
## Solucion
```python
while (True):
	i = input()
	if(i == None or i == ""):
		print(".")
		break
	print (chr(int(i)), end = "")

```
---
```
jt@jt-VirtualBox:~$ nc mercury.picoctf.net 43239 | python3 test.py
picoCTF{g00d_k1tty!_n1c3_k1tty!_7c0821f5}

```
## bandera
picoCTF{g00d_k1tty!_n1c3_k1tty!_7c0821f5}

## Notas adicionales 

## Referencias