## Descripcion
Connect to this PostgreSQL server and find the flag!
Connect to this PostgreSQL server and find the flag! `psql -h saturn.picoctf.net -p 49409 -U postgres pico` Password is `postgres`
## Pistas 
****** 
## Solucion
```
pico=# SELECT table_name FROM information_schema.tables;
pico=# SELECT * FROM flags;
 id | firstname | lastname  |                address                 
----+-----------+-----------+----------------------------------------
  1 | Luke      | Skywalker | picoCTF{L3arN_S0m3_5qL_t0d4Y_21c94904}
  2 | Leia      | Organa    | Alderaan
  3 | Han       | Solo      | Corellia
(3 rows)

```

## bandera
picoCTF{L3arN_S0m3_5qL_t0d4Y_21c94904}
## Notas adicionales 

## Referencias