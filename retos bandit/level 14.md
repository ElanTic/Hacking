## Objetivo
The password for the next level can be retrieved by submitting the password of the current level to **port 30000 on localhost**

## Datos de acceso al nivel
**bandit.labs.overthewire.org**
bandit14
Pasword
fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq
****** 
## Solucion
```
bandit14@bandit:~$ cat /etc/bandit_pass/bandit14
fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq
bandit14@bandit:~$ nc localhost 30000
fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq
Correct!
jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt


bandit14@bandit:~$ 
```
## Notas adicionales 

## Referencias
