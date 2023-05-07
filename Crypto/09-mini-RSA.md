## Descripcion
Let's decrypt this: [ciphertext](https://jupiter.challenges.picoctf.org/static/d21037ad23ed84cfff20a84768a0f2b2/ciphertext)? Something seems a bit small.
## Pistas 
****** 
## Solucion
```python
>>> from gmpy2 import *
>>> from Crypto.Util.number import long_to_bytes
>>> c = 2205316413931134031074603746928247799030155221252519872650073010782049179856976080512716237308882294226369300412719995904064931819531456392957957122459640736424089744772221933500860936331459280832211445548332429338572369823704784625368933
>>> e = 3
>>> gmpy2.get_context().precision=2048
>>> root, exact = iroot(c,e)
>>> long_to_bytes(root)
b'picoCTF{n33d_a_lArg3r_e_ccaa7776}'

```

## bandera
picoCTF{n33d_a_lArg3r_e_ccaa7776}
## Notas adicionales 

## Referencias