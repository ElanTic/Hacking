## Descripcion
We have recovered a [binary](https://jupiter.challenges.picoctf.org/static/31c9b832d036a10daeef52d8b4290ef0/rev) and a [text file](https://jupiter.challenges.picoctf.org/static/31c9b832d036a10daeef52d8b4290ef0/rev_this). Can you reverse the flag
## Pistas 
****** 
## Solucion
```python
rev = open('rev_this').read()
for j in range(8,len(rev)-1):
	if j & 1 == 0:
		print(chr(ord(rev[j])-5), end = '')
	else:
		print(chr(ord(rev[j])+2), end = '')
```

```
picoCTF{w1{1wq85jc=2i0<}jt@jt-VirtualBox:~/Desktop/repos/files/reversing$ python3 exploit.py 
r3v3rs37ee84d27jt@jt-VirtualBox:~/Desktop/repos/files/reversing$ 
```

## bandera
picoCTF{r3v3rs37ee84d27}
## Notas adicionales 

## Referencias