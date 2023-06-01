## Descripcion
Our data got corrupted on the way here. Luckily, nothing got replaced, but every block of 3 got scrambled around! The first word seems to be three letters long, maybe you can use that to recover the rest of the message. Download the corrupted message [here](https://artifacts.picoctf.net/c/193/message.txt).

## Pistas
## Solucion
```python
file = open("message.txt", "r")
txt = file.read()
n=3
corrupto = [txt[i:i+n] for i in range(0, len(txt), n)]
decode = []
for i in range(len(corrupto)):
        print(corrupto[i][2]+corrupto[i][0]+corrupto[i][1], end='')
```

```
jt@jt-VirtualBox:~/Desktop/repos/files/P3$ python3 decoder.py 
The flag is picoCTF{7R4N5P051N6_15_3XP3N51V3_A9AFB178}
```
## bandera
picoCTF{7R4N5P051N6_15_3XP3N51V3_A9AFB178}

## Notas adicionales 

## Referencias