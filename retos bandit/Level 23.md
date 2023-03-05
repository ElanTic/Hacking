## Objetivo
A program is running automatically at regular intervals from **cron**, the time-based job scheduler. Look in **/etc/cron.d/** for the configuration and see what command is being executed.

**NOTE:** This level requires you to create your own first shell-script. This is a very big step and you should be proud of yourself when you beat this level!

**NOTE 2:** Keep in mind that your shell script is removed once executed, so you may want to keep a copy around…

## Datos de acceso al nivel
**bandit.labs.overthewire.org**
bandit23
Pasword
QYw0Y2aiA672PsMmh9puTQuhoz8SyR2G

****** 
## Solucion
```
 nano elan02script.sh
Unable to create directory /home/bandit23/.local/share/nano/: No such file or directory
It is required for saving/loading search history or cursor positions.

bandit23@bandit:/tmp/elan02$ chmod 777 elan02script.sh
bandit23@bandit:/tmp/elan02$  touch password
bandit23@bandit:/tmp/elan02$ ls
elan02script.sh  password
bandit23@bandit:/tmp/elan02$ cat password 
bandit23@bandit:/tmp/elan02$ cat password 
bandit23@bandit:/tmp/elan02$ cat password 
bandit23@bandit:/tmp/elan02$ cat password 
bandit23@bandit:/tmp/elan02$ nano elan02script.sh
Unable to create directory /home/bandit23/.local/share/nano/: No such file or directory
It is required for saving/loading search history or cursor positions.

bandit23@bandit:/tmp/elan02$ cat password 
bandit23@bandit:/tmp/elan02$ nano elan02script.sh
Unable to create directory /home/bandit23/.local/share/nano/: No such file or directory
It is required for saving/loading search history or cursor positions.

bandit23@bandit:/tmp/elan02$ cp elan02script.sh /var/spool/bandit24/foo
bandit23@bandit:/tmp/elan02$ cat password 
bandit23@bandit:/tmp/elan02$ cat password 
bandit23@bandit:/tmp/elan02$ date
Tue Feb 28 06:41:28 PM UTC 2023
bandit23@bandit:/tmp/elan02$ date
Tue Feb 28 06:41:35 PM UTC 2023
bandit23@bandit:/tmp/elan02$ date
Tue Feb 28 06:41:53 PM UTC 2023
bandit23@bandit:/tmp/elan02$ cat password 
bandit23@bandit:/tmp/elan02$ date
Tue Feb 28 06:42:22 PM UTC 2023
bandit23@bandit:/tmp/elan02$ date
Tue Feb 28 06:42:37 PM UTC 2023
bandit23@bandit:/tmp/elan02$ cat password 
bandit23@bandit:/tmp/elan02$ nano elan02script.sh
Unable to create directory /home/bandit23/.local/share/nano/: No such file or directory
It is required for saving/loading search history or cursor positions.

bandit23@bandit:/tmp/elan02$ chmod 666 password 
elan02script.sh  password         
bandit23@bandit:/tmp/elan02$ chmod 666 password 
bandit23@bandit:/tmp/elan02$ ls
elan02script.sh  password
bandit23@bandit:/tmp/elan02$ date
Tue Feb 28 06:44:09 PM UTC 2023
bandit23@bandit:/tmp/elan02$ cat password 
bandit23@bandit:/tmp/elan02$ cat password 
bandit23@bandit:/tmp/elan02$ chmod 777 elan02script.sh
bandit23@bandit:/tmp/elan02$ cp elan02script.sh /var/spool/bandit24/foo
bandit23@bandit:/tmp/elan02$ cat password 
bandit23@bandit:/tmp/elan02$ date
Tue Feb 28 06:44:55 PM UTC 2023
bandit23@bandit:/tmp/elan02$ cat password 
VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar
bandit23@bandit:/tmp/elan02$ 

```
## Notas adicionales 

## Referencias