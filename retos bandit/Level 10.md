
## Objetivo
The password for the next level is stored in the file **data.txt**, which contains base64 encoded data

## Datos de acceso al nivel

**bandit.labs.overthewire.org**
bandit10
Pasword
G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s
## Solucion
Forma 1
```shell
cat data.txt | base64 -d
```
Forma 2
```python
#metodo alternativo
base 64.b64.decode(cadena)
```

The password is 6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM

## Notas adicionales 
los simbolos ==  alfinal de una cadena ayudan a saber si esta codificado en base 64


## Referencias