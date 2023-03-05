## Objetivo
The password for the next level is stored in the file **data.txt** in one of the few human-readable strings, preceded by several ‘=’ characters.

## Datos de acceso al nivel
**bandit.labs.overthewire.org**
bandit9
Pasword
EN632PlfYiZbn3PhVK3XOGSlNInNE00t
****** 
## Solucion
```
 strings data.txt | grep "=="
f========== theM
========== password
========== is
========== G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s
```
## Notas adicionales 

## Referencias
