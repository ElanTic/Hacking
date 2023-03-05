## Objetivo
There is a git repository at `ssh://bandit29-git@localhost/home/bandit29-git/repo`. The password for the user `bandit29-git` is the same as for the user `bandit29`.

Clone the repository and find the password for the next level.

## Datos de acceso al nivel
**bandit.labs.overthewire.org**
bandit29
Pasword
tQKvmcwNYcFS6vmPHIUSI3ShmsrQZK8S
****** 
## Solucion
```
bandit29@bandit:~$ mktemp -d
/tmp/tmp.JyhwRh2dtI
bandit29@bandit:~$ cd /tmp/tmp.JyhwRh2dtI
bandit29@bandit:/tmp/tmp.JyhwRh2dtI$ git clone ssh://bandit29-git@localhost:2220/home/bandit29-git/repo.

bandit29@bandit:/tmp/tmp.JyhwRh2dtI/repo$ cat README.md 
# Bandit Notes
Some notes for bandit30 of bandit.

## credentials

- username: bandit30
- password: <no passwords in production!>

bandit29@bandit:/tmp/tmp.JyhwRh2dtI/repo$ git log
commit 0afe3501277395fbfa017480925edee3df6e8bb5 (HEAD -> master, origin/master, origin/HEAD)
Author: Ben Dover <noone@overthewire.org>
Date:   Tue Feb 21 22:03:11 2023 +0000

	fix username

commit c2606dfc0aef7179bf1ccd6cffa9ed19151facb4
Author: Ben Dover <noone@overthewire.org>
Date:   Tue Feb 21 22:03:11 2023 +0000

	initial commit of README.md
bandit29@bandit:/tmp/tmp.JyhwRh2dtI/repo$ git show 0afe3501277395fbfa017480925edee3df6e8bb5
commit 0afe3501277395fbfa017480925edee3df6e8bb5 (HEAD -> master, origin/master, origin/HEAD)
Author: Ben Dover <noone@overthewire.org>
Date:   Tue Feb 21 22:03:11 2023 +0000

	fix username

diff --git a/README.md b/README.md
index 2da2f39..1af21d3 100644
--- a/README.md
+++ b/README.md
@@ -3,6 +3,6 @@ Some notes for bandit30 of bandit.
 
 ## credentials
 
-- username: bandit29
+- username: bandit30
 - password: <no passwords in production!>
 
bandit29@bandit:/tmp/tmp.JyhwRh2dtI/repo$ git branch -a
* master
  remotes/origin/HEAD -> origin/master
  remotes/origin/dev
  remotes/origin/master
  remotes/origin/sploits-dev
bandit29@bandit:/tmp/tmp.JyhwRh2dtI/repo$ git checkout remotes/origin/dev
Note: switching to 'remotes/origin/dev'.

You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by switching back to a branch.

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -c with the switch command. Example:

  git switch -c <new-branch-name>

Or undo this operation with:

  git switch -

Turn off this advice by setting config variable advice.detachedHead to false

HEAD is now at fbbce0e add data needed for development
bandit29@bandit:/tmp/tmp.JyhwRh2dtI/repo$ git branch
* (HEAD detached at origin/dev)
  master
bandit29@bandit:/tmp/tmp.JyhwRh2dtI/repo$ ls
code  README.md

bandit29@bandit:/tmp/tmp.JyhwRh2dtI/repo$ cat README.md 
# Bandit Notes
Some notes for bandit30 of bandit.

## credentials

- username: bandit30
- password: xbhV3HpNGlTIdnjUrdAlPzc2L6y9EOnS

bandit29@bandit:/tmp/tmp.JyhwRh2dtI/repo$ 

```
## Notas adicionales 

## Referencias
[como cambiar de ramas en git](https://support.atlassian.com/bitbucket-cloud/docs/check-out-a-branch/)