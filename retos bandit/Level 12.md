## Objetivo
The password for the next level is stored in the file **data.txt**, which is a hexdump of a file that has been repeatedly compressed. For this level it may be useful to create a directory under /tmp in which you can work using mkdir. For example: mkdir /tmp/myname123. Then copy the datafile using cp, and rename it using mv (read the manpages!)
## Datos de acceso al nivel
**bandit.labs.overthewire.org**
bandit12
Pasword
JVNBBFSmZwKKOP0XbFXOoW8chDz5yVRv
## Solucion
```
cat data.txt | xxd -r | zcat | bzcat | zcat | tar xO | tar xO| bzcat | tar xO | zcat 
The password is wbWdlBxEir4CaE8LaPhauuOo6pwRmrDw
```
## Notas adicionales 
Algunos comandos necesitan un - para tomar la salida de la izquierda
## Referencias
