## Objetivo
There is a git repository at `ssh://bandit27-git@localhost/home/bandit27-git/repo`. The password for the user `bandit27-git` is the same as for the user `bandit27`.

## Datos de acceso al nivel
**bandit.labs.overthewire.org**
bandit27
YnQpBuifNMas1hcUFk70ZmqkhUU2EuaS
****** 
## Solucion
```
 mktemp -d
/tmp/tmp.cFiJ40kQEs
bandit27@bandit:~$ cd /tmp/tmp.cFiJ40kQEs
git clone ssh://bandit27-git@localhost:2220/home/bandit27-git/repo
cd repo/
bandit27@bandit:/tmp/tmp.cFiJ40kQEs/repo$ ls
README
bandit27@bandit:/tmp/tmp.cFiJ40kQEs/repo$ cat README 
The password to the next level is: AVanL161y9rsbcJIsFHuw35rjaOM19nR

```
## Notas adicionales 

## Referencias