## Descripcion
In RSA, a small `e` value can be problematic, but what about `N`? Can you decrypt this? [values](https://mercury.picoctf.net/static/51d68e61bb41207a55f24e753f07c5a3/values)

## Pistas 
****** 
## Solucion
http://factordb.com/index.php?query=1280678415822214057864524798453297819181910621573945477544758171055968245116423923
```python
>>> n = 1280678415822214057864524798453297819181910621573945477544758171055968245116423923
>>> p = 1899107986527483535344517113948531328331
>>> q = 674357869540600933870145899564746495319033
>>> tn = (p-1) * (q-1)
>>> e = 65537
>>> d =  inverse(e,tn)
>>> m = pow(c,d,n)
>>> long_to_bytes(m)
b'picoCTF{sma11_N_n0_g0od_05012767}'
>>> 

```
## bandera
picoCTF{sma11_N_n0_g0od_05012767}

## Notas adicionales 

## Referencias