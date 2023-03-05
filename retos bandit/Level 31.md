## Objetivo
There is a git repository at `ssh://bandit31-git@localhost/home/bandit31-git/repo`. The password for the user `bandit31-git` is the same as for the user `bandit31`.

Clone the repository and find the password for the next level.

## Datos de acceso al nivel
**bandit.labs.overthewire.org**
bandit31
Pasword
OoffzGDlzhAlerFJ2cAiz1D41JW1Mhmt
****** 
## Solucion
```
bandit31@bandit:~$ mktemp -d
/tmp/tmp.kzXCI3ntk6
bandit31@bandit:~$ cd /tmp/tmp.kzXCI3ntk6
bandit31@bandit:/tmp/tmp.kzXCI3ntk6$ git clone ssh://bandit31-git@localhost:2220/home/bandit31-git/repo
...
bandit31@bandit:/tmp/tmp.kzXCI3ntk6$ ls
repo
bandit31@bandit:/tmp/tmp.kzXCI3ntk6$ cd repo/
bandit31@bandit:/tmp/tmp.kzXCI3ntk6/repo$ ls
README.md
bandit31@bandit:/tmp/tmp.kzXCI3ntk6/repo$ cat README.md 
This time your task is to push a file to the remote repository.

Details:
    File name: key.txt
    Content: 'May I come in?'
    Branch: master

bandit31@bandit:/tmp/tmp.kzXCI3ntk6/repo$ cat > key.txt
May I come in?
^C
bandit31@bandit:/tmp/tmp.kzXCI3ntk6/repo$ git add key.txt 
The following paths are ignored by one of your .gitignore files:
key.txt
hint: Use -f if you really want to add them.
hint: Turn this message off by running
hint: "git config advice.addIgnoredFile false"
bandit31@bandit:/tmp/tmp.kzXCI3ntk6/repo$ git commit -m "added key"
On branch master
Your branch is up to date with 'origin/master'.

nothing to commit, working tree clean
bandit31@bandit:/tmp/tmp.kzXCI3ntk6/repo$ git add .
bandit31@bandit:/tmp/tmp.kzXCI3ntk6/repo$ git commit -m "added key"
On branch master
Your branch is up to date with 'origin/master'.

nothing to commit, working tree clean
bandit31@bandit:/tmp/tmp.kzXCI3ntk6/repo$ ls
key.txt  README.md
bandit31@bandit:/tmp/tmp.kzXCI3ntk6/repo$ ls -la
total 24
drwxrwxr-x 3 bandit31 bandit31 4096 Mar  5 02:17 .
drwx------ 3 bandit31 bandit31 4096 Mar  5 02:16 ..
drwxrwxr-x 8 bandit31 bandit31 4096 Mar  5 02:18 .git
-rw-rw-r-- 1 bandit31 bandit31    6 Mar  5 02:16 .gitignore
-rw-rw-r-- 1 bandit31 bandit31   15 Mar  5 02:17 key.txt
-rw-rw-r-- 1 bandit31 bandit31  147 Mar  5 02:16 README.md
bandit31@bandit:/tmp/tmp.kzXCI3ntk6/repo$ nano .gitignore
```

```
*.tnt
```

```

Unable to create directory /home/bandit31/.local/share/nano/: No such file or directory
It is required for saving/loading search history or cursor positions.

bandit31@bandit:/tmp/tmp.kzXCI3ntk6/repo$ git add .
bandit31@bandit:/tmp/tmp.kzXCI3ntk6/repo$ git commit -m "added key"
[master 99f4e06] added key
 2 files changed, 2 insertions(+), 1 deletion(-)
 create mode 100644 key.txt
bandit31@bandit:/tmp/tmp.kzXCI3ntk6/repo$ git push
The authenticity of host '[localhost]:2220 ([127.0.0.1]:2220)' can't be established.
ED25519 key fingerprint is SHA256:C2ihUBV7ihnV1wUXRb4RrEcLfXC5CXlhmAAM/urerLY.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Could not create directory '/home/bandit31/.ssh' (Permission denied).
Failed to add the host to the list of known hosts (/home/bandit31/.ssh/known_hosts).
                         _                     _ _ _   
                        | |__   __ _ _ __   __| (_) |_ 
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_ 
                        |_.__/ \__,_|_| |_|\__,_|_|\__|
                                                       

                      This is an OverTheWire game server. 
            More information on http://www.overthewire.org/wargames

bandit31-git@localhost's password: 
Enumerating objects: 6, done.
Counting objects: 100% (6/6), done.
Delta compression using up to 2 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (4/4), 335 bytes | 335.00 KiB/s, done.
Total 4 (delta 0), reused 0 (delta 0), pack-reused 0
remote: ### Attempting to validate files... ####
remote: 
remote: .oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.
remote: 
remote: Well done! Here is the password for the next level:
remote: rmCBvG56y58BXzv98yZGdO7ATVL5dW8y 
remote: 
remote: .oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.
remote: 
To ssh://localhost:2220/home/bandit31-git/repo
 ! [remote rejected] master -> master (pre-receive hook declined)
error: failed to push some refs to 'ssh://localhost:2220/home/bandit31-git/repo'
```
## Notas adicionales 

## Referencias
