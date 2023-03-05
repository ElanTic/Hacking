## Objetivo
There is a git repository at `ssh://bandit28-git@localhost/home/bandit28-git/repo`. The password for the user `bandit28-git` is the same as for the user `bandit28`.

Clone the repository and find the password for the next level.

## Datos de acceso al nivel
**bandit.labs.overthewire.org**
bandit28
Pasword
AVanL161y9rsbcJIsFHuw35rjaOM19nR

****** 
## Solucion
```
bandit28@bandit:~$ mktemp -d
/tmp/tmp.senrS3WouW
bandit28@bandit:~$ cd /tmp/tmp.senrS3WouW
bandit28@bandit:/tmp/tmp.senrS3WouW$ git clone ssh://bandit28-git@localhost:2220/home/bandit28-git/repo

bandit28@bandit:/tmp/tmp.senrS3WouW$ cd repo
bandit28@bandit:/tmp/tmp.senrS3WouW/repo$ ls
README.md
bandit28@bandit:/tmp/tmp.senrS3WouW/repo$ cat README.md 
# Bandit Notes
Some notes for level29 of bandit.

## credentials

- username: bandit29
- password: xxxxxxxxxx

bandit28@bandit:/tmp/tmp.senrS3WouW/repo$ git log
commit 104db85a904e9691ff22aafe1a96124c88f75afa (HEAD -> master, origin/master, origin/HEAD)
Author: Morla Porla <morla@overthewire.org>
Date:   Tue Feb 21 22:03:10 2023 +0000

    fix info leak

commit 6c3c5e485cc531e5d52c321587ce1103833ab7c3
Author: Morla Porla <morla@overthewire.org>
Date:   Tue Feb 21 22:03:10 2023 +0000

    add missing data

commit cd3b97ef95879ec34df0d6c82f2a96d552f0e56c
Author: Ben Dover <noone@overthewire.org>
Date:   Tue Feb 21 22:03:10 2023 +0000

    initial commit of README.md

git show 104db85a904e9691ff22aafe1a96124c88f75afa
commit 104db85a904e9691ff22aafe1a96124c88f75afa (HEAD -> master, origin/master, origin/HEAD)
Author: Morla Porla <morla@overthewire.org>
Date:   Tue Feb 21 22:03:10 2023 +0000

    fix info leak

diff --git a/README.md b/README.md
index b302105..5c6457b 100644
--- a/README.md
+++ b/README.md
@@ -4,5 +4,5 @@ Some notes for level29 of bandit.
 ## credentials
 
 - username: bandit29
-- password: tQKvmcwNYcFS6vmPHIUSI3ShmsrQZK8S
+- password: xxxxxxxxxx
 

```
## Notas adicionales 

## Referencias
