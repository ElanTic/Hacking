## Objetivo
A program is running automatically at regular intervals from **cron**, the time-based job scheduler. Look in **/etc/cron.d/** for the configuration and see what command is being executed.

**NOTE:** Looking at shell scripts written by other people is a very useful skill. The script for this level is intentionally made easy to read. If you are having problems understanding what it does, try executing it to see the debug information it prints.

## Datos de acceso al nivel
**bandit.labs.overthewire.org**
bandit22
Pasword
WdDozAdTM2z9DiFEQ2mGlwngMfj4EZff
****** 
## Solucion
```shell
myname=bandit23
bandit22@bandit:~$ mytarget=$(echo I am user $myname | md5sum | cut -d ' ' -f 1) 
bandit22@bandit:~$ $mytarget
8ca319486bfbbc3663ea0fbe81326349: command not found
bandit22@bandit:~$ cat /tmp/8ca319486bfbbc3663ea0fbe81326349
QYw0Y2aiA672PsMmh9puTQuhoz8SyR2G

```
## Notas adicionales 

## Referencias