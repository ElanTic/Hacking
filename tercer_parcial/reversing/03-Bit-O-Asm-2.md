## Descripcion
Can you figure out what is in the `eax` register? Put your answer in the picoCTF flag format: `picoCTF{n}` where `n` is the contents of the `eax` register in the decimal number base. If the answer was `0x11` your flag would be `picoCTF{17}`. Download the assembly dump [here](https://artifacts.picoctf.net/c/510/disassembler-dump0_b.txt).

## Pistas

## Solucion
```python
>>> int('0x9fe1a' , 16)
654874
```
## bandera
picoCTF{654874}

## Notas adicionales 

## Referencias