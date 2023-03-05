## Objetivo
There is a git repository at `ssh://bandit30-git@localhost/home/bandit30-git/repo`. The password for the user `bandit30-git` is the same as for the user `bandit30`.

Clone the repository and find the password for the next level.

## Datos de acceso al nivel
**bandit.labs.overthewire.org**
bandit30
Pasword
xbhV3HpNGlTIdnjUrdAlPzc2L6y9EOnS
****** 
## Solucion
```
bandit30@bandit:~$ mktemp -d
/tmp/tmp.i8Y2YBMZUJ
bandit30@bandit:~$ cd /tmp/tmp.i8Y2YBMZUJ
bandit30@bandit:/tmp/tmp.i8Y2YBMZUJ$ git clone ssh://bandit30-git@localhost:2220/home/bandit30-git/repo
...
bandit30@bandit:/tmp/tmp.i8Y2YBMZUJ$ cd repo/
bandit30@bandit:/tmp/tmp.i8Y2YBMZUJ/repo$ ls
README.md
bandit30@bandit:/tmp/tmp.i8Y2YBMZUJ/repo$ cat README.md 
just an epmty file... muahaha
bandit30@bandit:/tmp/tmp.i8Y2YBMZUJ/repo$ git log
commit cf552c166d78421e64ddf52f850e680075d216e1 (HEAD -> master, origin/master, origin/HEAD)
Author: Ben Dover <noone@overthewire.org>
Date:   Tue Feb 21 22:03:13 2023 +0000

    initial commit of README.md
bandit30@bandit:/tmp/tmp.i8Y2YBMZUJ/repo$ git branch -a
* master
  remotes/origin/HEAD -> origin/master
  remotes/origin/master
bandit30@bandit:/tmp/tmp.i8Y2YBMZUJ/repo$ ls -la
total 16
drwxrwxr-x 3 bandit30 bandit30 4096 Mar  5 02:03 .
drwx------ 3 bandit30 bandit30 4096 Mar  5 02:03 ..
drwxrwxr-x 8 bandit30 bandit30 4096 Mar  5 02:03 .git
-rw-rw-r-- 1 bandit30 bandit30   30 Mar  5 02:03 README.md
bandit30@bandit:/tmp/tmp.i8Y2YBMZUJ/repo$ git tag
secret
bandit30@bandit:/tmp/tmp.i8Y2YBMZUJ/repo$ git show secret
OoffzGDlzhAlerFJ2cAiz1D41JW1Mhmt
bandit30@bandit:/tmp/tmp.i8Y2YBMZUJ/repo$ 
```
## Notas adicionales 

## Referencias
