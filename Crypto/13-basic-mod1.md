## Descripcion
We found this weird message being passed around on the servers, we think we have a working decryption scheme. Download the message [here](https://artifacts.picoctf.net/c/127/message.txt). Take each number mod 37 and map it to the following character set: 0-25 is the alphabet (uppercase), 26-35 are the decimal digits, and 36 is an underscore. Wrap your decrypted message in the picoCTF flag format (i.e. `picoCTF{decrypted_message}`)

## Pistas 
****** 
## Solucion
```python
f = open('message.txt').read().split()
#print(f)

flag =''
for n in f:
	n = int(n) % 37
	if (n < 26):
		c =chr( n + 65)
	elif n<=35:
		c = chr(n + 22)
	else:
		c = '_'
	flag += c
print(flag)
```
```
jt@jt-VirtualBox:~/Desktop/repos/files$ python3 exp.py 
R0UND_N_R0UND_79C18FB3
```

## bandera
picoCTF{R0UND_N_R0UND_79C18FB3}

## Notas adicionales 

## Referencias