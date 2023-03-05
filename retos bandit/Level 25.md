## Objetivo
Logging in to bandit26 from bandit25 should be fairly easy… The shell for user bandit26 is not **/bin/bash**, but something else. Find out what it is, how it works and how to break out of it.
## Datos de acceso al nivel
**bandit.labs.overthewire.org**
bandit25
Pasword
p7TaowMYrmu23Ol8hiZh9UvD0O9hpx8d
****** 
## Solucion
```shell
cat /etc/passwd | grep bandit26
cat /usr/bin/showtext
ssh -i bandit26.sshkey bandit26@localhost -p2220
ssh -i bandit26.sshkey bandit26@localhost -p2220
bandit25@bandit:~$ ssh -i bandit26.sshkey bandit26@localhost -p  
2220  
| | | (_) | |__ \ / /  
| |__ __ _ _ __ __| |_| |_ ) / /_  
| '_ \ / _` | '_ \ / _` | | __| / / '_ \  
| |_) | (_| | | | | (_| | | |_ / /| (_) |  
--More--(83%)  
v  
_ _ _ _ ___ __  
| | | (_) | |__ \ / /  
| |__ __ _ _ __ __| |_| |_ ) / /_  
| '_ \ / _` | '_ \ / _` | | __| / / '_ \  
| |_) | (_| | | | | (_| | | |_ / /| (_) |  
"~/text.txt" [readonly] 6L, 258B  
:e /etc/bandit_pass/bandit26  
c7GvcKlw9mC7aUQaPx7nwFstuAIBw1o1  
~  
~  
~  
~  
"/etc/bandit_pass/bandit26" [readonly] 1L, 33B

```
## Notas adicionales 

## Referencias
