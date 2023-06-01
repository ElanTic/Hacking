## Descripcion
Can you figure out what is in the `eax` register? Put your answer in the picoCTF flag format: `picoCTF{n}` where `n` is the contents of the `eax` register in the decimal number base. If the answer was `0x11` your flag would be `picoCTF{17}`. Download the assembly dump [here](https://artifacts.picoctf.net/c/511/disassembler-dump0_d.txt).

## Pistas

## Solucion
```python
>>> a = int('0x9fe1a' , 16)
>>> a - int('0x65', 16)
654773
```
## bandera
picoCTF{654773}

## Notas adicionales 

## Referencias