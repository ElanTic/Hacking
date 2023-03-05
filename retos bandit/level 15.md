## Objetivo
The password for the next level can be retrieved by submitting the password of the current level to **port 30001 on localhost** using SSL encryption.

**Helpful note: Getting “HEARTBEATING” and “Read R BLOCK”? Use -ign_eof and read the “CONNECTED COMMANDS” section in the manpage. Next to ‘R’ and ‘Q’, the ‘B’ command also works in this version of that command…**

## Datos de acceso al nivel
**bandit.labs.overthewire.org**
bandit15
Pasword
jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt
****** 
## Solucion
```
bandit15@bandit:~$ openssl s_client -connect localhost:30001
CONNECTED(00000003)
Can't use SSL_get_servername
depth=0 CN = localhost
verify error:num=18:self-signed certificate
verify return:1
depth=0 CN = localhost
verify error:num=10:certificate has expired
notAfter=Mar  4 13:56:53 2023 GMT
verify return:1
depth=0 CN = localhost
notAfter=Mar  4 13:56:53 2023 GMT
verify return:1
---
...
---
read R BLOCK
jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt
Correct!
JQttfApK4SeyHwDlI9SXGR50qclOAil1

closed

```
## Notas adicionales 

## Referencias
