## Objetivo
The password for the next level is stored in the file **data.txt**, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions
## Datos de acceso al nivel
**bandit.labs.overthewire.org**
bandit11
Pasword
6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM
## Solucion
Forma 1
```shell
cat data.txt | tr [a-zA-Z] [n-za-mN-ZA-M]
The password is JVNBBFSmZwKKOP0XbFXOoW8chDz5yVRv
```
## Notas adicionales 

## Referencias