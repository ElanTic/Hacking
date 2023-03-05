## Objetivo
The password for the next level is stored **somewhere on the server** and has all of the following properties:

-   owned by user bandit7
-   owned by group bandit6
-   33 bytes in size
## Datos de acceso al nivel
**bandit.labs.overthewire.org**
bandit6
Pasword
P4L4vucdmLnm8I7Vl7jG1ApGSfjYKqJU
****** 
## Solucion
```
bandit6@bandit:~$ find / -type f -group bandit6 -user bandit7 -size 33c 2>/dev/null
/var/lib/dpkg/info/bandit7.password
bandit6@bandit:~$ cat /var/lib/dpkg/info/bandit7.password 
z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S
bandit6@bandit:~$ 
```
## Notas adicionales 

## Referencias
[Ignorar permisos denegados](https://www.cyberciti.biz/faq/bash-find-exclude-all-permission-denied-messages/)
